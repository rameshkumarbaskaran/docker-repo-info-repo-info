<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `caddy`

-	[`caddy:2`](#caddy2)
-	[`caddy:2-alpine`](#caddy2-alpine)
-	[`caddy:2-builder`](#caddy2-builder)
-	[`caddy:2-builder-alpine`](#caddy2-builder-alpine)
-	[`caddy:2-builder-windowsservercore-1809`](#caddy2-builder-windowsservercore-1809)
-	[`caddy:2-builder-windowsservercore-ltsc2022`](#caddy2-builder-windowsservercore-ltsc2022)
-	[`caddy:2-windowsservercore`](#caddy2-windowsservercore)
-	[`caddy:2-windowsservercore-1809`](#caddy2-windowsservercore-1809)
-	[`caddy:2-windowsservercore-ltsc2022`](#caddy2-windowsservercore-ltsc2022)
-	[`caddy:2.6`](#caddy26)
-	[`caddy:2.6-alpine`](#caddy26-alpine)
-	[`caddy:2.6-builder`](#caddy26-builder)
-	[`caddy:2.6-builder-alpine`](#caddy26-builder-alpine)
-	[`caddy:2.6-builder-windowsservercore-1809`](#caddy26-builder-windowsservercore-1809)
-	[`caddy:2.6-builder-windowsservercore-ltsc2022`](#caddy26-builder-windowsservercore-ltsc2022)
-	[`caddy:2.6-windowsservercore`](#caddy26-windowsservercore)
-	[`caddy:2.6-windowsservercore-1809`](#caddy26-windowsservercore-1809)
-	[`caddy:2.6-windowsservercore-ltsc2022`](#caddy26-windowsservercore-ltsc2022)
-	[`caddy:2.6.4`](#caddy264)
-	[`caddy:2.6.4-alpine`](#caddy264-alpine)
-	[`caddy:2.6.4-builder`](#caddy264-builder)
-	[`caddy:2.6.4-builder-alpine`](#caddy264-builder-alpine)
-	[`caddy:2.6.4-builder-windowsservercore-1809`](#caddy264-builder-windowsservercore-1809)
-	[`caddy:2.6.4-builder-windowsservercore-ltsc2022`](#caddy264-builder-windowsservercore-ltsc2022)
-	[`caddy:2.6.4-windowsservercore`](#caddy264-windowsservercore)
-	[`caddy:2.6.4-windowsservercore-1809`](#caddy264-windowsservercore-1809)
-	[`caddy:2.6.4-windowsservercore-ltsc2022`](#caddy264-windowsservercore-ltsc2022)
-	[`caddy:alpine`](#caddyalpine)
-	[`caddy:builder`](#caddybuilder)
-	[`caddy:builder-alpine`](#caddybuilder-alpine)
-	[`caddy:builder-windowsservercore-1809`](#caddybuilder-windowsservercore-1809)
-	[`caddy:builder-windowsservercore-ltsc2022`](#caddybuilder-windowsservercore-ltsc2022)
-	[`caddy:latest`](#caddylatest)
-	[`caddy:windowsservercore`](#caddywindowsservercore)
-	[`caddy:windowsservercore-1809`](#caddywindowsservercore-1809)
-	[`caddy:windowsservercore-ltsc2022`](#caddywindowsservercore-ltsc2022)

## `caddy:2`

```console
$ docker pull caddy@sha256:236163a87c5609986ce7ddead7d8aaf992314f031699ddde2a400597640965e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.3887; amd64
	-	windows version 10.0.20348.1487; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:36ba71b44afa613ecf0aadce8e4b9e3f56e0c4b0a78c8edf4e8c2485f21b35ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17449113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8464e23f16f9a82426bbdc3ac8c94270a84453ddc86b9147505a2378a7c2fd0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:38:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 11 Feb 2023 07:38:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 19:19:21 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 19:19:23 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 19:19:24 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:25 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 19:19:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e3e797818bc929d95bae8220b7b6034b559c217ef5bf622dc7fedc8d270a48`  
		Last Modified: Sat, 11 Feb 2023 07:39:01 GMT  
		Size: 351.2 KB (351178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cebb4c80b3906a9b751ee9a512c1581331b1fd691c84f575c01a29e28403dde`  
		Last Modified: Sat, 11 Feb 2023 07:39:00 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90648ba22c191b969d8db393bf6138e7d6ecc1b70b3865d1717ec4d663192d89`  
		Last Modified: Wed, 15 Feb 2023 19:19:52 GMT  
		Size: 14.3 MB (14282621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5b39c4c37396031351c9753e4c7df6f2114d0ef588953b97c668d0ec7e2f1e50
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16582274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ffa8388ed5f7f62ab116b850faa63ff3214dea5fb007a77196a8efd0023832`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:28:54 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 21:28:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:49:22 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:49:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:49:26 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:49:26 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:49:27 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:49:28 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:49:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a400dcba29ff44f8e5bf01493def4f19629aca6d103cb2a66ca87c457f7414`  
		Last Modified: Fri, 10 Feb 2023 21:29:47 GMT  
		Size: 345.8 KB (345811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b946768825eb5ed2fc6f932fdb0b0c552f4c35c39dada07eddd70ce4a535953`  
		Last Modified: Fri, 10 Feb 2023 21:29:47 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f11ff5bb8d752ef2e91afa46770077fd62ddc9e78f280c00e796bf841c9d49f`  
		Last Modified: Wed, 15 Feb 2023 18:50:25 GMT  
		Size: 13.6 MB (13612205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:21302c9acb44ea61fccba3ef765712da93fede2d928aaafc8f7bd77a35d91953
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16365562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600d5193b2ba5875b66a6579717ec1aab50be117445a5a657045572141d1187c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:37 GMT
ADD file:193f48d48ed2e90a0e81663757e372f59806151c17e82113f03443db0ef723c3 in / 
# Fri, 10 Feb 2023 21:51:37 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:37:19 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:37:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:57:27 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:57:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:57:30 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:57:30 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:57:31 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:57:32 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:beefe5ad637c7db32e6afc68103fc4e779630219979216a625338ab55f7d191c`  
		Last Modified: Fri, 10 Feb 2023 21:52:51 GMT  
		Size: 2.4 MB (2420494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2ab4edb1f0a14b28a55f050d62d8e54111075639a0fa8f173448814ba0d00`  
		Last Modified: Fri, 10 Feb 2023 22:38:25 GMT  
		Size: 342.6 KB (342588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0580184dd0082f009564a7a3923731f202cbe4bd8b857dbca2c77da8e7434815`  
		Last Modified: Fri, 10 Feb 2023 22:38:25 GMT  
		Size: 7.5 KB (7479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8682e09bc231d5c9076b76cb92cb3b1185b870277da03dbd7e87d7981ff6147a`  
		Last Modified: Wed, 15 Feb 2023 18:58:28 GMT  
		Size: 13.6 MB (13595001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:6c2623f6bf30798be5c37fc7484e45ecc288d493fb657883f59ddb27ed714ad8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16130997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a38afdc517ef4cff6b6b51a1c6a633c2826599b07feb1e88380d0f783e35cf1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:00:35 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:00:37 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:39:20 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:39:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:39:22 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:39:22 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:39:23 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:39:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70730e8e2fb933ec157ec87f2a4fb4ad45e8e578b8f7c76cc4846631d773554`  
		Last Modified: Fri, 10 Feb 2023 22:01:02 GMT  
		Size: 350.2 KB (350153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a4b7390d269477c225f1d03e825d2d8bdf6b4d87b5f7bb8811b341e56b7d36`  
		Last Modified: Fri, 10 Feb 2023 22:01:02 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2743d2ef53ee6edb0e39c89bf16957e3a00990410b2d1a126dca1b2d196182`  
		Last Modified: Wed, 15 Feb 2023 18:39:53 GMT  
		Size: 13.1 MB (13063787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:8861ab3ae3d0c180e38142c2f7482f9ce1773419eb29ed9d6d18308246858093
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15955172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5819f0ab4928a30c29293a27299a3b44371cd3bd97df91432ef7b3f43b692d8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:13:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:13:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 19:16:26 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:16:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 19:16:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 19:16:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 19:16:42 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:16:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:16:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:16:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:16:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:16:47 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:16:47 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 19:16:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782bd0321e6539bb7dac8574fd36bad22059ef06bb63dc842165f69d0a821572`  
		Last Modified: Fri, 10 Feb 2023 22:14:16 GMT  
		Size: 363.1 KB (363088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb806b2600b0209a73fc7175ab778d0224661034b2f722bd1a0aec1eb9eabe3d`  
		Last Modified: Fri, 10 Feb 2023 22:14:15 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd7c8ae860931dd79dea76d33bc21bb11d89cd4d133cdb41078b040afc6633e`  
		Last Modified: Wed, 15 Feb 2023 19:17:41 GMT  
		Size: 12.8 MB (12779898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:4e1ed99f133abf02d6a7c77849978bb621f748e18c9cb9f7a1dbf88480ddb8d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16792756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45cd164da734310b788dcbd4f6c94bccff6e48705fe4d42ecca07a54e9459a9c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:14:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:41:48 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:41:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:41:59 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:41:59 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:42:00 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:42:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:42:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:42:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:42:03 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:42:04 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:42:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:42:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:42:05 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:42:06 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:42:07 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:42:07 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:42:08 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:42:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e6ec82400496ce74e37120e1655955b79303daaa5b8ca7e956e3cd96ddd6e9`  
		Last Modified: Fri, 10 Feb 2023 22:15:05 GMT  
		Size: 352.8 KB (352801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5b992687f93ced3715ad97bd95ab37daef5685b784e195209caefbc48f14e9`  
		Last Modified: Fri, 10 Feb 2023 22:15:05 GMT  
		Size: 7.6 KB (7557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccc40924ce2df3343fa5465a92ccaa4ed80e0883190a99d3f468c60f9ddbcf8`  
		Last Modified: Wed, 15 Feb 2023 18:43:19 GMT  
		Size: 13.8 MB (13838817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:371255c187169392f30d7caf1e65b8a8708afbdd8520eb74df9c38d973195766
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723380167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa79dce896513046be66642ea60c82eaf2266ff5533f3e8c40a79c7b779c0eca`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:16:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:15:47 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:17:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:17:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:17:11 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:17:12 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:17:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:17:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:17:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:17:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:17:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:17:20 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:17:21 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:17:22 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:17:24 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:17:43 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:17:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47af8a9c9ef8e49d65e53dd207ad0935ce7a2b50b2f253e6a5b037494ae19d0a`  
		Last Modified: Thu, 09 Feb 2023 01:16:50 GMT  
		Size: 401.5 KB (401472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d742cb3ca192278158c048ecc9f358855bc8f2629af70c62b9610a1fc66bbf0a`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859ce744a498d8f5affa0958dae6a0027cd48925c7c0bdf78214019c927eb34b`  
		Last Modified: Wed, 15 Feb 2023 20:17:06 GMT  
		Size: 14.7 MB (14694270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64525df3f764c2e65e711fbd328781c61243029c264aca6b09309e584dbb69b3`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231e1956368caba27b753959bf1fb5d38cf0e798477a45110f2691b063809554`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405677c240161263f0ca900ffca71596061f8d59668d524a80f16957c120f0c`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638a2e8fc9bd411f13b7b5a8b82272fd39024ac9b711d2bc73c28c39314fc3bb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1b8ca9045f120e19c22debd19df59f42aa442b84c073c7cfc2f5a2d0f463cb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c7468bd4bec28c11efd397d435df6a129ffc73265d2d2c4162bb121a336d08`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de41f5feb06b95a77601b9fd09ab7409b567e0d9684c46dfcdc4a067a00adc`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab6a97db0980bf9c94414bfb713b5db0ed7bec52a805303782c4309a6e9f62b`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41271d7026e5d15682fc59b1ac99ac0a67909c591ea0c7ab0885207386064744`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b605f7b22df792b7b41d97cec04cbfb795ba3588fd9e0b44363147a7a02820`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c2c11f6f75de707c6475d6248a27eb983282648b0a923c47e2894db7304e0d`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48461b499cb5763190c69d134f0b96625458bdd69fe78a15ade15efbad156033`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745ffdaac1ecada0622ef6d6ccfe6140992921240b91567821b96a07a72df8b8`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf9895ba16206d3ebb35a3a6e3f615542102d00230528158c62eee814428521`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc57c33625ddac815d78d81c0feb25f7dd3d6ea9f6d4f6238024e4898a15ef3c`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 316.4 KB (316447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31243cdae7d3d8bcf0b00d6c6c0a1f4ec3c2c277ca964f747f8acc133cef56a2`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:0722e548c2efb29869e87e89dc7cf03de8d31fe33c28e9e61a33f018b0a7a3e4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1401943529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a230b066a2fbe8bdfee6749b8afe9b1655260bb3643408c49082c8754a4cff75`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:18:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:18:03 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:19:13 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:19:14 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:19:15 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:24 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:26 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:27 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:46 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:19:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42eb48143612ee855d99c932e324b1bd035c60554117edeaa805402060613c51`  
		Last Modified: Thu, 09 Feb 2023 01:17:17 GMT  
		Size: 635.9 KB (635943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e120c0944228b4b6623b958c83433bc43f104b64cecccbd1ac7ab250e7a68db7`  
		Last Modified: Wed, 15 Feb 2023 20:17:30 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891cca6ce816bbe4dd40bd862cae84155f0da6f7f13ab15fb80f92c471772be7`  
		Last Modified: Wed, 15 Feb 2023 20:17:34 GMT  
		Size: 14.9 MB (14907106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e4718f6f1c46191ed75eaff08ff294c5ad0f384309aca914d5687324213f83`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0edcd24848e16049bee383e4ae89134f9d07da6079deed1398df66ad8a401ac`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b890b1c144cd00660796b630f5a2b8009a7c8b98a852cc4e645d13d84f4b48`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12054588e533ec29d2f174499ee24489e7b6d7b8527337dcdcc25a6ec29973`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e7efe9a5a718b562e89379f47cd1c2919b05c52ad1a2ceb9525d7f98f2f0d1`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fc39bc9c2bdee1444bb0e46b53cb55da0913be6b115f95bc50f5ed370138e`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d17482a1fa64018a51f2d8467fb3cba2c11aae5e67a689612e314d713ca8b0`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4843586865795ebb5e828c5f7fe6c9f829f9b12d5ad2e0bbf9f302874fc39a27`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd44712296ac1e7d28147c40159638788a75b58c17764de2757fcfda62f5551a`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5344aa95ac41ce0d03e95ae47d07c9ddef532b47bbfeb871053e69eacf5429a6`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf50f2a8532ee01e411b12116a827c2823a5cb2ee71091b4b724c44b6ba0f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b71f209c61027e4688f4e4b109ec883c187ed74b3d4c27e4b11596a4f20a07`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df052fc38d64efbb8657dd2c40cfa28c56f1137efcf1d7751277c1c81626b39e`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266955548153e827efba631ef21036116d523e11f332aae3910c4e6b773896f5`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59f15231c2a3b500e116b42a5254f441985197b1d364bc46a71cd917af38ec9`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 347.4 KB (347422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4a927a917a632a25082f22d95b2df35568f4522d622efe890c6d57457ed461`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:aacae65cfdcf61777306cf7c131fb968f67bb7fab8dfd683aa073e8b99867e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:36ba71b44afa613ecf0aadce8e4b9e3f56e0c4b0a78c8edf4e8c2485f21b35ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17449113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8464e23f16f9a82426bbdc3ac8c94270a84453ddc86b9147505a2378a7c2fd0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:38:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 11 Feb 2023 07:38:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 19:19:21 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 19:19:23 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 19:19:24 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:25 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 19:19:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e3e797818bc929d95bae8220b7b6034b559c217ef5bf622dc7fedc8d270a48`  
		Last Modified: Sat, 11 Feb 2023 07:39:01 GMT  
		Size: 351.2 KB (351178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cebb4c80b3906a9b751ee9a512c1581331b1fd691c84f575c01a29e28403dde`  
		Last Modified: Sat, 11 Feb 2023 07:39:00 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90648ba22c191b969d8db393bf6138e7d6ecc1b70b3865d1717ec4d663192d89`  
		Last Modified: Wed, 15 Feb 2023 19:19:52 GMT  
		Size: 14.3 MB (14282621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5b39c4c37396031351c9753e4c7df6f2114d0ef588953b97c668d0ec7e2f1e50
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16582274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ffa8388ed5f7f62ab116b850faa63ff3214dea5fb007a77196a8efd0023832`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:28:54 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 21:28:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:49:22 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:49:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:49:26 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:49:26 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:49:27 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:49:28 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:49:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a400dcba29ff44f8e5bf01493def4f19629aca6d103cb2a66ca87c457f7414`  
		Last Modified: Fri, 10 Feb 2023 21:29:47 GMT  
		Size: 345.8 KB (345811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b946768825eb5ed2fc6f932fdb0b0c552f4c35c39dada07eddd70ce4a535953`  
		Last Modified: Fri, 10 Feb 2023 21:29:47 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f11ff5bb8d752ef2e91afa46770077fd62ddc9e78f280c00e796bf841c9d49f`  
		Last Modified: Wed, 15 Feb 2023 18:50:25 GMT  
		Size: 13.6 MB (13612205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:21302c9acb44ea61fccba3ef765712da93fede2d928aaafc8f7bd77a35d91953
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16365562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600d5193b2ba5875b66a6579717ec1aab50be117445a5a657045572141d1187c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:37 GMT
ADD file:193f48d48ed2e90a0e81663757e372f59806151c17e82113f03443db0ef723c3 in / 
# Fri, 10 Feb 2023 21:51:37 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:37:19 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:37:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:57:27 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:57:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:57:30 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:57:30 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:57:31 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:57:32 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:beefe5ad637c7db32e6afc68103fc4e779630219979216a625338ab55f7d191c`  
		Last Modified: Fri, 10 Feb 2023 21:52:51 GMT  
		Size: 2.4 MB (2420494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2ab4edb1f0a14b28a55f050d62d8e54111075639a0fa8f173448814ba0d00`  
		Last Modified: Fri, 10 Feb 2023 22:38:25 GMT  
		Size: 342.6 KB (342588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0580184dd0082f009564a7a3923731f202cbe4bd8b857dbca2c77da8e7434815`  
		Last Modified: Fri, 10 Feb 2023 22:38:25 GMT  
		Size: 7.5 KB (7479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8682e09bc231d5c9076b76cb92cb3b1185b870277da03dbd7e87d7981ff6147a`  
		Last Modified: Wed, 15 Feb 2023 18:58:28 GMT  
		Size: 13.6 MB (13595001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:6c2623f6bf30798be5c37fc7484e45ecc288d493fb657883f59ddb27ed714ad8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16130997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a38afdc517ef4cff6b6b51a1c6a633c2826599b07feb1e88380d0f783e35cf1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:00:35 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:00:37 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:39:20 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:39:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:39:22 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:39:22 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:39:23 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:39:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70730e8e2fb933ec157ec87f2a4fb4ad45e8e578b8f7c76cc4846631d773554`  
		Last Modified: Fri, 10 Feb 2023 22:01:02 GMT  
		Size: 350.2 KB (350153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a4b7390d269477c225f1d03e825d2d8bdf6b4d87b5f7bb8811b341e56b7d36`  
		Last Modified: Fri, 10 Feb 2023 22:01:02 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2743d2ef53ee6edb0e39c89bf16957e3a00990410b2d1a126dca1b2d196182`  
		Last Modified: Wed, 15 Feb 2023 18:39:53 GMT  
		Size: 13.1 MB (13063787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:8861ab3ae3d0c180e38142c2f7482f9ce1773419eb29ed9d6d18308246858093
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15955172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5819f0ab4928a30c29293a27299a3b44371cd3bd97df91432ef7b3f43b692d8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:13:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:13:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 19:16:26 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:16:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 19:16:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 19:16:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 19:16:42 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:16:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:16:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:16:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:16:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:16:47 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:16:47 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 19:16:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782bd0321e6539bb7dac8574fd36bad22059ef06bb63dc842165f69d0a821572`  
		Last Modified: Fri, 10 Feb 2023 22:14:16 GMT  
		Size: 363.1 KB (363088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb806b2600b0209a73fc7175ab778d0224661034b2f722bd1a0aec1eb9eabe3d`  
		Last Modified: Fri, 10 Feb 2023 22:14:15 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd7c8ae860931dd79dea76d33bc21bb11d89cd4d133cdb41078b040afc6633e`  
		Last Modified: Wed, 15 Feb 2023 19:17:41 GMT  
		Size: 12.8 MB (12779898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:4e1ed99f133abf02d6a7c77849978bb621f748e18c9cb9f7a1dbf88480ddb8d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16792756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45cd164da734310b788dcbd4f6c94bccff6e48705fe4d42ecca07a54e9459a9c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:14:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:41:48 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:41:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:41:59 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:41:59 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:42:00 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:42:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:42:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:42:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:42:03 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:42:04 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:42:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:42:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:42:05 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:42:06 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:42:07 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:42:07 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:42:08 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:42:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e6ec82400496ce74e37120e1655955b79303daaa5b8ca7e956e3cd96ddd6e9`  
		Last Modified: Fri, 10 Feb 2023 22:15:05 GMT  
		Size: 352.8 KB (352801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5b992687f93ced3715ad97bd95ab37daef5685b784e195209caefbc48f14e9`  
		Last Modified: Fri, 10 Feb 2023 22:15:05 GMT  
		Size: 7.6 KB (7557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccc40924ce2df3343fa5465a92ccaa4ed80e0883190a99d3f468c60f9ddbcf8`  
		Last Modified: Wed, 15 Feb 2023 18:43:19 GMT  
		Size: 13.8 MB (13838817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:f3ac019c2a9615cd1adc2555d81ba8eb0412bfea8c34290fc0adfc7d77a468e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.3887; amd64
	-	windows version 10.0.20348.1487; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:47722ffc694507be1e2f34ca172e292fb5e226ea68d87871300b9d65f543fcce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131421587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4674ac67a52f4d29bc8349e9dcca7db8393d778c97c79d9e2f6e997603a99cd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 08:21:54 GMT
RUN apk add --no-cache ca-certificates
# Sat, 11 Feb 2023 08:21:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:24:10 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:25:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:25:43 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:25:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:25:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:25:44 GMT
WORKDIR /go
# Tue, 14 Feb 2023 19:47:10 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 19:47:10 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:19:27 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:19:28 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 19:19:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 19:19:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 19:19:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d21d5440ebff5aaaaeb115a003f7a4a3897f1866a87de95bc4a21436fc563c`  
		Last Modified: Sat, 11 Feb 2023 08:29:10 GMT  
		Size: 284.8 KB (284816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f790f4c5274f100158d4c23bc5eddf659c1fe93ef4025488f9493d88f1490d88`  
		Last Modified: Tue, 14 Feb 2023 19:31:12 GMT  
		Size: 122.4 MB (122355677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bf170fd9e6726c86c0d4b478d9ec522e82c527a8e708668f48233a4d03f618`  
		Last Modified: Tue, 14 Feb 2023 19:30:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a5d1c1b6ed103f8c7f97c73ed546ff7e767b10473b55c15c0d4e1a13a69481`  
		Last Modified: Tue, 14 Feb 2023 19:47:34 GMT  
		Size: 4.2 MB (4188243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0130eaa2f0b1f7646719d82927743bd84c83ed450eb8be4db5327d280d5e4d0`  
		Last Modified: Wed, 15 Feb 2023 19:20:05 GMT  
		Size: 1.2 MB (1217841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab1f57409241476a86d26944527bc2c6c3903eadb21221b8d96da52120b3109`  
		Last Modified: Wed, 15 Feb 2023 19:20:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ef43980c42cd8a35929f0378a7ecd1918acd54140264da387b01dc7e3d6bea0b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127437368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd812dbbfb10d2a70518b9169ed3ed8f3e00b43a8b7ce2f98f7e72b09d33330`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:49:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 21:49:23 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:54:56 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:57:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:57:12 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:57:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:57:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:57:13 GMT
WORKDIR /go
# Tue, 14 Feb 2023 21:22:55 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 21:22:55 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:49:33 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:49:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:49:33 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:49:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:49:35 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:49:35 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11114cba5e5d7175bb4d5b434db94e1c2bf0f8263c6cf2b8cbf3c1fc853114b5`  
		Last Modified: Fri, 10 Feb 2023 22:00:04 GMT  
		Size: 286.1 KB (286119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbe98122be79c40d67ce24806b19f5bd6a2f3025a18faa3a9e07c836eda77a3`  
		Last Modified: Tue, 14 Feb 2023 20:03:20 GMT  
		Size: 118.7 MB (118722534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2006a6001995de26a92cbdcc7917c763ee43c1f153331e17ed59bc706622a4`  
		Last Modified: Tue, 14 Feb 2023 20:02:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241e307a6c2a59713b29a4001892e4737b03b8bdc797f283f8bfef8e5976a360`  
		Last Modified: Tue, 14 Feb 2023 21:23:46 GMT  
		Size: 4.2 MB (4151224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd6d861ad1e103851af9cad05cca9ddd82af819c16eef77a788212eb48a451a`  
		Last Modified: Wed, 15 Feb 2023 18:50:44 GMT  
		Size: 1.2 MB (1166072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff6cca8082ff38bb36e60b71883dc986b05c54b1322ffe5c5906933155af3db`  
		Last Modified: Wed, 15 Feb 2023 18:50:44 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ae944139e672dc9c4065b2e83f98a2c2522db0397a33f3b287e771e01c90b043
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126518789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b5e54b6cc5a620df577f3659a5f2415b1ab88786c0ee932fd73c5c026786cb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 23:34:00 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 23:34:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 22:43:55 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 22:46:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 22:46:04 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 22:46:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 22:46:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 22:46:05 GMT
WORKDIR /go
# Wed, 15 Feb 2023 01:37:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 15 Feb 2023 01:37:44 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:57:37 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:57:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:57:37 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:57:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:57:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ee22df4e0527c9d317c1729808b4fc333083ad4d5a41645d79beabb64e9415`  
		Last Modified: Fri, 10 Feb 2023 23:50:08 GMT  
		Size: 285.4 KB (285353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0083f2e9af62d9a5b5bcf25401158f3ebb34f9fe9e7e951a52b22e9f6a15f1ed`  
		Last Modified: Tue, 14 Feb 2023 22:54:26 GMT  
		Size: 118.5 MB (118480449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6506d85184bedd4e64bb66e1357511d9dde4bc32c2c99d3183c2cec84f20e7e5`  
		Last Modified: Tue, 14 Feb 2023 22:54:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc4386697a4bb55f0e63b324c4a0b444eec215aff0cffc35d7affc50fff2041`  
		Last Modified: Wed, 15 Feb 2023 01:38:34 GMT  
		Size: 3.7 MB (3720630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03d748e87e34207a999297a575c405a0c36bf6b02a35f1c1b370ae25d1daf26`  
		Last Modified: Wed, 15 Feb 2023 18:58:45 GMT  
		Size: 1.2 MB (1163331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957e61fda37fb7df272efba4e6f8cd0083db173bff77b1e4dbbfad3fba3cd92b`  
		Last Modified: Wed, 15 Feb 2023 18:58:44 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:345963f3560e208ac6bacd024a578f5b7e01f8b734c723eddee3617aa9f0eb48
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125824793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e4189a65557b7e2dd531761f337fa9ebac950fe19c378297b031b64ef548d7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:38:33 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:38:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:43:03 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:44:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:44:06 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:44:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:44:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:44:07 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:05:45 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:05:45 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:39:25 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:39:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:39:26 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:39:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:39:28 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:39:28 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55522c79112429742fe76c795b9509c5cd1e8198e0caa2a1e355c0e60a719576`  
		Last Modified: Fri, 10 Feb 2023 22:44:19 GMT  
		Size: 286.3 KB (286257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a025c151a25ec079b20475bc7d9114a55273ff4768db3589c2a9e3556263ff`  
		Last Modified: Tue, 14 Feb 2023 19:48:57 GMT  
		Size: 116.9 MB (116917630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e172ed32e80e014974dc5c64a3cec7ac2d456fe4b21179f48138df590112cdab`  
		Last Modified: Tue, 14 Feb 2023 19:48:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbab95e946333dfac53de76b5f4cfc1f90fec80107055af4eb888824c147950`  
		Last Modified: Tue, 14 Feb 2023 20:06:09 GMT  
		Size: 4.2 MB (4234639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52ae4d010a784b362566e543eeacafbef900440cdda0b182dc5ea51a53b070c`  
		Last Modified: Wed, 15 Feb 2023 18:40:08 GMT  
		Size: 1.1 MB (1123743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d9033ce04f11b49957c7855096c7e5ed4a4e3ad840dd150fc0823b230b3742`  
		Last Modified: Wed, 15 Feb 2023 18:40:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:8126a0d2b7cc9613f70b6b5375c14cc61dfca5dc1b83adc5be33efab8eacc69f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126579575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da1cd24f35f4106a8a7176a2f2b5656a22982a1787b9204d3eaab9ec535ef58`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:36 GMT
ADD file:ec037a0d4b462d12963ac20d9ec49bb73b4bcaf84d4bc7b364ebf93667e585b0 in / 
# Fri, 10 Feb 2023 21:20:36 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:40:13 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:40:14 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:46:09 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:48:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:48:44 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:48:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:48:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:48:46 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:12:48 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:12:48 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:16:53 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:16:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:16:54 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 19:16:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 19:16:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 19:16:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:aa3c56f9c6f127b6c8f628c95db165741ca400d19bdaef2752d80f093e47451e`  
		Last Modified: Fri, 10 Feb 2023 21:21:37 GMT  
		Size: 3.4 MB (3390750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788962e1689dbb14c760601cbf633ae350e98e3a045f8010924cd585de6b6a3e`  
		Last Modified: Fri, 10 Feb 2023 22:53:32 GMT  
		Size: 286.6 KB (286645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ae39b9ad00c218f9156f0958fa48f3062eb5830b791b8592e5f25fd576c7c5`  
		Last Modified: Tue, 14 Feb 2023 19:56:18 GMT  
		Size: 117.3 MB (117316160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f3bf55d586b31bb5c97f2cbf5167fd359b61336f93bed839c2f4de055ced88`  
		Last Modified: Tue, 14 Feb 2023 19:55:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e012d53123423a5fe128ab31d41596d83d8e48699ad608e9eb58dd0b2322fe0`  
		Last Modified: Tue, 14 Feb 2023 20:13:35 GMT  
		Size: 4.5 MB (4479556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90177e6cf58218f094608b8401f41d0da78a0cf57d95718e48e8c6e2f77c6fae`  
		Last Modified: Wed, 15 Feb 2023 19:18:00 GMT  
		Size: 1.1 MB (1105899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e897949e5a46b09b4606d86b20ecb5684cb43f7e1bed1f208ee9b7e93d208c`  
		Last Modified: Wed, 15 Feb 2023 19:17:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:777aec044ded48957652f0c6ceac314892e1c892c85a07084f80762791aa55b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129606877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4f36416ff115d90097fe1378fca1a1ded179a50ee13701194f1193833e1d5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:25 GMT
ADD file:03b2fb4d732a294329449ff55c5d84f7d2735e6510985718979469994f3a607b in / 
# Fri, 10 Feb 2023 21:41:26 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:27:44 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:27:44 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:47:34 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:49:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:49:23 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:49:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:49:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:49:24 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:12:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:12:32 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:42:20 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:42:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:42:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:42:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:42:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:42:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:24c4f8de3549a39c64b0edc2cfa68769b373f35138d0f13725100160bb32d4e2`  
		Last Modified: Fri, 10 Feb 2023 21:42:16 GMT  
		Size: 3.2 MB (3175116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affa53ed2f1b70a83e3a15cae881ca47cd40f6ac11060717cdbbd4e405f9d586`  
		Last Modified: Fri, 10 Feb 2023 22:37:18 GMT  
		Size: 285.0 KB (285032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafa18be4ff892e2222424e6e25c36c21c4d94825607e8b840d2384c6ab73651`  
		Last Modified: Tue, 14 Feb 2023 19:54:27 GMT  
		Size: 120.8 MB (120811850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c3965c085d018b012055d834e6c56402c39a086413f83eb42fed0eba26be6`  
		Last Modified: Tue, 14 Feb 2023 19:54:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250c53f2b7534f15112393341635149f8ad756241a7c7979ec7ad6fbd3959ff1`  
		Last Modified: Tue, 14 Feb 2023 20:13:22 GMT  
		Size: 4.2 MB (4163882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11288ef421d5fc2fc1e1a7cd7350fb7f4ad371aa6edad42bb5ffa8f95cb2f2bc`  
		Last Modified: Wed, 15 Feb 2023 18:43:31 GMT  
		Size: 1.2 MB (1170432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b792196575b477b3bd73841238a0c4445026bc982b5e0236ef24a59eec4875`  
		Last Modified: Wed, 15 Feb 2023 18:43:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:bff20886c4e50c2ff56c65ce2b8b2f6f861b63544087ebc9828b8283abf3e9ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1893205034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9666c08cd03c61fe14a234d3f8760533430f35e891dccd0f5540cb34fd9834a4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 03:01:55 GMT
ENV GIT_VERSION=2.23.0
# Thu, 12 Jan 2023 03:01:56 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 12 Jan 2023 03:01:57 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 12 Jan 2023 03:01:58 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 12 Jan 2023 03:02:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 03:03:01 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 03:03:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Feb 2023 20:35:10 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 20:39:32 GMT
RUN $url = 'https://dl.google.com/go/go1.19.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8d84af29e46c38b1eec77f9310310517c9e394ac7489e1c7329a94b443b0388d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Feb 2023 20:39:34 GMT
WORKDIR C:\go
# Tue, 14 Feb 2023 21:16:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 21:16:10 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:20:04 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:20:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Feb 2023 19:20:39 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203425975bec1802428fad91a2e5f01172b161062c12eddf729e548bf7e134e0`  
		Last Modified: Thu, 12 Jan 2023 03:48:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80e42e19ab862b4adea06f1995e1f5cbb2c11ad8d68ae4a7bb5d0da5d0e6f38`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be5d5df8cec6d1386f78a342668c3d2cb809372865459c1b35aa8d5a39a463b`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e467d553c4972b55bf8e3d80b16f245e5bb38f28d80b91ca4f9f90c09a6c28d`  
		Last Modified: Thu, 12 Jan 2023 03:48:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97054b77b205167acd5a303c8aa82e380f090ff4e2ded81d3425ec78500139d`  
		Last Modified: Thu, 12 Jan 2023 03:48:14 GMT  
		Size: 25.5 MB (25470784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e150d9e1a1da09e17313cb3b6358d2f16cf2919c51e9addf30500de9d03292ef`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c0d792e2a7942826a61fdc26b6081ab404122751ff4f4dd8f5b8b0eca21399`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 324.5 KB (324466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd89ac843c0479ae40ca8c747e8a676229754549dbfeb9fe7157fdf1a60e685f`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0892c7d4de38540a99ca06e09c0a995b2e119c5ae853eadc2f7558f69bf44bb1`  
		Last Modified: Tue, 14 Feb 2023 20:56:57 GMT  
		Size: 157.8 MB (157805981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b2ec2bef689e3f934369ec3ebb90a5b06c0cbd77b2364e23a776b4da7a68f5`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066daab446064e42a798fe1592cbb9befd18dc7c368cc287f403168c17647f44`  
		Last Modified: Tue, 14 Feb 2023 21:18:46 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ea7fb211a6a6bdf1db9842354942dfaf3dc66bb87b9ce2b1620b897655022d`  
		Last Modified: Tue, 14 Feb 2023 21:18:44 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1a9f71a17b653aeea9897c2da8205709b77073460fc648f6daa323ffffee8d`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53678f100709f21522f2dd0732c10bbb5a70107fa9a4fcdd4895786c68d0bb27`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a973e4e836b19e1ccb3104f7458b2ed9a0aee58d697b6b7a8f7b8800265560f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:53 GMT  
		Size: 1.6 MB (1641852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9b2ad53ca032d7a1d8ef1944923a40be2d6c2fbd4945695a1d7cf5ea708613`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:8208748738c8ad71587dbe2fa710487d6ed5a1ef462b3591e30be906145cab13
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1572172924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c99c2ba8e5059d5dc3ad70afada06d399bff99be54c4c7bf3908b0889a8719a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 02:57:40 GMT
ENV GIT_VERSION=2.23.0
# Thu, 12 Jan 2023 02:57:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 12 Jan 2023 02:57:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 12 Jan 2023 02:57:42 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 12 Jan 2023 02:58:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 02:58:23 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 02:58:47 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Feb 2023 20:31:21 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 20:34:49 GMT
RUN $url = 'https://dl.google.com/go/go1.19.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8d84af29e46c38b1eec77f9310310517c9e394ac7489e1c7329a94b443b0388d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Feb 2023 20:34:51 GMT
WORKDIR C:\go
# Tue, 14 Feb 2023 21:17:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 21:17:18 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:20:52 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:20:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:21:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Feb 2023 19:21:22 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2fc8728d9c7bf65edf893fd902f8b1bd780f93623858960c9db79e39922b169`  
		Last Modified: Thu, 12 Jan 2023 03:47:24 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7935a4c648078e79f67a11bcd5908e251110dd6c5a4ee49a607f332dd25af9`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d257f8b122044547f89f00f58661b25aca97c92f3831e7aaa11975639b6e35d4`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95acaa75c1852ba1320c5db382b01f587badb615b6746b59be27eedcf96ab667`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5201ba65043fa621c187729f18aecf4c549cdfa12cd6d8cab7a901d893f3a8a8`  
		Last Modified: Thu, 12 Jan 2023 03:47:29 GMT  
		Size: 25.7 MB (25702230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a317a349bca5ab28ba7c1ce039928a56390f7e7a8d7ddec07efcc1c9883e5d`  
		Last Modified: Thu, 12 Jan 2023 03:47:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8850296b8fbb853a6eb6341f7484cd4bc622e9f679f12c4123eddf08b7f398fb`  
		Last Modified: Thu, 12 Jan 2023 03:47:18 GMT  
		Size: 554.2 KB (554212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b724dc103b7bd177436e0035a2c0eaffd1187dcb978222f4e7c1014ca50ee`  
		Last Modified: Tue, 14 Feb 2023 20:55:01 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f4ea18edcbbc3120e8b270d76ae1a1876db9d493e1b703d25194e08b0896c`  
		Last Modified: Tue, 14 Feb 2023 20:55:55 GMT  
		Size: 158.0 MB (158000355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81da76ff355cb5fcac2247f23ca1fe8dd4256b41f2edd58b34f886fcb74bc6e7`  
		Last Modified: Tue, 14 Feb 2023 20:55:01 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc05ca820f63f78de074bd0a9ffe6889c8e3405b0563cf21ef5013179b8f407`  
		Last Modified: Tue, 14 Feb 2023 21:19:03 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b911bfee9062064c2f989b2acf01493bb3c9ad5989eb456277dfe272c1dcd2`  
		Last Modified: Tue, 14 Feb 2023 21:19:01 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aa3117c7e54c9d38a6d368beb815482c58bd46981294fc7c45046ca02b8d34`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710d1b3e32dd905f2dc2f33df9481f9abdd52cbd0028eadd5d0517fe673c3de1`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df812b30f4c795624a0ff09a18f3ac73987de268d9ee1aa080998e222a6f6e3`  
		Last Modified: Wed, 15 Feb 2023 20:18:10 GMT  
		Size: 1.9 MB (1868549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced4b40932769c58cc0b5348fdc7b4189892820c655d4029b988aafd8692dcd0`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:ef81823d12a3d4befb8d3dc29929c37f003682cc6a9cc8a7e8ed08442fc2644a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:47722ffc694507be1e2f34ca172e292fb5e226ea68d87871300b9d65f543fcce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131421587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4674ac67a52f4d29bc8349e9dcca7db8393d778c97c79d9e2f6e997603a99cd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 08:21:54 GMT
RUN apk add --no-cache ca-certificates
# Sat, 11 Feb 2023 08:21:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:24:10 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:25:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:25:43 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:25:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:25:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:25:44 GMT
WORKDIR /go
# Tue, 14 Feb 2023 19:47:10 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 19:47:10 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:19:27 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:19:28 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 19:19:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 19:19:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 19:19:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d21d5440ebff5aaaaeb115a003f7a4a3897f1866a87de95bc4a21436fc563c`  
		Last Modified: Sat, 11 Feb 2023 08:29:10 GMT  
		Size: 284.8 KB (284816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f790f4c5274f100158d4c23bc5eddf659c1fe93ef4025488f9493d88f1490d88`  
		Last Modified: Tue, 14 Feb 2023 19:31:12 GMT  
		Size: 122.4 MB (122355677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bf170fd9e6726c86c0d4b478d9ec522e82c527a8e708668f48233a4d03f618`  
		Last Modified: Tue, 14 Feb 2023 19:30:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a5d1c1b6ed103f8c7f97c73ed546ff7e767b10473b55c15c0d4e1a13a69481`  
		Last Modified: Tue, 14 Feb 2023 19:47:34 GMT  
		Size: 4.2 MB (4188243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0130eaa2f0b1f7646719d82927743bd84c83ed450eb8be4db5327d280d5e4d0`  
		Last Modified: Wed, 15 Feb 2023 19:20:05 GMT  
		Size: 1.2 MB (1217841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab1f57409241476a86d26944527bc2c6c3903eadb21221b8d96da52120b3109`  
		Last Modified: Wed, 15 Feb 2023 19:20:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ef43980c42cd8a35929f0378a7ecd1918acd54140264da387b01dc7e3d6bea0b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127437368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd812dbbfb10d2a70518b9169ed3ed8f3e00b43a8b7ce2f98f7e72b09d33330`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:49:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 21:49:23 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:54:56 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:57:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:57:12 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:57:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:57:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:57:13 GMT
WORKDIR /go
# Tue, 14 Feb 2023 21:22:55 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 21:22:55 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:49:33 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:49:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:49:33 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:49:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:49:35 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:49:35 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11114cba5e5d7175bb4d5b434db94e1c2bf0f8263c6cf2b8cbf3c1fc853114b5`  
		Last Modified: Fri, 10 Feb 2023 22:00:04 GMT  
		Size: 286.1 KB (286119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbe98122be79c40d67ce24806b19f5bd6a2f3025a18faa3a9e07c836eda77a3`  
		Last Modified: Tue, 14 Feb 2023 20:03:20 GMT  
		Size: 118.7 MB (118722534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2006a6001995de26a92cbdcc7917c763ee43c1f153331e17ed59bc706622a4`  
		Last Modified: Tue, 14 Feb 2023 20:02:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241e307a6c2a59713b29a4001892e4737b03b8bdc797f283f8bfef8e5976a360`  
		Last Modified: Tue, 14 Feb 2023 21:23:46 GMT  
		Size: 4.2 MB (4151224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd6d861ad1e103851af9cad05cca9ddd82af819c16eef77a788212eb48a451a`  
		Last Modified: Wed, 15 Feb 2023 18:50:44 GMT  
		Size: 1.2 MB (1166072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff6cca8082ff38bb36e60b71883dc986b05c54b1322ffe5c5906933155af3db`  
		Last Modified: Wed, 15 Feb 2023 18:50:44 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ae944139e672dc9c4065b2e83f98a2c2522db0397a33f3b287e771e01c90b043
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126518789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b5e54b6cc5a620df577f3659a5f2415b1ab88786c0ee932fd73c5c026786cb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 23:34:00 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 23:34:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 22:43:55 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 22:46:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 22:46:04 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 22:46:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 22:46:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 22:46:05 GMT
WORKDIR /go
# Wed, 15 Feb 2023 01:37:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 15 Feb 2023 01:37:44 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:57:37 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:57:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:57:37 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:57:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:57:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ee22df4e0527c9d317c1729808b4fc333083ad4d5a41645d79beabb64e9415`  
		Last Modified: Fri, 10 Feb 2023 23:50:08 GMT  
		Size: 285.4 KB (285353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0083f2e9af62d9a5b5bcf25401158f3ebb34f9fe9e7e951a52b22e9f6a15f1ed`  
		Last Modified: Tue, 14 Feb 2023 22:54:26 GMT  
		Size: 118.5 MB (118480449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6506d85184bedd4e64bb66e1357511d9dde4bc32c2c99d3183c2cec84f20e7e5`  
		Last Modified: Tue, 14 Feb 2023 22:54:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc4386697a4bb55f0e63b324c4a0b444eec215aff0cffc35d7affc50fff2041`  
		Last Modified: Wed, 15 Feb 2023 01:38:34 GMT  
		Size: 3.7 MB (3720630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03d748e87e34207a999297a575c405a0c36bf6b02a35f1c1b370ae25d1daf26`  
		Last Modified: Wed, 15 Feb 2023 18:58:45 GMT  
		Size: 1.2 MB (1163331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957e61fda37fb7df272efba4e6f8cd0083db173bff77b1e4dbbfad3fba3cd92b`  
		Last Modified: Wed, 15 Feb 2023 18:58:44 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:345963f3560e208ac6bacd024a578f5b7e01f8b734c723eddee3617aa9f0eb48
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125824793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e4189a65557b7e2dd531761f337fa9ebac950fe19c378297b031b64ef548d7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:38:33 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:38:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:43:03 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:44:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:44:06 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:44:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:44:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:44:07 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:05:45 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:05:45 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:39:25 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:39:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:39:26 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:39:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:39:28 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:39:28 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55522c79112429742fe76c795b9509c5cd1e8198e0caa2a1e355c0e60a719576`  
		Last Modified: Fri, 10 Feb 2023 22:44:19 GMT  
		Size: 286.3 KB (286257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a025c151a25ec079b20475bc7d9114a55273ff4768db3589c2a9e3556263ff`  
		Last Modified: Tue, 14 Feb 2023 19:48:57 GMT  
		Size: 116.9 MB (116917630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e172ed32e80e014974dc5c64a3cec7ac2d456fe4b21179f48138df590112cdab`  
		Last Modified: Tue, 14 Feb 2023 19:48:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbab95e946333dfac53de76b5f4cfc1f90fec80107055af4eb888824c147950`  
		Last Modified: Tue, 14 Feb 2023 20:06:09 GMT  
		Size: 4.2 MB (4234639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52ae4d010a784b362566e543eeacafbef900440cdda0b182dc5ea51a53b070c`  
		Last Modified: Wed, 15 Feb 2023 18:40:08 GMT  
		Size: 1.1 MB (1123743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d9033ce04f11b49957c7855096c7e5ed4a4e3ad840dd150fc0823b230b3742`  
		Last Modified: Wed, 15 Feb 2023 18:40:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:8126a0d2b7cc9613f70b6b5375c14cc61dfca5dc1b83adc5be33efab8eacc69f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126579575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da1cd24f35f4106a8a7176a2f2b5656a22982a1787b9204d3eaab9ec535ef58`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:36 GMT
ADD file:ec037a0d4b462d12963ac20d9ec49bb73b4bcaf84d4bc7b364ebf93667e585b0 in / 
# Fri, 10 Feb 2023 21:20:36 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:40:13 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:40:14 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:46:09 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:48:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:48:44 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:48:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:48:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:48:46 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:12:48 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:12:48 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:16:53 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:16:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:16:54 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 19:16:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 19:16:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 19:16:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:aa3c56f9c6f127b6c8f628c95db165741ca400d19bdaef2752d80f093e47451e`  
		Last Modified: Fri, 10 Feb 2023 21:21:37 GMT  
		Size: 3.4 MB (3390750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788962e1689dbb14c760601cbf633ae350e98e3a045f8010924cd585de6b6a3e`  
		Last Modified: Fri, 10 Feb 2023 22:53:32 GMT  
		Size: 286.6 KB (286645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ae39b9ad00c218f9156f0958fa48f3062eb5830b791b8592e5f25fd576c7c5`  
		Last Modified: Tue, 14 Feb 2023 19:56:18 GMT  
		Size: 117.3 MB (117316160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f3bf55d586b31bb5c97f2cbf5167fd359b61336f93bed839c2f4de055ced88`  
		Last Modified: Tue, 14 Feb 2023 19:55:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e012d53123423a5fe128ab31d41596d83d8e48699ad608e9eb58dd0b2322fe0`  
		Last Modified: Tue, 14 Feb 2023 20:13:35 GMT  
		Size: 4.5 MB (4479556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90177e6cf58218f094608b8401f41d0da78a0cf57d95718e48e8c6e2f77c6fae`  
		Last Modified: Wed, 15 Feb 2023 19:18:00 GMT  
		Size: 1.1 MB (1105899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e897949e5a46b09b4606d86b20ecb5684cb43f7e1bed1f208ee9b7e93d208c`  
		Last Modified: Wed, 15 Feb 2023 19:17:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:777aec044ded48957652f0c6ceac314892e1c892c85a07084f80762791aa55b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129606877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4f36416ff115d90097fe1378fca1a1ded179a50ee13701194f1193833e1d5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:25 GMT
ADD file:03b2fb4d732a294329449ff55c5d84f7d2735e6510985718979469994f3a607b in / 
# Fri, 10 Feb 2023 21:41:26 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:27:44 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:27:44 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:47:34 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:49:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:49:23 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:49:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:49:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:49:24 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:12:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:12:32 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:42:20 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:42:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:42:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:42:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:42:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:42:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:24c4f8de3549a39c64b0edc2cfa68769b373f35138d0f13725100160bb32d4e2`  
		Last Modified: Fri, 10 Feb 2023 21:42:16 GMT  
		Size: 3.2 MB (3175116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affa53ed2f1b70a83e3a15cae881ca47cd40f6ac11060717cdbbd4e405f9d586`  
		Last Modified: Fri, 10 Feb 2023 22:37:18 GMT  
		Size: 285.0 KB (285032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafa18be4ff892e2222424e6e25c36c21c4d94825607e8b840d2384c6ab73651`  
		Last Modified: Tue, 14 Feb 2023 19:54:27 GMT  
		Size: 120.8 MB (120811850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c3965c085d018b012055d834e6c56402c39a086413f83eb42fed0eba26be6`  
		Last Modified: Tue, 14 Feb 2023 19:54:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250c53f2b7534f15112393341635149f8ad756241a7c7979ec7ad6fbd3959ff1`  
		Last Modified: Tue, 14 Feb 2023 20:13:22 GMT  
		Size: 4.2 MB (4163882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11288ef421d5fc2fc1e1a7cd7350fb7f4ad371aa6edad42bb5ffa8f95cb2f2bc`  
		Last Modified: Wed, 15 Feb 2023 18:43:31 GMT  
		Size: 1.2 MB (1170432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b792196575b477b3bd73841238a0c4445026bc982b5e0236ef24a59eec4875`  
		Last Modified: Wed, 15 Feb 2023 18:43:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:e4b4bb126038410035c8c6962d643dbf73d0b1d8ee3108c4f005238402a9a0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:bff20886c4e50c2ff56c65ce2b8b2f6f861b63544087ebc9828b8283abf3e9ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1893205034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9666c08cd03c61fe14a234d3f8760533430f35e891dccd0f5540cb34fd9834a4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 03:01:55 GMT
ENV GIT_VERSION=2.23.0
# Thu, 12 Jan 2023 03:01:56 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 12 Jan 2023 03:01:57 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 12 Jan 2023 03:01:58 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 12 Jan 2023 03:02:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 03:03:01 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 03:03:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Feb 2023 20:35:10 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 20:39:32 GMT
RUN $url = 'https://dl.google.com/go/go1.19.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8d84af29e46c38b1eec77f9310310517c9e394ac7489e1c7329a94b443b0388d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Feb 2023 20:39:34 GMT
WORKDIR C:\go
# Tue, 14 Feb 2023 21:16:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 21:16:10 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:20:04 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:20:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Feb 2023 19:20:39 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203425975bec1802428fad91a2e5f01172b161062c12eddf729e548bf7e134e0`  
		Last Modified: Thu, 12 Jan 2023 03:48:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80e42e19ab862b4adea06f1995e1f5cbb2c11ad8d68ae4a7bb5d0da5d0e6f38`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be5d5df8cec6d1386f78a342668c3d2cb809372865459c1b35aa8d5a39a463b`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e467d553c4972b55bf8e3d80b16f245e5bb38f28d80b91ca4f9f90c09a6c28d`  
		Last Modified: Thu, 12 Jan 2023 03:48:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97054b77b205167acd5a303c8aa82e380f090ff4e2ded81d3425ec78500139d`  
		Last Modified: Thu, 12 Jan 2023 03:48:14 GMT  
		Size: 25.5 MB (25470784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e150d9e1a1da09e17313cb3b6358d2f16cf2919c51e9addf30500de9d03292ef`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c0d792e2a7942826a61fdc26b6081ab404122751ff4f4dd8f5b8b0eca21399`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 324.5 KB (324466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd89ac843c0479ae40ca8c747e8a676229754549dbfeb9fe7157fdf1a60e685f`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0892c7d4de38540a99ca06e09c0a995b2e119c5ae853eadc2f7558f69bf44bb1`  
		Last Modified: Tue, 14 Feb 2023 20:56:57 GMT  
		Size: 157.8 MB (157805981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b2ec2bef689e3f934369ec3ebb90a5b06c0cbd77b2364e23a776b4da7a68f5`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066daab446064e42a798fe1592cbb9befd18dc7c368cc287f403168c17647f44`  
		Last Modified: Tue, 14 Feb 2023 21:18:46 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ea7fb211a6a6bdf1db9842354942dfaf3dc66bb87b9ce2b1620b897655022d`  
		Last Modified: Tue, 14 Feb 2023 21:18:44 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1a9f71a17b653aeea9897c2da8205709b77073460fc648f6daa323ffffee8d`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53678f100709f21522f2dd0732c10bbb5a70107fa9a4fcdd4895786c68d0bb27`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a973e4e836b19e1ccb3104f7458b2ed9a0aee58d697b6b7a8f7b8800265560f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:53 GMT  
		Size: 1.6 MB (1641852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9b2ad53ca032d7a1d8ef1944923a40be2d6c2fbd4945695a1d7cf5ea708613`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:8bfb22a6d9ad624ddad733879370d4e05a82cc5c15125cdc2365e8f7a4fe79e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:8208748738c8ad71587dbe2fa710487d6ed5a1ef462b3591e30be906145cab13
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1572172924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c99c2ba8e5059d5dc3ad70afada06d399bff99be54c4c7bf3908b0889a8719a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 02:57:40 GMT
ENV GIT_VERSION=2.23.0
# Thu, 12 Jan 2023 02:57:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 12 Jan 2023 02:57:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 12 Jan 2023 02:57:42 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 12 Jan 2023 02:58:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 02:58:23 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 02:58:47 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Feb 2023 20:31:21 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 20:34:49 GMT
RUN $url = 'https://dl.google.com/go/go1.19.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8d84af29e46c38b1eec77f9310310517c9e394ac7489e1c7329a94b443b0388d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Feb 2023 20:34:51 GMT
WORKDIR C:\go
# Tue, 14 Feb 2023 21:17:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 21:17:18 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:20:52 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:20:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:21:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Feb 2023 19:21:22 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2fc8728d9c7bf65edf893fd902f8b1bd780f93623858960c9db79e39922b169`  
		Last Modified: Thu, 12 Jan 2023 03:47:24 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7935a4c648078e79f67a11bcd5908e251110dd6c5a4ee49a607f332dd25af9`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d257f8b122044547f89f00f58661b25aca97c92f3831e7aaa11975639b6e35d4`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95acaa75c1852ba1320c5db382b01f587badb615b6746b59be27eedcf96ab667`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5201ba65043fa621c187729f18aecf4c549cdfa12cd6d8cab7a901d893f3a8a8`  
		Last Modified: Thu, 12 Jan 2023 03:47:29 GMT  
		Size: 25.7 MB (25702230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a317a349bca5ab28ba7c1ce039928a56390f7e7a8d7ddec07efcc1c9883e5d`  
		Last Modified: Thu, 12 Jan 2023 03:47:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8850296b8fbb853a6eb6341f7484cd4bc622e9f679f12c4123eddf08b7f398fb`  
		Last Modified: Thu, 12 Jan 2023 03:47:18 GMT  
		Size: 554.2 KB (554212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b724dc103b7bd177436e0035a2c0eaffd1187dcb978222f4e7c1014ca50ee`  
		Last Modified: Tue, 14 Feb 2023 20:55:01 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f4ea18edcbbc3120e8b270d76ae1a1876db9d493e1b703d25194e08b0896c`  
		Last Modified: Tue, 14 Feb 2023 20:55:55 GMT  
		Size: 158.0 MB (158000355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81da76ff355cb5fcac2247f23ca1fe8dd4256b41f2edd58b34f886fcb74bc6e7`  
		Last Modified: Tue, 14 Feb 2023 20:55:01 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc05ca820f63f78de074bd0a9ffe6889c8e3405b0563cf21ef5013179b8f407`  
		Last Modified: Tue, 14 Feb 2023 21:19:03 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b911bfee9062064c2f989b2acf01493bb3c9ad5989eb456277dfe272c1dcd2`  
		Last Modified: Tue, 14 Feb 2023 21:19:01 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aa3117c7e54c9d38a6d368beb815482c58bd46981294fc7c45046ca02b8d34`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710d1b3e32dd905f2dc2f33df9481f9abdd52cbd0028eadd5d0517fe673c3de1`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df812b30f4c795624a0ff09a18f3ac73987de268d9ee1aa080998e222a6f6e3`  
		Last Modified: Wed, 15 Feb 2023 20:18:10 GMT  
		Size: 1.9 MB (1868549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced4b40932769c58cc0b5348fdc7b4189892820c655d4029b988aafd8692dcd0`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:a0e880f407bc812d350d220b76e5e9da56ef9a34384f075923fb0eacfc9eef27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.3887; amd64
	-	windows version 10.0.20348.1487; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:371255c187169392f30d7caf1e65b8a8708afbdd8520eb74df9c38d973195766
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723380167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa79dce896513046be66642ea60c82eaf2266ff5533f3e8c40a79c7b779c0eca`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:16:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:15:47 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:17:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:17:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:17:11 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:17:12 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:17:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:17:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:17:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:17:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:17:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:17:20 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:17:21 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:17:22 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:17:24 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:17:43 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:17:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47af8a9c9ef8e49d65e53dd207ad0935ce7a2b50b2f253e6a5b037494ae19d0a`  
		Last Modified: Thu, 09 Feb 2023 01:16:50 GMT  
		Size: 401.5 KB (401472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d742cb3ca192278158c048ecc9f358855bc8f2629af70c62b9610a1fc66bbf0a`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859ce744a498d8f5affa0958dae6a0027cd48925c7c0bdf78214019c927eb34b`  
		Last Modified: Wed, 15 Feb 2023 20:17:06 GMT  
		Size: 14.7 MB (14694270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64525df3f764c2e65e711fbd328781c61243029c264aca6b09309e584dbb69b3`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231e1956368caba27b753959bf1fb5d38cf0e798477a45110f2691b063809554`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405677c240161263f0ca900ffca71596061f8d59668d524a80f16957c120f0c`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638a2e8fc9bd411f13b7b5a8b82272fd39024ac9b711d2bc73c28c39314fc3bb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1b8ca9045f120e19c22debd19df59f42aa442b84c073c7cfc2f5a2d0f463cb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c7468bd4bec28c11efd397d435df6a129ffc73265d2d2c4162bb121a336d08`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de41f5feb06b95a77601b9fd09ab7409b567e0d9684c46dfcdc4a067a00adc`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab6a97db0980bf9c94414bfb713b5db0ed7bec52a805303782c4309a6e9f62b`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41271d7026e5d15682fc59b1ac99ac0a67909c591ea0c7ab0885207386064744`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b605f7b22df792b7b41d97cec04cbfb795ba3588fd9e0b44363147a7a02820`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c2c11f6f75de707c6475d6248a27eb983282648b0a923c47e2894db7304e0d`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48461b499cb5763190c69d134f0b96625458bdd69fe78a15ade15efbad156033`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745ffdaac1ecada0622ef6d6ccfe6140992921240b91567821b96a07a72df8b8`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf9895ba16206d3ebb35a3a6e3f615542102d00230528158c62eee814428521`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc57c33625ddac815d78d81c0feb25f7dd3d6ea9f6d4f6238024e4898a15ef3c`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 316.4 KB (316447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31243cdae7d3d8bcf0b00d6c6c0a1f4ec3c2c277ca964f747f8acc133cef56a2`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:0722e548c2efb29869e87e89dc7cf03de8d31fe33c28e9e61a33f018b0a7a3e4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1401943529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a230b066a2fbe8bdfee6749b8afe9b1655260bb3643408c49082c8754a4cff75`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:18:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:18:03 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:19:13 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:19:14 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:19:15 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:24 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:26 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:27 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:46 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:19:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42eb48143612ee855d99c932e324b1bd035c60554117edeaa805402060613c51`  
		Last Modified: Thu, 09 Feb 2023 01:17:17 GMT  
		Size: 635.9 KB (635943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e120c0944228b4b6623b958c83433bc43f104b64cecccbd1ac7ab250e7a68db7`  
		Last Modified: Wed, 15 Feb 2023 20:17:30 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891cca6ce816bbe4dd40bd862cae84155f0da6f7f13ab15fb80f92c471772be7`  
		Last Modified: Wed, 15 Feb 2023 20:17:34 GMT  
		Size: 14.9 MB (14907106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e4718f6f1c46191ed75eaff08ff294c5ad0f384309aca914d5687324213f83`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0edcd24848e16049bee383e4ae89134f9d07da6079deed1398df66ad8a401ac`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b890b1c144cd00660796b630f5a2b8009a7c8b98a852cc4e645d13d84f4b48`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12054588e533ec29d2f174499ee24489e7b6d7b8527337dcdcc25a6ec29973`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e7efe9a5a718b562e89379f47cd1c2919b05c52ad1a2ceb9525d7f98f2f0d1`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fc39bc9c2bdee1444bb0e46b53cb55da0913be6b115f95bc50f5ed370138e`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d17482a1fa64018a51f2d8467fb3cba2c11aae5e67a689612e314d713ca8b0`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4843586865795ebb5e828c5f7fe6c9f829f9b12d5ad2e0bbf9f302874fc39a27`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd44712296ac1e7d28147c40159638788a75b58c17764de2757fcfda62f5551a`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5344aa95ac41ce0d03e95ae47d07c9ddef532b47bbfeb871053e69eacf5429a6`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf50f2a8532ee01e411b12116a827c2823a5cb2ee71091b4b724c44b6ba0f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b71f209c61027e4688f4e4b109ec883c187ed74b3d4c27e4b11596a4f20a07`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df052fc38d64efbb8657dd2c40cfa28c56f1137efcf1d7751277c1c81626b39e`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266955548153e827efba631ef21036116d523e11f332aae3910c4e6b773896f5`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59f15231c2a3b500e116b42a5254f441985197b1d364bc46a71cd917af38ec9`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 347.4 KB (347422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4a927a917a632a25082f22d95b2df35568f4522d622efe890c6d57457ed461`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:9b3fc2e9403b99a6fce9d5b94de587e848616342ccad9275d8bbead1a4b8f1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:371255c187169392f30d7caf1e65b8a8708afbdd8520eb74df9c38d973195766
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723380167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa79dce896513046be66642ea60c82eaf2266ff5533f3e8c40a79c7b779c0eca`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:16:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:15:47 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:17:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:17:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:17:11 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:17:12 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:17:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:17:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:17:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:17:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:17:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:17:20 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:17:21 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:17:22 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:17:24 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:17:43 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:17:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47af8a9c9ef8e49d65e53dd207ad0935ce7a2b50b2f253e6a5b037494ae19d0a`  
		Last Modified: Thu, 09 Feb 2023 01:16:50 GMT  
		Size: 401.5 KB (401472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d742cb3ca192278158c048ecc9f358855bc8f2629af70c62b9610a1fc66bbf0a`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859ce744a498d8f5affa0958dae6a0027cd48925c7c0bdf78214019c927eb34b`  
		Last Modified: Wed, 15 Feb 2023 20:17:06 GMT  
		Size: 14.7 MB (14694270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64525df3f764c2e65e711fbd328781c61243029c264aca6b09309e584dbb69b3`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231e1956368caba27b753959bf1fb5d38cf0e798477a45110f2691b063809554`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405677c240161263f0ca900ffca71596061f8d59668d524a80f16957c120f0c`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638a2e8fc9bd411f13b7b5a8b82272fd39024ac9b711d2bc73c28c39314fc3bb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1b8ca9045f120e19c22debd19df59f42aa442b84c073c7cfc2f5a2d0f463cb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c7468bd4bec28c11efd397d435df6a129ffc73265d2d2c4162bb121a336d08`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de41f5feb06b95a77601b9fd09ab7409b567e0d9684c46dfcdc4a067a00adc`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab6a97db0980bf9c94414bfb713b5db0ed7bec52a805303782c4309a6e9f62b`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41271d7026e5d15682fc59b1ac99ac0a67909c591ea0c7ab0885207386064744`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b605f7b22df792b7b41d97cec04cbfb795ba3588fd9e0b44363147a7a02820`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c2c11f6f75de707c6475d6248a27eb983282648b0a923c47e2894db7304e0d`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48461b499cb5763190c69d134f0b96625458bdd69fe78a15ade15efbad156033`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745ffdaac1ecada0622ef6d6ccfe6140992921240b91567821b96a07a72df8b8`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf9895ba16206d3ebb35a3a6e3f615542102d00230528158c62eee814428521`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc57c33625ddac815d78d81c0feb25f7dd3d6ea9f6d4f6238024e4898a15ef3c`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 316.4 KB (316447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31243cdae7d3d8bcf0b00d6c6c0a1f4ec3c2c277ca964f747f8acc133cef56a2`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:113f187a1100da96770eeaecc6e118b4be7ef33cb4d01611de3e3045ed3a4acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:0722e548c2efb29869e87e89dc7cf03de8d31fe33c28e9e61a33f018b0a7a3e4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1401943529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a230b066a2fbe8bdfee6749b8afe9b1655260bb3643408c49082c8754a4cff75`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:18:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:18:03 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:19:13 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:19:14 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:19:15 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:24 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:26 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:27 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:46 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:19:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42eb48143612ee855d99c932e324b1bd035c60554117edeaa805402060613c51`  
		Last Modified: Thu, 09 Feb 2023 01:17:17 GMT  
		Size: 635.9 KB (635943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e120c0944228b4b6623b958c83433bc43f104b64cecccbd1ac7ab250e7a68db7`  
		Last Modified: Wed, 15 Feb 2023 20:17:30 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891cca6ce816bbe4dd40bd862cae84155f0da6f7f13ab15fb80f92c471772be7`  
		Last Modified: Wed, 15 Feb 2023 20:17:34 GMT  
		Size: 14.9 MB (14907106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e4718f6f1c46191ed75eaff08ff294c5ad0f384309aca914d5687324213f83`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0edcd24848e16049bee383e4ae89134f9d07da6079deed1398df66ad8a401ac`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b890b1c144cd00660796b630f5a2b8009a7c8b98a852cc4e645d13d84f4b48`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12054588e533ec29d2f174499ee24489e7b6d7b8527337dcdcc25a6ec29973`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e7efe9a5a718b562e89379f47cd1c2919b05c52ad1a2ceb9525d7f98f2f0d1`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fc39bc9c2bdee1444bb0e46b53cb55da0913be6b115f95bc50f5ed370138e`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d17482a1fa64018a51f2d8467fb3cba2c11aae5e67a689612e314d713ca8b0`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4843586865795ebb5e828c5f7fe6c9f829f9b12d5ad2e0bbf9f302874fc39a27`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd44712296ac1e7d28147c40159638788a75b58c17764de2757fcfda62f5551a`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5344aa95ac41ce0d03e95ae47d07c9ddef532b47bbfeb871053e69eacf5429a6`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf50f2a8532ee01e411b12116a827c2823a5cb2ee71091b4b724c44b6ba0f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b71f209c61027e4688f4e4b109ec883c187ed74b3d4c27e4b11596a4f20a07`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df052fc38d64efbb8657dd2c40cfa28c56f1137efcf1d7751277c1c81626b39e`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266955548153e827efba631ef21036116d523e11f332aae3910c4e6b773896f5`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59f15231c2a3b500e116b42a5254f441985197b1d364bc46a71cd917af38ec9`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 347.4 KB (347422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4a927a917a632a25082f22d95b2df35568f4522d622efe890c6d57457ed461`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6`

```console
$ docker pull caddy@sha256:236163a87c5609986ce7ddead7d8aaf992314f031699ddde2a400597640965e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.3887; amd64
	-	windows version 10.0.20348.1487; amd64

### `caddy:2.6` - linux; amd64

```console
$ docker pull caddy@sha256:36ba71b44afa613ecf0aadce8e4b9e3f56e0c4b0a78c8edf4e8c2485f21b35ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17449113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8464e23f16f9a82426bbdc3ac8c94270a84453ddc86b9147505a2378a7c2fd0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:38:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 11 Feb 2023 07:38:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 19:19:21 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 19:19:23 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 19:19:24 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:25 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 19:19:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e3e797818bc929d95bae8220b7b6034b559c217ef5bf622dc7fedc8d270a48`  
		Last Modified: Sat, 11 Feb 2023 07:39:01 GMT  
		Size: 351.2 KB (351178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cebb4c80b3906a9b751ee9a512c1581331b1fd691c84f575c01a29e28403dde`  
		Last Modified: Sat, 11 Feb 2023 07:39:00 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90648ba22c191b969d8db393bf6138e7d6ecc1b70b3865d1717ec4d663192d89`  
		Last Modified: Wed, 15 Feb 2023 19:19:52 GMT  
		Size: 14.3 MB (14282621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5b39c4c37396031351c9753e4c7df6f2114d0ef588953b97c668d0ec7e2f1e50
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16582274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ffa8388ed5f7f62ab116b850faa63ff3214dea5fb007a77196a8efd0023832`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:28:54 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 21:28:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:49:22 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:49:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:49:26 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:49:26 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:49:27 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:49:28 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:49:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a400dcba29ff44f8e5bf01493def4f19629aca6d103cb2a66ca87c457f7414`  
		Last Modified: Fri, 10 Feb 2023 21:29:47 GMT  
		Size: 345.8 KB (345811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b946768825eb5ed2fc6f932fdb0b0c552f4c35c39dada07eddd70ce4a535953`  
		Last Modified: Fri, 10 Feb 2023 21:29:47 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f11ff5bb8d752ef2e91afa46770077fd62ddc9e78f280c00e796bf841c9d49f`  
		Last Modified: Wed, 15 Feb 2023 18:50:25 GMT  
		Size: 13.6 MB (13612205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6` - linux; arm variant v7

```console
$ docker pull caddy@sha256:21302c9acb44ea61fccba3ef765712da93fede2d928aaafc8f7bd77a35d91953
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16365562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600d5193b2ba5875b66a6579717ec1aab50be117445a5a657045572141d1187c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:37 GMT
ADD file:193f48d48ed2e90a0e81663757e372f59806151c17e82113f03443db0ef723c3 in / 
# Fri, 10 Feb 2023 21:51:37 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:37:19 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:37:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:57:27 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:57:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:57:30 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:57:30 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:57:31 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:57:32 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:beefe5ad637c7db32e6afc68103fc4e779630219979216a625338ab55f7d191c`  
		Last Modified: Fri, 10 Feb 2023 21:52:51 GMT  
		Size: 2.4 MB (2420494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2ab4edb1f0a14b28a55f050d62d8e54111075639a0fa8f173448814ba0d00`  
		Last Modified: Fri, 10 Feb 2023 22:38:25 GMT  
		Size: 342.6 KB (342588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0580184dd0082f009564a7a3923731f202cbe4bd8b857dbca2c77da8e7434815`  
		Last Modified: Fri, 10 Feb 2023 22:38:25 GMT  
		Size: 7.5 KB (7479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8682e09bc231d5c9076b76cb92cb3b1185b870277da03dbd7e87d7981ff6147a`  
		Last Modified: Wed, 15 Feb 2023 18:58:28 GMT  
		Size: 13.6 MB (13595001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:6c2623f6bf30798be5c37fc7484e45ecc288d493fb657883f59ddb27ed714ad8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16130997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a38afdc517ef4cff6b6b51a1c6a633c2826599b07feb1e88380d0f783e35cf1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:00:35 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:00:37 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:39:20 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:39:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:39:22 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:39:22 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:39:23 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:39:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70730e8e2fb933ec157ec87f2a4fb4ad45e8e578b8f7c76cc4846631d773554`  
		Last Modified: Fri, 10 Feb 2023 22:01:02 GMT  
		Size: 350.2 KB (350153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a4b7390d269477c225f1d03e825d2d8bdf6b4d87b5f7bb8811b341e56b7d36`  
		Last Modified: Fri, 10 Feb 2023 22:01:02 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2743d2ef53ee6edb0e39c89bf16957e3a00990410b2d1a126dca1b2d196182`  
		Last Modified: Wed, 15 Feb 2023 18:39:53 GMT  
		Size: 13.1 MB (13063787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6` - linux; ppc64le

```console
$ docker pull caddy@sha256:8861ab3ae3d0c180e38142c2f7482f9ce1773419eb29ed9d6d18308246858093
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15955172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5819f0ab4928a30c29293a27299a3b44371cd3bd97df91432ef7b3f43b692d8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:13:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:13:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 19:16:26 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:16:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 19:16:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 19:16:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 19:16:42 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:16:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:16:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:16:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:16:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:16:47 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:16:47 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 19:16:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782bd0321e6539bb7dac8574fd36bad22059ef06bb63dc842165f69d0a821572`  
		Last Modified: Fri, 10 Feb 2023 22:14:16 GMT  
		Size: 363.1 KB (363088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb806b2600b0209a73fc7175ab778d0224661034b2f722bd1a0aec1eb9eabe3d`  
		Last Modified: Fri, 10 Feb 2023 22:14:15 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd7c8ae860931dd79dea76d33bc21bb11d89cd4d133cdb41078b040afc6633e`  
		Last Modified: Wed, 15 Feb 2023 19:17:41 GMT  
		Size: 12.8 MB (12779898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6` - linux; s390x

```console
$ docker pull caddy@sha256:4e1ed99f133abf02d6a7c77849978bb621f748e18c9cb9f7a1dbf88480ddb8d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16792756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45cd164da734310b788dcbd4f6c94bccff6e48705fe4d42ecca07a54e9459a9c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:14:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:41:48 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:41:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:41:59 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:41:59 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:42:00 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:42:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:42:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:42:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:42:03 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:42:04 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:42:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:42:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:42:05 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:42:06 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:42:07 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:42:07 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:42:08 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:42:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e6ec82400496ce74e37120e1655955b79303daaa5b8ca7e956e3cd96ddd6e9`  
		Last Modified: Fri, 10 Feb 2023 22:15:05 GMT  
		Size: 352.8 KB (352801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5b992687f93ced3715ad97bd95ab37daef5685b784e195209caefbc48f14e9`  
		Last Modified: Fri, 10 Feb 2023 22:15:05 GMT  
		Size: 7.6 KB (7557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccc40924ce2df3343fa5465a92ccaa4ed80e0883190a99d3f468c60f9ddbcf8`  
		Last Modified: Wed, 15 Feb 2023 18:43:19 GMT  
		Size: 13.8 MB (13838817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:371255c187169392f30d7caf1e65b8a8708afbdd8520eb74df9c38d973195766
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723380167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa79dce896513046be66642ea60c82eaf2266ff5533f3e8c40a79c7b779c0eca`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:16:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:15:47 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:17:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:17:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:17:11 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:17:12 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:17:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:17:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:17:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:17:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:17:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:17:20 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:17:21 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:17:22 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:17:24 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:17:43 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:17:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47af8a9c9ef8e49d65e53dd207ad0935ce7a2b50b2f253e6a5b037494ae19d0a`  
		Last Modified: Thu, 09 Feb 2023 01:16:50 GMT  
		Size: 401.5 KB (401472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d742cb3ca192278158c048ecc9f358855bc8f2629af70c62b9610a1fc66bbf0a`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859ce744a498d8f5affa0958dae6a0027cd48925c7c0bdf78214019c927eb34b`  
		Last Modified: Wed, 15 Feb 2023 20:17:06 GMT  
		Size: 14.7 MB (14694270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64525df3f764c2e65e711fbd328781c61243029c264aca6b09309e584dbb69b3`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231e1956368caba27b753959bf1fb5d38cf0e798477a45110f2691b063809554`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405677c240161263f0ca900ffca71596061f8d59668d524a80f16957c120f0c`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638a2e8fc9bd411f13b7b5a8b82272fd39024ac9b711d2bc73c28c39314fc3bb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1b8ca9045f120e19c22debd19df59f42aa442b84c073c7cfc2f5a2d0f463cb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c7468bd4bec28c11efd397d435df6a129ffc73265d2d2c4162bb121a336d08`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de41f5feb06b95a77601b9fd09ab7409b567e0d9684c46dfcdc4a067a00adc`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab6a97db0980bf9c94414bfb713b5db0ed7bec52a805303782c4309a6e9f62b`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41271d7026e5d15682fc59b1ac99ac0a67909c591ea0c7ab0885207386064744`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b605f7b22df792b7b41d97cec04cbfb795ba3588fd9e0b44363147a7a02820`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c2c11f6f75de707c6475d6248a27eb983282648b0a923c47e2894db7304e0d`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48461b499cb5763190c69d134f0b96625458bdd69fe78a15ade15efbad156033`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745ffdaac1ecada0622ef6d6ccfe6140992921240b91567821b96a07a72df8b8`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf9895ba16206d3ebb35a3a6e3f615542102d00230528158c62eee814428521`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc57c33625ddac815d78d81c0feb25f7dd3d6ea9f6d4f6238024e4898a15ef3c`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 316.4 KB (316447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31243cdae7d3d8bcf0b00d6c6c0a1f4ec3c2c277ca964f747f8acc133cef56a2`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:0722e548c2efb29869e87e89dc7cf03de8d31fe33c28e9e61a33f018b0a7a3e4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1401943529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a230b066a2fbe8bdfee6749b8afe9b1655260bb3643408c49082c8754a4cff75`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:18:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:18:03 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:19:13 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:19:14 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:19:15 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:24 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:26 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:27 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:46 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:19:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42eb48143612ee855d99c932e324b1bd035c60554117edeaa805402060613c51`  
		Last Modified: Thu, 09 Feb 2023 01:17:17 GMT  
		Size: 635.9 KB (635943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e120c0944228b4b6623b958c83433bc43f104b64cecccbd1ac7ab250e7a68db7`  
		Last Modified: Wed, 15 Feb 2023 20:17:30 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891cca6ce816bbe4dd40bd862cae84155f0da6f7f13ab15fb80f92c471772be7`  
		Last Modified: Wed, 15 Feb 2023 20:17:34 GMT  
		Size: 14.9 MB (14907106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e4718f6f1c46191ed75eaff08ff294c5ad0f384309aca914d5687324213f83`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0edcd24848e16049bee383e4ae89134f9d07da6079deed1398df66ad8a401ac`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b890b1c144cd00660796b630f5a2b8009a7c8b98a852cc4e645d13d84f4b48`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12054588e533ec29d2f174499ee24489e7b6d7b8527337dcdcc25a6ec29973`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e7efe9a5a718b562e89379f47cd1c2919b05c52ad1a2ceb9525d7f98f2f0d1`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fc39bc9c2bdee1444bb0e46b53cb55da0913be6b115f95bc50f5ed370138e`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d17482a1fa64018a51f2d8467fb3cba2c11aae5e67a689612e314d713ca8b0`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4843586865795ebb5e828c5f7fe6c9f829f9b12d5ad2e0bbf9f302874fc39a27`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd44712296ac1e7d28147c40159638788a75b58c17764de2757fcfda62f5551a`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5344aa95ac41ce0d03e95ae47d07c9ddef532b47bbfeb871053e69eacf5429a6`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf50f2a8532ee01e411b12116a827c2823a5cb2ee71091b4b724c44b6ba0f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b71f209c61027e4688f4e4b109ec883c187ed74b3d4c27e4b11596a4f20a07`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df052fc38d64efbb8657dd2c40cfa28c56f1137efcf1d7751277c1c81626b39e`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266955548153e827efba631ef21036116d523e11f332aae3910c4e6b773896f5`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59f15231c2a3b500e116b42a5254f441985197b1d364bc46a71cd917af38ec9`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 347.4 KB (347422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4a927a917a632a25082f22d95b2df35568f4522d622efe890c6d57457ed461`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6-alpine`

```console
$ docker pull caddy@sha256:aacae65cfdcf61777306cf7c131fb968f67bb7fab8dfd683aa073e8b99867e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.6-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:36ba71b44afa613ecf0aadce8e4b9e3f56e0c4b0a78c8edf4e8c2485f21b35ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17449113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8464e23f16f9a82426bbdc3ac8c94270a84453ddc86b9147505a2378a7c2fd0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:38:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 11 Feb 2023 07:38:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 19:19:21 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 19:19:23 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 19:19:24 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:25 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 19:19:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e3e797818bc929d95bae8220b7b6034b559c217ef5bf622dc7fedc8d270a48`  
		Last Modified: Sat, 11 Feb 2023 07:39:01 GMT  
		Size: 351.2 KB (351178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cebb4c80b3906a9b751ee9a512c1581331b1fd691c84f575c01a29e28403dde`  
		Last Modified: Sat, 11 Feb 2023 07:39:00 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90648ba22c191b969d8db393bf6138e7d6ecc1b70b3865d1717ec4d663192d89`  
		Last Modified: Wed, 15 Feb 2023 19:19:52 GMT  
		Size: 14.3 MB (14282621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5b39c4c37396031351c9753e4c7df6f2114d0ef588953b97c668d0ec7e2f1e50
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16582274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ffa8388ed5f7f62ab116b850faa63ff3214dea5fb007a77196a8efd0023832`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:28:54 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 21:28:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:49:22 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:49:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:49:26 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:49:26 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:49:27 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:49:28 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:49:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a400dcba29ff44f8e5bf01493def4f19629aca6d103cb2a66ca87c457f7414`  
		Last Modified: Fri, 10 Feb 2023 21:29:47 GMT  
		Size: 345.8 KB (345811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b946768825eb5ed2fc6f932fdb0b0c552f4c35c39dada07eddd70ce4a535953`  
		Last Modified: Fri, 10 Feb 2023 21:29:47 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f11ff5bb8d752ef2e91afa46770077fd62ddc9e78f280c00e796bf841c9d49f`  
		Last Modified: Wed, 15 Feb 2023 18:50:25 GMT  
		Size: 13.6 MB (13612205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:21302c9acb44ea61fccba3ef765712da93fede2d928aaafc8f7bd77a35d91953
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16365562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600d5193b2ba5875b66a6579717ec1aab50be117445a5a657045572141d1187c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:37 GMT
ADD file:193f48d48ed2e90a0e81663757e372f59806151c17e82113f03443db0ef723c3 in / 
# Fri, 10 Feb 2023 21:51:37 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:37:19 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:37:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:57:27 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:57:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:57:30 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:57:30 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:57:31 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:57:32 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:beefe5ad637c7db32e6afc68103fc4e779630219979216a625338ab55f7d191c`  
		Last Modified: Fri, 10 Feb 2023 21:52:51 GMT  
		Size: 2.4 MB (2420494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2ab4edb1f0a14b28a55f050d62d8e54111075639a0fa8f173448814ba0d00`  
		Last Modified: Fri, 10 Feb 2023 22:38:25 GMT  
		Size: 342.6 KB (342588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0580184dd0082f009564a7a3923731f202cbe4bd8b857dbca2c77da8e7434815`  
		Last Modified: Fri, 10 Feb 2023 22:38:25 GMT  
		Size: 7.5 KB (7479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8682e09bc231d5c9076b76cb92cb3b1185b870277da03dbd7e87d7981ff6147a`  
		Last Modified: Wed, 15 Feb 2023 18:58:28 GMT  
		Size: 13.6 MB (13595001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:6c2623f6bf30798be5c37fc7484e45ecc288d493fb657883f59ddb27ed714ad8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16130997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a38afdc517ef4cff6b6b51a1c6a633c2826599b07feb1e88380d0f783e35cf1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:00:35 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:00:37 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:39:20 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:39:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:39:22 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:39:22 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:39:23 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:39:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70730e8e2fb933ec157ec87f2a4fb4ad45e8e578b8f7c76cc4846631d773554`  
		Last Modified: Fri, 10 Feb 2023 22:01:02 GMT  
		Size: 350.2 KB (350153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a4b7390d269477c225f1d03e825d2d8bdf6b4d87b5f7bb8811b341e56b7d36`  
		Last Modified: Fri, 10 Feb 2023 22:01:02 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2743d2ef53ee6edb0e39c89bf16957e3a00990410b2d1a126dca1b2d196182`  
		Last Modified: Wed, 15 Feb 2023 18:39:53 GMT  
		Size: 13.1 MB (13063787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:8861ab3ae3d0c180e38142c2f7482f9ce1773419eb29ed9d6d18308246858093
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15955172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5819f0ab4928a30c29293a27299a3b44371cd3bd97df91432ef7b3f43b692d8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:13:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:13:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 19:16:26 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:16:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 19:16:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 19:16:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 19:16:42 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:16:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:16:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:16:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:16:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:16:47 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:16:47 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 19:16:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782bd0321e6539bb7dac8574fd36bad22059ef06bb63dc842165f69d0a821572`  
		Last Modified: Fri, 10 Feb 2023 22:14:16 GMT  
		Size: 363.1 KB (363088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb806b2600b0209a73fc7175ab778d0224661034b2f722bd1a0aec1eb9eabe3d`  
		Last Modified: Fri, 10 Feb 2023 22:14:15 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd7c8ae860931dd79dea76d33bc21bb11d89cd4d133cdb41078b040afc6633e`  
		Last Modified: Wed, 15 Feb 2023 19:17:41 GMT  
		Size: 12.8 MB (12779898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:4e1ed99f133abf02d6a7c77849978bb621f748e18c9cb9f7a1dbf88480ddb8d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16792756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45cd164da734310b788dcbd4f6c94bccff6e48705fe4d42ecca07a54e9459a9c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:14:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:41:48 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:41:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:41:59 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:41:59 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:42:00 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:42:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:42:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:42:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:42:03 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:42:04 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:42:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:42:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:42:05 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:42:06 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:42:07 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:42:07 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:42:08 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:42:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e6ec82400496ce74e37120e1655955b79303daaa5b8ca7e956e3cd96ddd6e9`  
		Last Modified: Fri, 10 Feb 2023 22:15:05 GMT  
		Size: 352.8 KB (352801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5b992687f93ced3715ad97bd95ab37daef5685b784e195209caefbc48f14e9`  
		Last Modified: Fri, 10 Feb 2023 22:15:05 GMT  
		Size: 7.6 KB (7557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccc40924ce2df3343fa5465a92ccaa4ed80e0883190a99d3f468c60f9ddbcf8`  
		Last Modified: Wed, 15 Feb 2023 18:43:19 GMT  
		Size: 13.8 MB (13838817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6-builder`

```console
$ docker pull caddy@sha256:f3ac019c2a9615cd1adc2555d81ba8eb0412bfea8c34290fc0adfc7d77a468e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.3887; amd64
	-	windows version 10.0.20348.1487; amd64

### `caddy:2.6-builder` - linux; amd64

```console
$ docker pull caddy@sha256:47722ffc694507be1e2f34ca172e292fb5e226ea68d87871300b9d65f543fcce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131421587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4674ac67a52f4d29bc8349e9dcca7db8393d778c97c79d9e2f6e997603a99cd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 08:21:54 GMT
RUN apk add --no-cache ca-certificates
# Sat, 11 Feb 2023 08:21:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:24:10 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:25:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:25:43 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:25:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:25:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:25:44 GMT
WORKDIR /go
# Tue, 14 Feb 2023 19:47:10 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 19:47:10 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:19:27 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:19:28 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 19:19:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 19:19:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 19:19:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d21d5440ebff5aaaaeb115a003f7a4a3897f1866a87de95bc4a21436fc563c`  
		Last Modified: Sat, 11 Feb 2023 08:29:10 GMT  
		Size: 284.8 KB (284816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f790f4c5274f100158d4c23bc5eddf659c1fe93ef4025488f9493d88f1490d88`  
		Last Modified: Tue, 14 Feb 2023 19:31:12 GMT  
		Size: 122.4 MB (122355677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bf170fd9e6726c86c0d4b478d9ec522e82c527a8e708668f48233a4d03f618`  
		Last Modified: Tue, 14 Feb 2023 19:30:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a5d1c1b6ed103f8c7f97c73ed546ff7e767b10473b55c15c0d4e1a13a69481`  
		Last Modified: Tue, 14 Feb 2023 19:47:34 GMT  
		Size: 4.2 MB (4188243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0130eaa2f0b1f7646719d82927743bd84c83ed450eb8be4db5327d280d5e4d0`  
		Last Modified: Wed, 15 Feb 2023 19:20:05 GMT  
		Size: 1.2 MB (1217841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab1f57409241476a86d26944527bc2c6c3903eadb21221b8d96da52120b3109`  
		Last Modified: Wed, 15 Feb 2023 19:20:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ef43980c42cd8a35929f0378a7ecd1918acd54140264da387b01dc7e3d6bea0b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127437368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd812dbbfb10d2a70518b9169ed3ed8f3e00b43a8b7ce2f98f7e72b09d33330`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:49:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 21:49:23 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:54:56 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:57:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:57:12 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:57:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:57:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:57:13 GMT
WORKDIR /go
# Tue, 14 Feb 2023 21:22:55 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 21:22:55 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:49:33 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:49:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:49:33 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:49:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:49:35 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:49:35 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11114cba5e5d7175bb4d5b434db94e1c2bf0f8263c6cf2b8cbf3c1fc853114b5`  
		Last Modified: Fri, 10 Feb 2023 22:00:04 GMT  
		Size: 286.1 KB (286119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbe98122be79c40d67ce24806b19f5bd6a2f3025a18faa3a9e07c836eda77a3`  
		Last Modified: Tue, 14 Feb 2023 20:03:20 GMT  
		Size: 118.7 MB (118722534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2006a6001995de26a92cbdcc7917c763ee43c1f153331e17ed59bc706622a4`  
		Last Modified: Tue, 14 Feb 2023 20:02:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241e307a6c2a59713b29a4001892e4737b03b8bdc797f283f8bfef8e5976a360`  
		Last Modified: Tue, 14 Feb 2023 21:23:46 GMT  
		Size: 4.2 MB (4151224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd6d861ad1e103851af9cad05cca9ddd82af819c16eef77a788212eb48a451a`  
		Last Modified: Wed, 15 Feb 2023 18:50:44 GMT  
		Size: 1.2 MB (1166072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff6cca8082ff38bb36e60b71883dc986b05c54b1322ffe5c5906933155af3db`  
		Last Modified: Wed, 15 Feb 2023 18:50:44 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ae944139e672dc9c4065b2e83f98a2c2522db0397a33f3b287e771e01c90b043
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126518789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b5e54b6cc5a620df577f3659a5f2415b1ab88786c0ee932fd73c5c026786cb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 23:34:00 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 23:34:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 22:43:55 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 22:46:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 22:46:04 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 22:46:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 22:46:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 22:46:05 GMT
WORKDIR /go
# Wed, 15 Feb 2023 01:37:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 15 Feb 2023 01:37:44 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:57:37 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:57:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:57:37 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:57:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:57:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ee22df4e0527c9d317c1729808b4fc333083ad4d5a41645d79beabb64e9415`  
		Last Modified: Fri, 10 Feb 2023 23:50:08 GMT  
		Size: 285.4 KB (285353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0083f2e9af62d9a5b5bcf25401158f3ebb34f9fe9e7e951a52b22e9f6a15f1ed`  
		Last Modified: Tue, 14 Feb 2023 22:54:26 GMT  
		Size: 118.5 MB (118480449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6506d85184bedd4e64bb66e1357511d9dde4bc32c2c99d3183c2cec84f20e7e5`  
		Last Modified: Tue, 14 Feb 2023 22:54:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc4386697a4bb55f0e63b324c4a0b444eec215aff0cffc35d7affc50fff2041`  
		Last Modified: Wed, 15 Feb 2023 01:38:34 GMT  
		Size: 3.7 MB (3720630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03d748e87e34207a999297a575c405a0c36bf6b02a35f1c1b370ae25d1daf26`  
		Last Modified: Wed, 15 Feb 2023 18:58:45 GMT  
		Size: 1.2 MB (1163331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957e61fda37fb7df272efba4e6f8cd0083db173bff77b1e4dbbfad3fba3cd92b`  
		Last Modified: Wed, 15 Feb 2023 18:58:44 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:345963f3560e208ac6bacd024a578f5b7e01f8b734c723eddee3617aa9f0eb48
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125824793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e4189a65557b7e2dd531761f337fa9ebac950fe19c378297b031b64ef548d7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:38:33 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:38:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:43:03 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:44:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:44:06 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:44:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:44:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:44:07 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:05:45 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:05:45 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:39:25 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:39:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:39:26 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:39:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:39:28 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:39:28 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55522c79112429742fe76c795b9509c5cd1e8198e0caa2a1e355c0e60a719576`  
		Last Modified: Fri, 10 Feb 2023 22:44:19 GMT  
		Size: 286.3 KB (286257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a025c151a25ec079b20475bc7d9114a55273ff4768db3589c2a9e3556263ff`  
		Last Modified: Tue, 14 Feb 2023 19:48:57 GMT  
		Size: 116.9 MB (116917630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e172ed32e80e014974dc5c64a3cec7ac2d456fe4b21179f48138df590112cdab`  
		Last Modified: Tue, 14 Feb 2023 19:48:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbab95e946333dfac53de76b5f4cfc1f90fec80107055af4eb888824c147950`  
		Last Modified: Tue, 14 Feb 2023 20:06:09 GMT  
		Size: 4.2 MB (4234639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52ae4d010a784b362566e543eeacafbef900440cdda0b182dc5ea51a53b070c`  
		Last Modified: Wed, 15 Feb 2023 18:40:08 GMT  
		Size: 1.1 MB (1123743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d9033ce04f11b49957c7855096c7e5ed4a4e3ad840dd150fc0823b230b3742`  
		Last Modified: Wed, 15 Feb 2023 18:40:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:8126a0d2b7cc9613f70b6b5375c14cc61dfca5dc1b83adc5be33efab8eacc69f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126579575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da1cd24f35f4106a8a7176a2f2b5656a22982a1787b9204d3eaab9ec535ef58`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:36 GMT
ADD file:ec037a0d4b462d12963ac20d9ec49bb73b4bcaf84d4bc7b364ebf93667e585b0 in / 
# Fri, 10 Feb 2023 21:20:36 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:40:13 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:40:14 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:46:09 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:48:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:48:44 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:48:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:48:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:48:46 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:12:48 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:12:48 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:16:53 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:16:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:16:54 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 19:16:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 19:16:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 19:16:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:aa3c56f9c6f127b6c8f628c95db165741ca400d19bdaef2752d80f093e47451e`  
		Last Modified: Fri, 10 Feb 2023 21:21:37 GMT  
		Size: 3.4 MB (3390750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788962e1689dbb14c760601cbf633ae350e98e3a045f8010924cd585de6b6a3e`  
		Last Modified: Fri, 10 Feb 2023 22:53:32 GMT  
		Size: 286.6 KB (286645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ae39b9ad00c218f9156f0958fa48f3062eb5830b791b8592e5f25fd576c7c5`  
		Last Modified: Tue, 14 Feb 2023 19:56:18 GMT  
		Size: 117.3 MB (117316160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f3bf55d586b31bb5c97f2cbf5167fd359b61336f93bed839c2f4de055ced88`  
		Last Modified: Tue, 14 Feb 2023 19:55:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e012d53123423a5fe128ab31d41596d83d8e48699ad608e9eb58dd0b2322fe0`  
		Last Modified: Tue, 14 Feb 2023 20:13:35 GMT  
		Size: 4.5 MB (4479556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90177e6cf58218f094608b8401f41d0da78a0cf57d95718e48e8c6e2f77c6fae`  
		Last Modified: Wed, 15 Feb 2023 19:18:00 GMT  
		Size: 1.1 MB (1105899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e897949e5a46b09b4606d86b20ecb5684cb43f7e1bed1f208ee9b7e93d208c`  
		Last Modified: Wed, 15 Feb 2023 19:17:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-builder` - linux; s390x

```console
$ docker pull caddy@sha256:777aec044ded48957652f0c6ceac314892e1c892c85a07084f80762791aa55b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129606877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4f36416ff115d90097fe1378fca1a1ded179a50ee13701194f1193833e1d5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:25 GMT
ADD file:03b2fb4d732a294329449ff55c5d84f7d2735e6510985718979469994f3a607b in / 
# Fri, 10 Feb 2023 21:41:26 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:27:44 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:27:44 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:47:34 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:49:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:49:23 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:49:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:49:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:49:24 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:12:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:12:32 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:42:20 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:42:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:42:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:42:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:42:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:42:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:24c4f8de3549a39c64b0edc2cfa68769b373f35138d0f13725100160bb32d4e2`  
		Last Modified: Fri, 10 Feb 2023 21:42:16 GMT  
		Size: 3.2 MB (3175116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affa53ed2f1b70a83e3a15cae881ca47cd40f6ac11060717cdbbd4e405f9d586`  
		Last Modified: Fri, 10 Feb 2023 22:37:18 GMT  
		Size: 285.0 KB (285032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafa18be4ff892e2222424e6e25c36c21c4d94825607e8b840d2384c6ab73651`  
		Last Modified: Tue, 14 Feb 2023 19:54:27 GMT  
		Size: 120.8 MB (120811850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c3965c085d018b012055d834e6c56402c39a086413f83eb42fed0eba26be6`  
		Last Modified: Tue, 14 Feb 2023 19:54:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250c53f2b7534f15112393341635149f8ad756241a7c7979ec7ad6fbd3959ff1`  
		Last Modified: Tue, 14 Feb 2023 20:13:22 GMT  
		Size: 4.2 MB (4163882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11288ef421d5fc2fc1e1a7cd7350fb7f4ad371aa6edad42bb5ffa8f95cb2f2bc`  
		Last Modified: Wed, 15 Feb 2023 18:43:31 GMT  
		Size: 1.2 MB (1170432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b792196575b477b3bd73841238a0c4445026bc982b5e0236ef24a59eec4875`  
		Last Modified: Wed, 15 Feb 2023 18:43:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-builder` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:bff20886c4e50c2ff56c65ce2b8b2f6f861b63544087ebc9828b8283abf3e9ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1893205034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9666c08cd03c61fe14a234d3f8760533430f35e891dccd0f5540cb34fd9834a4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 03:01:55 GMT
ENV GIT_VERSION=2.23.0
# Thu, 12 Jan 2023 03:01:56 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 12 Jan 2023 03:01:57 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 12 Jan 2023 03:01:58 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 12 Jan 2023 03:02:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 03:03:01 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 03:03:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Feb 2023 20:35:10 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 20:39:32 GMT
RUN $url = 'https://dl.google.com/go/go1.19.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8d84af29e46c38b1eec77f9310310517c9e394ac7489e1c7329a94b443b0388d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Feb 2023 20:39:34 GMT
WORKDIR C:\go
# Tue, 14 Feb 2023 21:16:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 21:16:10 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:20:04 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:20:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Feb 2023 19:20:39 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203425975bec1802428fad91a2e5f01172b161062c12eddf729e548bf7e134e0`  
		Last Modified: Thu, 12 Jan 2023 03:48:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80e42e19ab862b4adea06f1995e1f5cbb2c11ad8d68ae4a7bb5d0da5d0e6f38`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be5d5df8cec6d1386f78a342668c3d2cb809372865459c1b35aa8d5a39a463b`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e467d553c4972b55bf8e3d80b16f245e5bb38f28d80b91ca4f9f90c09a6c28d`  
		Last Modified: Thu, 12 Jan 2023 03:48:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97054b77b205167acd5a303c8aa82e380f090ff4e2ded81d3425ec78500139d`  
		Last Modified: Thu, 12 Jan 2023 03:48:14 GMT  
		Size: 25.5 MB (25470784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e150d9e1a1da09e17313cb3b6358d2f16cf2919c51e9addf30500de9d03292ef`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c0d792e2a7942826a61fdc26b6081ab404122751ff4f4dd8f5b8b0eca21399`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 324.5 KB (324466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd89ac843c0479ae40ca8c747e8a676229754549dbfeb9fe7157fdf1a60e685f`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0892c7d4de38540a99ca06e09c0a995b2e119c5ae853eadc2f7558f69bf44bb1`  
		Last Modified: Tue, 14 Feb 2023 20:56:57 GMT  
		Size: 157.8 MB (157805981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b2ec2bef689e3f934369ec3ebb90a5b06c0cbd77b2364e23a776b4da7a68f5`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066daab446064e42a798fe1592cbb9befd18dc7c368cc287f403168c17647f44`  
		Last Modified: Tue, 14 Feb 2023 21:18:46 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ea7fb211a6a6bdf1db9842354942dfaf3dc66bb87b9ce2b1620b897655022d`  
		Last Modified: Tue, 14 Feb 2023 21:18:44 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1a9f71a17b653aeea9897c2da8205709b77073460fc648f6daa323ffffee8d`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53678f100709f21522f2dd0732c10bbb5a70107fa9a4fcdd4895786c68d0bb27`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a973e4e836b19e1ccb3104f7458b2ed9a0aee58d697b6b7a8f7b8800265560f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:53 GMT  
		Size: 1.6 MB (1641852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9b2ad53ca032d7a1d8ef1944923a40be2d6c2fbd4945695a1d7cf5ea708613`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-builder` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:8208748738c8ad71587dbe2fa710487d6ed5a1ef462b3591e30be906145cab13
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1572172924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c99c2ba8e5059d5dc3ad70afada06d399bff99be54c4c7bf3908b0889a8719a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 02:57:40 GMT
ENV GIT_VERSION=2.23.0
# Thu, 12 Jan 2023 02:57:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 12 Jan 2023 02:57:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 12 Jan 2023 02:57:42 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 12 Jan 2023 02:58:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 02:58:23 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 02:58:47 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Feb 2023 20:31:21 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 20:34:49 GMT
RUN $url = 'https://dl.google.com/go/go1.19.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8d84af29e46c38b1eec77f9310310517c9e394ac7489e1c7329a94b443b0388d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Feb 2023 20:34:51 GMT
WORKDIR C:\go
# Tue, 14 Feb 2023 21:17:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 21:17:18 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:20:52 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:20:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:21:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Feb 2023 19:21:22 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2fc8728d9c7bf65edf893fd902f8b1bd780f93623858960c9db79e39922b169`  
		Last Modified: Thu, 12 Jan 2023 03:47:24 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7935a4c648078e79f67a11bcd5908e251110dd6c5a4ee49a607f332dd25af9`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d257f8b122044547f89f00f58661b25aca97c92f3831e7aaa11975639b6e35d4`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95acaa75c1852ba1320c5db382b01f587badb615b6746b59be27eedcf96ab667`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5201ba65043fa621c187729f18aecf4c549cdfa12cd6d8cab7a901d893f3a8a8`  
		Last Modified: Thu, 12 Jan 2023 03:47:29 GMT  
		Size: 25.7 MB (25702230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a317a349bca5ab28ba7c1ce039928a56390f7e7a8d7ddec07efcc1c9883e5d`  
		Last Modified: Thu, 12 Jan 2023 03:47:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8850296b8fbb853a6eb6341f7484cd4bc622e9f679f12c4123eddf08b7f398fb`  
		Last Modified: Thu, 12 Jan 2023 03:47:18 GMT  
		Size: 554.2 KB (554212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b724dc103b7bd177436e0035a2c0eaffd1187dcb978222f4e7c1014ca50ee`  
		Last Modified: Tue, 14 Feb 2023 20:55:01 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f4ea18edcbbc3120e8b270d76ae1a1876db9d493e1b703d25194e08b0896c`  
		Last Modified: Tue, 14 Feb 2023 20:55:55 GMT  
		Size: 158.0 MB (158000355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81da76ff355cb5fcac2247f23ca1fe8dd4256b41f2edd58b34f886fcb74bc6e7`  
		Last Modified: Tue, 14 Feb 2023 20:55:01 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc05ca820f63f78de074bd0a9ffe6889c8e3405b0563cf21ef5013179b8f407`  
		Last Modified: Tue, 14 Feb 2023 21:19:03 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b911bfee9062064c2f989b2acf01493bb3c9ad5989eb456277dfe272c1dcd2`  
		Last Modified: Tue, 14 Feb 2023 21:19:01 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aa3117c7e54c9d38a6d368beb815482c58bd46981294fc7c45046ca02b8d34`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710d1b3e32dd905f2dc2f33df9481f9abdd52cbd0028eadd5d0517fe673c3de1`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df812b30f4c795624a0ff09a18f3ac73987de268d9ee1aa080998e222a6f6e3`  
		Last Modified: Wed, 15 Feb 2023 20:18:10 GMT  
		Size: 1.9 MB (1868549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced4b40932769c58cc0b5348fdc7b4189892820c655d4029b988aafd8692dcd0`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6-builder-alpine`

```console
$ docker pull caddy@sha256:ef81823d12a3d4befb8d3dc29929c37f003682cc6a9cc8a7e8ed08442fc2644a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.6-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:47722ffc694507be1e2f34ca172e292fb5e226ea68d87871300b9d65f543fcce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131421587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4674ac67a52f4d29bc8349e9dcca7db8393d778c97c79d9e2f6e997603a99cd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 08:21:54 GMT
RUN apk add --no-cache ca-certificates
# Sat, 11 Feb 2023 08:21:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:24:10 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:25:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:25:43 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:25:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:25:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:25:44 GMT
WORKDIR /go
# Tue, 14 Feb 2023 19:47:10 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 19:47:10 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:19:27 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:19:28 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 19:19:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 19:19:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 19:19:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d21d5440ebff5aaaaeb115a003f7a4a3897f1866a87de95bc4a21436fc563c`  
		Last Modified: Sat, 11 Feb 2023 08:29:10 GMT  
		Size: 284.8 KB (284816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f790f4c5274f100158d4c23bc5eddf659c1fe93ef4025488f9493d88f1490d88`  
		Last Modified: Tue, 14 Feb 2023 19:31:12 GMT  
		Size: 122.4 MB (122355677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bf170fd9e6726c86c0d4b478d9ec522e82c527a8e708668f48233a4d03f618`  
		Last Modified: Tue, 14 Feb 2023 19:30:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a5d1c1b6ed103f8c7f97c73ed546ff7e767b10473b55c15c0d4e1a13a69481`  
		Last Modified: Tue, 14 Feb 2023 19:47:34 GMT  
		Size: 4.2 MB (4188243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0130eaa2f0b1f7646719d82927743bd84c83ed450eb8be4db5327d280d5e4d0`  
		Last Modified: Wed, 15 Feb 2023 19:20:05 GMT  
		Size: 1.2 MB (1217841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab1f57409241476a86d26944527bc2c6c3903eadb21221b8d96da52120b3109`  
		Last Modified: Wed, 15 Feb 2023 19:20:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ef43980c42cd8a35929f0378a7ecd1918acd54140264da387b01dc7e3d6bea0b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127437368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd812dbbfb10d2a70518b9169ed3ed8f3e00b43a8b7ce2f98f7e72b09d33330`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:49:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 21:49:23 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:54:56 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:57:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:57:12 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:57:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:57:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:57:13 GMT
WORKDIR /go
# Tue, 14 Feb 2023 21:22:55 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 21:22:55 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:49:33 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:49:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:49:33 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:49:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:49:35 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:49:35 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11114cba5e5d7175bb4d5b434db94e1c2bf0f8263c6cf2b8cbf3c1fc853114b5`  
		Last Modified: Fri, 10 Feb 2023 22:00:04 GMT  
		Size: 286.1 KB (286119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbe98122be79c40d67ce24806b19f5bd6a2f3025a18faa3a9e07c836eda77a3`  
		Last Modified: Tue, 14 Feb 2023 20:03:20 GMT  
		Size: 118.7 MB (118722534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2006a6001995de26a92cbdcc7917c763ee43c1f153331e17ed59bc706622a4`  
		Last Modified: Tue, 14 Feb 2023 20:02:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241e307a6c2a59713b29a4001892e4737b03b8bdc797f283f8bfef8e5976a360`  
		Last Modified: Tue, 14 Feb 2023 21:23:46 GMT  
		Size: 4.2 MB (4151224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd6d861ad1e103851af9cad05cca9ddd82af819c16eef77a788212eb48a451a`  
		Last Modified: Wed, 15 Feb 2023 18:50:44 GMT  
		Size: 1.2 MB (1166072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff6cca8082ff38bb36e60b71883dc986b05c54b1322ffe5c5906933155af3db`  
		Last Modified: Wed, 15 Feb 2023 18:50:44 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ae944139e672dc9c4065b2e83f98a2c2522db0397a33f3b287e771e01c90b043
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126518789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b5e54b6cc5a620df577f3659a5f2415b1ab88786c0ee932fd73c5c026786cb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 23:34:00 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 23:34:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 22:43:55 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 22:46:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 22:46:04 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 22:46:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 22:46:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 22:46:05 GMT
WORKDIR /go
# Wed, 15 Feb 2023 01:37:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 15 Feb 2023 01:37:44 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:57:37 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:57:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:57:37 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:57:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:57:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ee22df4e0527c9d317c1729808b4fc333083ad4d5a41645d79beabb64e9415`  
		Last Modified: Fri, 10 Feb 2023 23:50:08 GMT  
		Size: 285.4 KB (285353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0083f2e9af62d9a5b5bcf25401158f3ebb34f9fe9e7e951a52b22e9f6a15f1ed`  
		Last Modified: Tue, 14 Feb 2023 22:54:26 GMT  
		Size: 118.5 MB (118480449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6506d85184bedd4e64bb66e1357511d9dde4bc32c2c99d3183c2cec84f20e7e5`  
		Last Modified: Tue, 14 Feb 2023 22:54:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc4386697a4bb55f0e63b324c4a0b444eec215aff0cffc35d7affc50fff2041`  
		Last Modified: Wed, 15 Feb 2023 01:38:34 GMT  
		Size: 3.7 MB (3720630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03d748e87e34207a999297a575c405a0c36bf6b02a35f1c1b370ae25d1daf26`  
		Last Modified: Wed, 15 Feb 2023 18:58:45 GMT  
		Size: 1.2 MB (1163331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957e61fda37fb7df272efba4e6f8cd0083db173bff77b1e4dbbfad3fba3cd92b`  
		Last Modified: Wed, 15 Feb 2023 18:58:44 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:345963f3560e208ac6bacd024a578f5b7e01f8b734c723eddee3617aa9f0eb48
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125824793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e4189a65557b7e2dd531761f337fa9ebac950fe19c378297b031b64ef548d7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:38:33 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:38:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:43:03 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:44:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:44:06 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:44:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:44:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:44:07 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:05:45 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:05:45 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:39:25 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:39:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:39:26 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:39:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:39:28 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:39:28 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55522c79112429742fe76c795b9509c5cd1e8198e0caa2a1e355c0e60a719576`  
		Last Modified: Fri, 10 Feb 2023 22:44:19 GMT  
		Size: 286.3 KB (286257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a025c151a25ec079b20475bc7d9114a55273ff4768db3589c2a9e3556263ff`  
		Last Modified: Tue, 14 Feb 2023 19:48:57 GMT  
		Size: 116.9 MB (116917630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e172ed32e80e014974dc5c64a3cec7ac2d456fe4b21179f48138df590112cdab`  
		Last Modified: Tue, 14 Feb 2023 19:48:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbab95e946333dfac53de76b5f4cfc1f90fec80107055af4eb888824c147950`  
		Last Modified: Tue, 14 Feb 2023 20:06:09 GMT  
		Size: 4.2 MB (4234639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52ae4d010a784b362566e543eeacafbef900440cdda0b182dc5ea51a53b070c`  
		Last Modified: Wed, 15 Feb 2023 18:40:08 GMT  
		Size: 1.1 MB (1123743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d9033ce04f11b49957c7855096c7e5ed4a4e3ad840dd150fc0823b230b3742`  
		Last Modified: Wed, 15 Feb 2023 18:40:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:8126a0d2b7cc9613f70b6b5375c14cc61dfca5dc1b83adc5be33efab8eacc69f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126579575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da1cd24f35f4106a8a7176a2f2b5656a22982a1787b9204d3eaab9ec535ef58`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:36 GMT
ADD file:ec037a0d4b462d12963ac20d9ec49bb73b4bcaf84d4bc7b364ebf93667e585b0 in / 
# Fri, 10 Feb 2023 21:20:36 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:40:13 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:40:14 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:46:09 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:48:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:48:44 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:48:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:48:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:48:46 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:12:48 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:12:48 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:16:53 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:16:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:16:54 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 19:16:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 19:16:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 19:16:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:aa3c56f9c6f127b6c8f628c95db165741ca400d19bdaef2752d80f093e47451e`  
		Last Modified: Fri, 10 Feb 2023 21:21:37 GMT  
		Size: 3.4 MB (3390750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788962e1689dbb14c760601cbf633ae350e98e3a045f8010924cd585de6b6a3e`  
		Last Modified: Fri, 10 Feb 2023 22:53:32 GMT  
		Size: 286.6 KB (286645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ae39b9ad00c218f9156f0958fa48f3062eb5830b791b8592e5f25fd576c7c5`  
		Last Modified: Tue, 14 Feb 2023 19:56:18 GMT  
		Size: 117.3 MB (117316160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f3bf55d586b31bb5c97f2cbf5167fd359b61336f93bed839c2f4de055ced88`  
		Last Modified: Tue, 14 Feb 2023 19:55:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e012d53123423a5fe128ab31d41596d83d8e48699ad608e9eb58dd0b2322fe0`  
		Last Modified: Tue, 14 Feb 2023 20:13:35 GMT  
		Size: 4.5 MB (4479556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90177e6cf58218f094608b8401f41d0da78a0cf57d95718e48e8c6e2f77c6fae`  
		Last Modified: Wed, 15 Feb 2023 19:18:00 GMT  
		Size: 1.1 MB (1105899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e897949e5a46b09b4606d86b20ecb5684cb43f7e1bed1f208ee9b7e93d208c`  
		Last Modified: Wed, 15 Feb 2023 19:17:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:777aec044ded48957652f0c6ceac314892e1c892c85a07084f80762791aa55b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129606877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4f36416ff115d90097fe1378fca1a1ded179a50ee13701194f1193833e1d5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:25 GMT
ADD file:03b2fb4d732a294329449ff55c5d84f7d2735e6510985718979469994f3a607b in / 
# Fri, 10 Feb 2023 21:41:26 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:27:44 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:27:44 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:47:34 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:49:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:49:23 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:49:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:49:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:49:24 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:12:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:12:32 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:42:20 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:42:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:42:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:42:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:42:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:42:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:24c4f8de3549a39c64b0edc2cfa68769b373f35138d0f13725100160bb32d4e2`  
		Last Modified: Fri, 10 Feb 2023 21:42:16 GMT  
		Size: 3.2 MB (3175116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affa53ed2f1b70a83e3a15cae881ca47cd40f6ac11060717cdbbd4e405f9d586`  
		Last Modified: Fri, 10 Feb 2023 22:37:18 GMT  
		Size: 285.0 KB (285032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafa18be4ff892e2222424e6e25c36c21c4d94825607e8b840d2384c6ab73651`  
		Last Modified: Tue, 14 Feb 2023 19:54:27 GMT  
		Size: 120.8 MB (120811850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c3965c085d018b012055d834e6c56402c39a086413f83eb42fed0eba26be6`  
		Last Modified: Tue, 14 Feb 2023 19:54:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250c53f2b7534f15112393341635149f8ad756241a7c7979ec7ad6fbd3959ff1`  
		Last Modified: Tue, 14 Feb 2023 20:13:22 GMT  
		Size: 4.2 MB (4163882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11288ef421d5fc2fc1e1a7cd7350fb7f4ad371aa6edad42bb5ffa8f95cb2f2bc`  
		Last Modified: Wed, 15 Feb 2023 18:43:31 GMT  
		Size: 1.2 MB (1170432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b792196575b477b3bd73841238a0c4445026bc982b5e0236ef24a59eec4875`  
		Last Modified: Wed, 15 Feb 2023 18:43:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:e4b4bb126038410035c8c6962d643dbf73d0b1d8ee3108c4f005238402a9a0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `caddy:2.6-builder-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:bff20886c4e50c2ff56c65ce2b8b2f6f861b63544087ebc9828b8283abf3e9ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1893205034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9666c08cd03c61fe14a234d3f8760533430f35e891dccd0f5540cb34fd9834a4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 03:01:55 GMT
ENV GIT_VERSION=2.23.0
# Thu, 12 Jan 2023 03:01:56 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 12 Jan 2023 03:01:57 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 12 Jan 2023 03:01:58 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 12 Jan 2023 03:02:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 03:03:01 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 03:03:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Feb 2023 20:35:10 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 20:39:32 GMT
RUN $url = 'https://dl.google.com/go/go1.19.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8d84af29e46c38b1eec77f9310310517c9e394ac7489e1c7329a94b443b0388d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Feb 2023 20:39:34 GMT
WORKDIR C:\go
# Tue, 14 Feb 2023 21:16:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 21:16:10 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:20:04 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:20:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Feb 2023 19:20:39 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203425975bec1802428fad91a2e5f01172b161062c12eddf729e548bf7e134e0`  
		Last Modified: Thu, 12 Jan 2023 03:48:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80e42e19ab862b4adea06f1995e1f5cbb2c11ad8d68ae4a7bb5d0da5d0e6f38`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be5d5df8cec6d1386f78a342668c3d2cb809372865459c1b35aa8d5a39a463b`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e467d553c4972b55bf8e3d80b16f245e5bb38f28d80b91ca4f9f90c09a6c28d`  
		Last Modified: Thu, 12 Jan 2023 03:48:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97054b77b205167acd5a303c8aa82e380f090ff4e2ded81d3425ec78500139d`  
		Last Modified: Thu, 12 Jan 2023 03:48:14 GMT  
		Size: 25.5 MB (25470784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e150d9e1a1da09e17313cb3b6358d2f16cf2919c51e9addf30500de9d03292ef`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c0d792e2a7942826a61fdc26b6081ab404122751ff4f4dd8f5b8b0eca21399`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 324.5 KB (324466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd89ac843c0479ae40ca8c747e8a676229754549dbfeb9fe7157fdf1a60e685f`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0892c7d4de38540a99ca06e09c0a995b2e119c5ae853eadc2f7558f69bf44bb1`  
		Last Modified: Tue, 14 Feb 2023 20:56:57 GMT  
		Size: 157.8 MB (157805981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b2ec2bef689e3f934369ec3ebb90a5b06c0cbd77b2364e23a776b4da7a68f5`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066daab446064e42a798fe1592cbb9befd18dc7c368cc287f403168c17647f44`  
		Last Modified: Tue, 14 Feb 2023 21:18:46 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ea7fb211a6a6bdf1db9842354942dfaf3dc66bb87b9ce2b1620b897655022d`  
		Last Modified: Tue, 14 Feb 2023 21:18:44 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1a9f71a17b653aeea9897c2da8205709b77073460fc648f6daa323ffffee8d`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53678f100709f21522f2dd0732c10bbb5a70107fa9a4fcdd4895786c68d0bb27`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a973e4e836b19e1ccb3104f7458b2ed9a0aee58d697b6b7a8f7b8800265560f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:53 GMT  
		Size: 1.6 MB (1641852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9b2ad53ca032d7a1d8ef1944923a40be2d6c2fbd4945695a1d7cf5ea708613`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:8bfb22a6d9ad624ddad733879370d4e05a82cc5c15125cdc2365e8f7a4fe79e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `caddy:2.6-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:8208748738c8ad71587dbe2fa710487d6ed5a1ef462b3591e30be906145cab13
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1572172924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c99c2ba8e5059d5dc3ad70afada06d399bff99be54c4c7bf3908b0889a8719a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 02:57:40 GMT
ENV GIT_VERSION=2.23.0
# Thu, 12 Jan 2023 02:57:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 12 Jan 2023 02:57:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 12 Jan 2023 02:57:42 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 12 Jan 2023 02:58:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 02:58:23 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 02:58:47 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Feb 2023 20:31:21 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 20:34:49 GMT
RUN $url = 'https://dl.google.com/go/go1.19.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8d84af29e46c38b1eec77f9310310517c9e394ac7489e1c7329a94b443b0388d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Feb 2023 20:34:51 GMT
WORKDIR C:\go
# Tue, 14 Feb 2023 21:17:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 21:17:18 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:20:52 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:20:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:21:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Feb 2023 19:21:22 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2fc8728d9c7bf65edf893fd902f8b1bd780f93623858960c9db79e39922b169`  
		Last Modified: Thu, 12 Jan 2023 03:47:24 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7935a4c648078e79f67a11bcd5908e251110dd6c5a4ee49a607f332dd25af9`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d257f8b122044547f89f00f58661b25aca97c92f3831e7aaa11975639b6e35d4`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95acaa75c1852ba1320c5db382b01f587badb615b6746b59be27eedcf96ab667`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5201ba65043fa621c187729f18aecf4c549cdfa12cd6d8cab7a901d893f3a8a8`  
		Last Modified: Thu, 12 Jan 2023 03:47:29 GMT  
		Size: 25.7 MB (25702230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a317a349bca5ab28ba7c1ce039928a56390f7e7a8d7ddec07efcc1c9883e5d`  
		Last Modified: Thu, 12 Jan 2023 03:47:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8850296b8fbb853a6eb6341f7484cd4bc622e9f679f12c4123eddf08b7f398fb`  
		Last Modified: Thu, 12 Jan 2023 03:47:18 GMT  
		Size: 554.2 KB (554212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b724dc103b7bd177436e0035a2c0eaffd1187dcb978222f4e7c1014ca50ee`  
		Last Modified: Tue, 14 Feb 2023 20:55:01 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f4ea18edcbbc3120e8b270d76ae1a1876db9d493e1b703d25194e08b0896c`  
		Last Modified: Tue, 14 Feb 2023 20:55:55 GMT  
		Size: 158.0 MB (158000355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81da76ff355cb5fcac2247f23ca1fe8dd4256b41f2edd58b34f886fcb74bc6e7`  
		Last Modified: Tue, 14 Feb 2023 20:55:01 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc05ca820f63f78de074bd0a9ffe6889c8e3405b0563cf21ef5013179b8f407`  
		Last Modified: Tue, 14 Feb 2023 21:19:03 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b911bfee9062064c2f989b2acf01493bb3c9ad5989eb456277dfe272c1dcd2`  
		Last Modified: Tue, 14 Feb 2023 21:19:01 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aa3117c7e54c9d38a6d368beb815482c58bd46981294fc7c45046ca02b8d34`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710d1b3e32dd905f2dc2f33df9481f9abdd52cbd0028eadd5d0517fe673c3de1`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df812b30f4c795624a0ff09a18f3ac73987de268d9ee1aa080998e222a6f6e3`  
		Last Modified: Wed, 15 Feb 2023 20:18:10 GMT  
		Size: 1.9 MB (1868549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced4b40932769c58cc0b5348fdc7b4189892820c655d4029b988aafd8692dcd0`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6-windowsservercore`

```console
$ docker pull caddy@sha256:a0e880f407bc812d350d220b76e5e9da56ef9a34384f075923fb0eacfc9eef27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.3887; amd64
	-	windows version 10.0.20348.1487; amd64

### `caddy:2.6-windowsservercore` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:371255c187169392f30d7caf1e65b8a8708afbdd8520eb74df9c38d973195766
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723380167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa79dce896513046be66642ea60c82eaf2266ff5533f3e8c40a79c7b779c0eca`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:16:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:15:47 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:17:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:17:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:17:11 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:17:12 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:17:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:17:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:17:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:17:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:17:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:17:20 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:17:21 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:17:22 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:17:24 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:17:43 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:17:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47af8a9c9ef8e49d65e53dd207ad0935ce7a2b50b2f253e6a5b037494ae19d0a`  
		Last Modified: Thu, 09 Feb 2023 01:16:50 GMT  
		Size: 401.5 KB (401472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d742cb3ca192278158c048ecc9f358855bc8f2629af70c62b9610a1fc66bbf0a`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859ce744a498d8f5affa0958dae6a0027cd48925c7c0bdf78214019c927eb34b`  
		Last Modified: Wed, 15 Feb 2023 20:17:06 GMT  
		Size: 14.7 MB (14694270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64525df3f764c2e65e711fbd328781c61243029c264aca6b09309e584dbb69b3`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231e1956368caba27b753959bf1fb5d38cf0e798477a45110f2691b063809554`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405677c240161263f0ca900ffca71596061f8d59668d524a80f16957c120f0c`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638a2e8fc9bd411f13b7b5a8b82272fd39024ac9b711d2bc73c28c39314fc3bb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1b8ca9045f120e19c22debd19df59f42aa442b84c073c7cfc2f5a2d0f463cb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c7468bd4bec28c11efd397d435df6a129ffc73265d2d2c4162bb121a336d08`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de41f5feb06b95a77601b9fd09ab7409b567e0d9684c46dfcdc4a067a00adc`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab6a97db0980bf9c94414bfb713b5db0ed7bec52a805303782c4309a6e9f62b`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41271d7026e5d15682fc59b1ac99ac0a67909c591ea0c7ab0885207386064744`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b605f7b22df792b7b41d97cec04cbfb795ba3588fd9e0b44363147a7a02820`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c2c11f6f75de707c6475d6248a27eb983282648b0a923c47e2894db7304e0d`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48461b499cb5763190c69d134f0b96625458bdd69fe78a15ade15efbad156033`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745ffdaac1ecada0622ef6d6ccfe6140992921240b91567821b96a07a72df8b8`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf9895ba16206d3ebb35a3a6e3f615542102d00230528158c62eee814428521`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc57c33625ddac815d78d81c0feb25f7dd3d6ea9f6d4f6238024e4898a15ef3c`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 316.4 KB (316447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31243cdae7d3d8bcf0b00d6c6c0a1f4ec3c2c277ca964f747f8acc133cef56a2`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6-windowsservercore` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:0722e548c2efb29869e87e89dc7cf03de8d31fe33c28e9e61a33f018b0a7a3e4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1401943529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a230b066a2fbe8bdfee6749b8afe9b1655260bb3643408c49082c8754a4cff75`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:18:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:18:03 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:19:13 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:19:14 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:19:15 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:24 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:26 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:27 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:46 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:19:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42eb48143612ee855d99c932e324b1bd035c60554117edeaa805402060613c51`  
		Last Modified: Thu, 09 Feb 2023 01:17:17 GMT  
		Size: 635.9 KB (635943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e120c0944228b4b6623b958c83433bc43f104b64cecccbd1ac7ab250e7a68db7`  
		Last Modified: Wed, 15 Feb 2023 20:17:30 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891cca6ce816bbe4dd40bd862cae84155f0da6f7f13ab15fb80f92c471772be7`  
		Last Modified: Wed, 15 Feb 2023 20:17:34 GMT  
		Size: 14.9 MB (14907106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e4718f6f1c46191ed75eaff08ff294c5ad0f384309aca914d5687324213f83`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0edcd24848e16049bee383e4ae89134f9d07da6079deed1398df66ad8a401ac`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b890b1c144cd00660796b630f5a2b8009a7c8b98a852cc4e645d13d84f4b48`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12054588e533ec29d2f174499ee24489e7b6d7b8527337dcdcc25a6ec29973`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e7efe9a5a718b562e89379f47cd1c2919b05c52ad1a2ceb9525d7f98f2f0d1`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fc39bc9c2bdee1444bb0e46b53cb55da0913be6b115f95bc50f5ed370138e`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d17482a1fa64018a51f2d8467fb3cba2c11aae5e67a689612e314d713ca8b0`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4843586865795ebb5e828c5f7fe6c9f829f9b12d5ad2e0bbf9f302874fc39a27`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd44712296ac1e7d28147c40159638788a75b58c17764de2757fcfda62f5551a`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5344aa95ac41ce0d03e95ae47d07c9ddef532b47bbfeb871053e69eacf5429a6`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf50f2a8532ee01e411b12116a827c2823a5cb2ee71091b4b724c44b6ba0f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b71f209c61027e4688f4e4b109ec883c187ed74b3d4c27e4b11596a4f20a07`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df052fc38d64efbb8657dd2c40cfa28c56f1137efcf1d7751277c1c81626b39e`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266955548153e827efba631ef21036116d523e11f332aae3910c4e6b773896f5`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59f15231c2a3b500e116b42a5254f441985197b1d364bc46a71cd917af38ec9`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 347.4 KB (347422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4a927a917a632a25082f22d95b2df35568f4522d622efe890c6d57457ed461`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6-windowsservercore-1809`

```console
$ docker pull caddy@sha256:9b3fc2e9403b99a6fce9d5b94de587e848616342ccad9275d8bbead1a4b8f1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `caddy:2.6-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:371255c187169392f30d7caf1e65b8a8708afbdd8520eb74df9c38d973195766
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723380167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa79dce896513046be66642ea60c82eaf2266ff5533f3e8c40a79c7b779c0eca`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:16:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:15:47 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:17:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:17:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:17:11 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:17:12 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:17:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:17:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:17:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:17:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:17:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:17:20 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:17:21 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:17:22 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:17:24 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:17:43 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:17:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47af8a9c9ef8e49d65e53dd207ad0935ce7a2b50b2f253e6a5b037494ae19d0a`  
		Last Modified: Thu, 09 Feb 2023 01:16:50 GMT  
		Size: 401.5 KB (401472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d742cb3ca192278158c048ecc9f358855bc8f2629af70c62b9610a1fc66bbf0a`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859ce744a498d8f5affa0958dae6a0027cd48925c7c0bdf78214019c927eb34b`  
		Last Modified: Wed, 15 Feb 2023 20:17:06 GMT  
		Size: 14.7 MB (14694270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64525df3f764c2e65e711fbd328781c61243029c264aca6b09309e584dbb69b3`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231e1956368caba27b753959bf1fb5d38cf0e798477a45110f2691b063809554`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405677c240161263f0ca900ffca71596061f8d59668d524a80f16957c120f0c`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638a2e8fc9bd411f13b7b5a8b82272fd39024ac9b711d2bc73c28c39314fc3bb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1b8ca9045f120e19c22debd19df59f42aa442b84c073c7cfc2f5a2d0f463cb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c7468bd4bec28c11efd397d435df6a129ffc73265d2d2c4162bb121a336d08`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de41f5feb06b95a77601b9fd09ab7409b567e0d9684c46dfcdc4a067a00adc`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab6a97db0980bf9c94414bfb713b5db0ed7bec52a805303782c4309a6e9f62b`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41271d7026e5d15682fc59b1ac99ac0a67909c591ea0c7ab0885207386064744`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b605f7b22df792b7b41d97cec04cbfb795ba3588fd9e0b44363147a7a02820`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c2c11f6f75de707c6475d6248a27eb983282648b0a923c47e2894db7304e0d`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48461b499cb5763190c69d134f0b96625458bdd69fe78a15ade15efbad156033`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745ffdaac1ecada0622ef6d6ccfe6140992921240b91567821b96a07a72df8b8`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf9895ba16206d3ebb35a3a6e3f615542102d00230528158c62eee814428521`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc57c33625ddac815d78d81c0feb25f7dd3d6ea9f6d4f6238024e4898a15ef3c`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 316.4 KB (316447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31243cdae7d3d8bcf0b00d6c6c0a1f4ec3c2c277ca964f747f8acc133cef56a2`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:113f187a1100da96770eeaecc6e118b4be7ef33cb4d01611de3e3045ed3a4acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `caddy:2.6-windowsservercore-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:0722e548c2efb29869e87e89dc7cf03de8d31fe33c28e9e61a33f018b0a7a3e4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1401943529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a230b066a2fbe8bdfee6749b8afe9b1655260bb3643408c49082c8754a4cff75`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:18:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:18:03 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:19:13 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:19:14 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:19:15 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:24 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:26 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:27 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:46 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:19:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42eb48143612ee855d99c932e324b1bd035c60554117edeaa805402060613c51`  
		Last Modified: Thu, 09 Feb 2023 01:17:17 GMT  
		Size: 635.9 KB (635943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e120c0944228b4b6623b958c83433bc43f104b64cecccbd1ac7ab250e7a68db7`  
		Last Modified: Wed, 15 Feb 2023 20:17:30 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891cca6ce816bbe4dd40bd862cae84155f0da6f7f13ab15fb80f92c471772be7`  
		Last Modified: Wed, 15 Feb 2023 20:17:34 GMT  
		Size: 14.9 MB (14907106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e4718f6f1c46191ed75eaff08ff294c5ad0f384309aca914d5687324213f83`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0edcd24848e16049bee383e4ae89134f9d07da6079deed1398df66ad8a401ac`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b890b1c144cd00660796b630f5a2b8009a7c8b98a852cc4e645d13d84f4b48`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12054588e533ec29d2f174499ee24489e7b6d7b8527337dcdcc25a6ec29973`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e7efe9a5a718b562e89379f47cd1c2919b05c52ad1a2ceb9525d7f98f2f0d1`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fc39bc9c2bdee1444bb0e46b53cb55da0913be6b115f95bc50f5ed370138e`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d17482a1fa64018a51f2d8467fb3cba2c11aae5e67a689612e314d713ca8b0`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4843586865795ebb5e828c5f7fe6c9f829f9b12d5ad2e0bbf9f302874fc39a27`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd44712296ac1e7d28147c40159638788a75b58c17764de2757fcfda62f5551a`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5344aa95ac41ce0d03e95ae47d07c9ddef532b47bbfeb871053e69eacf5429a6`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf50f2a8532ee01e411b12116a827c2823a5cb2ee71091b4b724c44b6ba0f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b71f209c61027e4688f4e4b109ec883c187ed74b3d4c27e4b11596a4f20a07`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df052fc38d64efbb8657dd2c40cfa28c56f1137efcf1d7751277c1c81626b39e`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266955548153e827efba631ef21036116d523e11f332aae3910c4e6b773896f5`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59f15231c2a3b500e116b42a5254f441985197b1d364bc46a71cd917af38ec9`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 347.4 KB (347422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4a927a917a632a25082f22d95b2df35568f4522d622efe890c6d57457ed461`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6.4`

```console
$ docker pull caddy@sha256:236163a87c5609986ce7ddead7d8aaf992314f031699ddde2a400597640965e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.3887; amd64
	-	windows version 10.0.20348.1487; amd64

### `caddy:2.6.4` - linux; amd64

```console
$ docker pull caddy@sha256:36ba71b44afa613ecf0aadce8e4b9e3f56e0c4b0a78c8edf4e8c2485f21b35ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17449113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8464e23f16f9a82426bbdc3ac8c94270a84453ddc86b9147505a2378a7c2fd0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:38:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 11 Feb 2023 07:38:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 19:19:21 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 19:19:23 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 19:19:24 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:25 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 19:19:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e3e797818bc929d95bae8220b7b6034b559c217ef5bf622dc7fedc8d270a48`  
		Last Modified: Sat, 11 Feb 2023 07:39:01 GMT  
		Size: 351.2 KB (351178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cebb4c80b3906a9b751ee9a512c1581331b1fd691c84f575c01a29e28403dde`  
		Last Modified: Sat, 11 Feb 2023 07:39:00 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90648ba22c191b969d8db393bf6138e7d6ecc1b70b3865d1717ec4d663192d89`  
		Last Modified: Wed, 15 Feb 2023 19:19:52 GMT  
		Size: 14.3 MB (14282621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5b39c4c37396031351c9753e4c7df6f2114d0ef588953b97c668d0ec7e2f1e50
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16582274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ffa8388ed5f7f62ab116b850faa63ff3214dea5fb007a77196a8efd0023832`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:28:54 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 21:28:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:49:22 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:49:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:49:26 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:49:26 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:49:27 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:49:28 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:49:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a400dcba29ff44f8e5bf01493def4f19629aca6d103cb2a66ca87c457f7414`  
		Last Modified: Fri, 10 Feb 2023 21:29:47 GMT  
		Size: 345.8 KB (345811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b946768825eb5ed2fc6f932fdb0b0c552f4c35c39dada07eddd70ce4a535953`  
		Last Modified: Fri, 10 Feb 2023 21:29:47 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f11ff5bb8d752ef2e91afa46770077fd62ddc9e78f280c00e796bf841c9d49f`  
		Last Modified: Wed, 15 Feb 2023 18:50:25 GMT  
		Size: 13.6 MB (13612205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4` - linux; arm variant v7

```console
$ docker pull caddy@sha256:21302c9acb44ea61fccba3ef765712da93fede2d928aaafc8f7bd77a35d91953
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16365562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600d5193b2ba5875b66a6579717ec1aab50be117445a5a657045572141d1187c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:37 GMT
ADD file:193f48d48ed2e90a0e81663757e372f59806151c17e82113f03443db0ef723c3 in / 
# Fri, 10 Feb 2023 21:51:37 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:37:19 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:37:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:57:27 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:57:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:57:30 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:57:30 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:57:31 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:57:32 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:beefe5ad637c7db32e6afc68103fc4e779630219979216a625338ab55f7d191c`  
		Last Modified: Fri, 10 Feb 2023 21:52:51 GMT  
		Size: 2.4 MB (2420494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2ab4edb1f0a14b28a55f050d62d8e54111075639a0fa8f173448814ba0d00`  
		Last Modified: Fri, 10 Feb 2023 22:38:25 GMT  
		Size: 342.6 KB (342588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0580184dd0082f009564a7a3923731f202cbe4bd8b857dbca2c77da8e7434815`  
		Last Modified: Fri, 10 Feb 2023 22:38:25 GMT  
		Size: 7.5 KB (7479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8682e09bc231d5c9076b76cb92cb3b1185b870277da03dbd7e87d7981ff6147a`  
		Last Modified: Wed, 15 Feb 2023 18:58:28 GMT  
		Size: 13.6 MB (13595001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:6c2623f6bf30798be5c37fc7484e45ecc288d493fb657883f59ddb27ed714ad8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16130997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a38afdc517ef4cff6b6b51a1c6a633c2826599b07feb1e88380d0f783e35cf1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:00:35 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:00:37 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:39:20 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:39:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:39:22 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:39:22 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:39:23 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:39:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70730e8e2fb933ec157ec87f2a4fb4ad45e8e578b8f7c76cc4846631d773554`  
		Last Modified: Fri, 10 Feb 2023 22:01:02 GMT  
		Size: 350.2 KB (350153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a4b7390d269477c225f1d03e825d2d8bdf6b4d87b5f7bb8811b341e56b7d36`  
		Last Modified: Fri, 10 Feb 2023 22:01:02 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2743d2ef53ee6edb0e39c89bf16957e3a00990410b2d1a126dca1b2d196182`  
		Last Modified: Wed, 15 Feb 2023 18:39:53 GMT  
		Size: 13.1 MB (13063787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4` - linux; ppc64le

```console
$ docker pull caddy@sha256:8861ab3ae3d0c180e38142c2f7482f9ce1773419eb29ed9d6d18308246858093
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15955172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5819f0ab4928a30c29293a27299a3b44371cd3bd97df91432ef7b3f43b692d8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:13:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:13:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 19:16:26 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:16:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 19:16:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 19:16:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 19:16:42 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:16:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:16:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:16:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:16:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:16:47 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:16:47 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 19:16:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782bd0321e6539bb7dac8574fd36bad22059ef06bb63dc842165f69d0a821572`  
		Last Modified: Fri, 10 Feb 2023 22:14:16 GMT  
		Size: 363.1 KB (363088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb806b2600b0209a73fc7175ab778d0224661034b2f722bd1a0aec1eb9eabe3d`  
		Last Modified: Fri, 10 Feb 2023 22:14:15 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd7c8ae860931dd79dea76d33bc21bb11d89cd4d133cdb41078b040afc6633e`  
		Last Modified: Wed, 15 Feb 2023 19:17:41 GMT  
		Size: 12.8 MB (12779898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4` - linux; s390x

```console
$ docker pull caddy@sha256:4e1ed99f133abf02d6a7c77849978bb621f748e18c9cb9f7a1dbf88480ddb8d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16792756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45cd164da734310b788dcbd4f6c94bccff6e48705fe4d42ecca07a54e9459a9c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:14:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:41:48 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:41:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:41:59 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:41:59 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:42:00 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:42:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:42:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:42:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:42:03 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:42:04 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:42:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:42:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:42:05 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:42:06 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:42:07 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:42:07 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:42:08 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:42:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e6ec82400496ce74e37120e1655955b79303daaa5b8ca7e956e3cd96ddd6e9`  
		Last Modified: Fri, 10 Feb 2023 22:15:05 GMT  
		Size: 352.8 KB (352801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5b992687f93ced3715ad97bd95ab37daef5685b784e195209caefbc48f14e9`  
		Last Modified: Fri, 10 Feb 2023 22:15:05 GMT  
		Size: 7.6 KB (7557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccc40924ce2df3343fa5465a92ccaa4ed80e0883190a99d3f468c60f9ddbcf8`  
		Last Modified: Wed, 15 Feb 2023 18:43:19 GMT  
		Size: 13.8 MB (13838817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:371255c187169392f30d7caf1e65b8a8708afbdd8520eb74df9c38d973195766
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723380167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa79dce896513046be66642ea60c82eaf2266ff5533f3e8c40a79c7b779c0eca`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:16:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:15:47 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:17:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:17:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:17:11 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:17:12 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:17:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:17:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:17:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:17:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:17:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:17:20 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:17:21 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:17:22 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:17:24 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:17:43 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:17:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47af8a9c9ef8e49d65e53dd207ad0935ce7a2b50b2f253e6a5b037494ae19d0a`  
		Last Modified: Thu, 09 Feb 2023 01:16:50 GMT  
		Size: 401.5 KB (401472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d742cb3ca192278158c048ecc9f358855bc8f2629af70c62b9610a1fc66bbf0a`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859ce744a498d8f5affa0958dae6a0027cd48925c7c0bdf78214019c927eb34b`  
		Last Modified: Wed, 15 Feb 2023 20:17:06 GMT  
		Size: 14.7 MB (14694270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64525df3f764c2e65e711fbd328781c61243029c264aca6b09309e584dbb69b3`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231e1956368caba27b753959bf1fb5d38cf0e798477a45110f2691b063809554`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405677c240161263f0ca900ffca71596061f8d59668d524a80f16957c120f0c`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638a2e8fc9bd411f13b7b5a8b82272fd39024ac9b711d2bc73c28c39314fc3bb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1b8ca9045f120e19c22debd19df59f42aa442b84c073c7cfc2f5a2d0f463cb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c7468bd4bec28c11efd397d435df6a129ffc73265d2d2c4162bb121a336d08`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de41f5feb06b95a77601b9fd09ab7409b567e0d9684c46dfcdc4a067a00adc`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab6a97db0980bf9c94414bfb713b5db0ed7bec52a805303782c4309a6e9f62b`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41271d7026e5d15682fc59b1ac99ac0a67909c591ea0c7ab0885207386064744`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b605f7b22df792b7b41d97cec04cbfb795ba3588fd9e0b44363147a7a02820`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c2c11f6f75de707c6475d6248a27eb983282648b0a923c47e2894db7304e0d`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48461b499cb5763190c69d134f0b96625458bdd69fe78a15ade15efbad156033`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745ffdaac1ecada0622ef6d6ccfe6140992921240b91567821b96a07a72df8b8`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf9895ba16206d3ebb35a3a6e3f615542102d00230528158c62eee814428521`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc57c33625ddac815d78d81c0feb25f7dd3d6ea9f6d4f6238024e4898a15ef3c`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 316.4 KB (316447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31243cdae7d3d8bcf0b00d6c6c0a1f4ec3c2c277ca964f747f8acc133cef56a2`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:0722e548c2efb29869e87e89dc7cf03de8d31fe33c28e9e61a33f018b0a7a3e4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1401943529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a230b066a2fbe8bdfee6749b8afe9b1655260bb3643408c49082c8754a4cff75`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:18:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:18:03 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:19:13 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:19:14 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:19:15 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:24 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:26 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:27 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:46 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:19:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42eb48143612ee855d99c932e324b1bd035c60554117edeaa805402060613c51`  
		Last Modified: Thu, 09 Feb 2023 01:17:17 GMT  
		Size: 635.9 KB (635943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e120c0944228b4b6623b958c83433bc43f104b64cecccbd1ac7ab250e7a68db7`  
		Last Modified: Wed, 15 Feb 2023 20:17:30 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891cca6ce816bbe4dd40bd862cae84155f0da6f7f13ab15fb80f92c471772be7`  
		Last Modified: Wed, 15 Feb 2023 20:17:34 GMT  
		Size: 14.9 MB (14907106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e4718f6f1c46191ed75eaff08ff294c5ad0f384309aca914d5687324213f83`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0edcd24848e16049bee383e4ae89134f9d07da6079deed1398df66ad8a401ac`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b890b1c144cd00660796b630f5a2b8009a7c8b98a852cc4e645d13d84f4b48`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12054588e533ec29d2f174499ee24489e7b6d7b8527337dcdcc25a6ec29973`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e7efe9a5a718b562e89379f47cd1c2919b05c52ad1a2ceb9525d7f98f2f0d1`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fc39bc9c2bdee1444bb0e46b53cb55da0913be6b115f95bc50f5ed370138e`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d17482a1fa64018a51f2d8467fb3cba2c11aae5e67a689612e314d713ca8b0`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4843586865795ebb5e828c5f7fe6c9f829f9b12d5ad2e0bbf9f302874fc39a27`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd44712296ac1e7d28147c40159638788a75b58c17764de2757fcfda62f5551a`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5344aa95ac41ce0d03e95ae47d07c9ddef532b47bbfeb871053e69eacf5429a6`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf50f2a8532ee01e411b12116a827c2823a5cb2ee71091b4b724c44b6ba0f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b71f209c61027e4688f4e4b109ec883c187ed74b3d4c27e4b11596a4f20a07`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df052fc38d64efbb8657dd2c40cfa28c56f1137efcf1d7751277c1c81626b39e`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266955548153e827efba631ef21036116d523e11f332aae3910c4e6b773896f5`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59f15231c2a3b500e116b42a5254f441985197b1d364bc46a71cd917af38ec9`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 347.4 KB (347422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4a927a917a632a25082f22d95b2df35568f4522d622efe890c6d57457ed461`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6.4-alpine`

```console
$ docker pull caddy@sha256:aacae65cfdcf61777306cf7c131fb968f67bb7fab8dfd683aa073e8b99867e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.6.4-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:36ba71b44afa613ecf0aadce8e4b9e3f56e0c4b0a78c8edf4e8c2485f21b35ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17449113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8464e23f16f9a82426bbdc3ac8c94270a84453ddc86b9147505a2378a7c2fd0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:38:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 11 Feb 2023 07:38:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 19:19:21 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 19:19:23 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 19:19:24 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:25 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 19:19:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e3e797818bc929d95bae8220b7b6034b559c217ef5bf622dc7fedc8d270a48`  
		Last Modified: Sat, 11 Feb 2023 07:39:01 GMT  
		Size: 351.2 KB (351178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cebb4c80b3906a9b751ee9a512c1581331b1fd691c84f575c01a29e28403dde`  
		Last Modified: Sat, 11 Feb 2023 07:39:00 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90648ba22c191b969d8db393bf6138e7d6ecc1b70b3865d1717ec4d663192d89`  
		Last Modified: Wed, 15 Feb 2023 19:19:52 GMT  
		Size: 14.3 MB (14282621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5b39c4c37396031351c9753e4c7df6f2114d0ef588953b97c668d0ec7e2f1e50
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16582274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ffa8388ed5f7f62ab116b850faa63ff3214dea5fb007a77196a8efd0023832`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:28:54 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 21:28:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:49:22 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:49:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:49:26 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:49:26 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:49:27 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:49:28 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:49:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a400dcba29ff44f8e5bf01493def4f19629aca6d103cb2a66ca87c457f7414`  
		Last Modified: Fri, 10 Feb 2023 21:29:47 GMT  
		Size: 345.8 KB (345811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b946768825eb5ed2fc6f932fdb0b0c552f4c35c39dada07eddd70ce4a535953`  
		Last Modified: Fri, 10 Feb 2023 21:29:47 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f11ff5bb8d752ef2e91afa46770077fd62ddc9e78f280c00e796bf841c9d49f`  
		Last Modified: Wed, 15 Feb 2023 18:50:25 GMT  
		Size: 13.6 MB (13612205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:21302c9acb44ea61fccba3ef765712da93fede2d928aaafc8f7bd77a35d91953
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16365562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600d5193b2ba5875b66a6579717ec1aab50be117445a5a657045572141d1187c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:37 GMT
ADD file:193f48d48ed2e90a0e81663757e372f59806151c17e82113f03443db0ef723c3 in / 
# Fri, 10 Feb 2023 21:51:37 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:37:19 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:37:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:57:27 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:57:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:57:30 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:57:30 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:57:31 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:57:32 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:beefe5ad637c7db32e6afc68103fc4e779630219979216a625338ab55f7d191c`  
		Last Modified: Fri, 10 Feb 2023 21:52:51 GMT  
		Size: 2.4 MB (2420494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2ab4edb1f0a14b28a55f050d62d8e54111075639a0fa8f173448814ba0d00`  
		Last Modified: Fri, 10 Feb 2023 22:38:25 GMT  
		Size: 342.6 KB (342588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0580184dd0082f009564a7a3923731f202cbe4bd8b857dbca2c77da8e7434815`  
		Last Modified: Fri, 10 Feb 2023 22:38:25 GMT  
		Size: 7.5 KB (7479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8682e09bc231d5c9076b76cb92cb3b1185b870277da03dbd7e87d7981ff6147a`  
		Last Modified: Wed, 15 Feb 2023 18:58:28 GMT  
		Size: 13.6 MB (13595001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:6c2623f6bf30798be5c37fc7484e45ecc288d493fb657883f59ddb27ed714ad8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16130997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a38afdc517ef4cff6b6b51a1c6a633c2826599b07feb1e88380d0f783e35cf1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:00:35 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:00:37 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:39:20 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:39:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:39:22 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:39:22 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:39:23 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:39:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70730e8e2fb933ec157ec87f2a4fb4ad45e8e578b8f7c76cc4846631d773554`  
		Last Modified: Fri, 10 Feb 2023 22:01:02 GMT  
		Size: 350.2 KB (350153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a4b7390d269477c225f1d03e825d2d8bdf6b4d87b5f7bb8811b341e56b7d36`  
		Last Modified: Fri, 10 Feb 2023 22:01:02 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2743d2ef53ee6edb0e39c89bf16957e3a00990410b2d1a126dca1b2d196182`  
		Last Modified: Wed, 15 Feb 2023 18:39:53 GMT  
		Size: 13.1 MB (13063787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:8861ab3ae3d0c180e38142c2f7482f9ce1773419eb29ed9d6d18308246858093
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15955172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5819f0ab4928a30c29293a27299a3b44371cd3bd97df91432ef7b3f43b692d8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:13:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:13:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 19:16:26 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:16:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 19:16:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 19:16:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 19:16:42 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:16:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:16:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:16:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:16:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:16:47 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:16:47 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 19:16:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782bd0321e6539bb7dac8574fd36bad22059ef06bb63dc842165f69d0a821572`  
		Last Modified: Fri, 10 Feb 2023 22:14:16 GMT  
		Size: 363.1 KB (363088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb806b2600b0209a73fc7175ab778d0224661034b2f722bd1a0aec1eb9eabe3d`  
		Last Modified: Fri, 10 Feb 2023 22:14:15 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd7c8ae860931dd79dea76d33bc21bb11d89cd4d133cdb41078b040afc6633e`  
		Last Modified: Wed, 15 Feb 2023 19:17:41 GMT  
		Size: 12.8 MB (12779898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:4e1ed99f133abf02d6a7c77849978bb621f748e18c9cb9f7a1dbf88480ddb8d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16792756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45cd164da734310b788dcbd4f6c94bccff6e48705fe4d42ecca07a54e9459a9c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:14:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:41:48 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:41:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:41:59 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:41:59 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:42:00 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:42:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:42:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:42:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:42:03 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:42:04 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:42:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:42:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:42:05 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:42:06 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:42:07 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:42:07 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:42:08 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:42:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e6ec82400496ce74e37120e1655955b79303daaa5b8ca7e956e3cd96ddd6e9`  
		Last Modified: Fri, 10 Feb 2023 22:15:05 GMT  
		Size: 352.8 KB (352801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5b992687f93ced3715ad97bd95ab37daef5685b784e195209caefbc48f14e9`  
		Last Modified: Fri, 10 Feb 2023 22:15:05 GMT  
		Size: 7.6 KB (7557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccc40924ce2df3343fa5465a92ccaa4ed80e0883190a99d3f468c60f9ddbcf8`  
		Last Modified: Wed, 15 Feb 2023 18:43:19 GMT  
		Size: 13.8 MB (13838817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6.4-builder`

```console
$ docker pull caddy@sha256:f3ac019c2a9615cd1adc2555d81ba8eb0412bfea8c34290fc0adfc7d77a468e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.3887; amd64
	-	windows version 10.0.20348.1487; amd64

### `caddy:2.6.4-builder` - linux; amd64

```console
$ docker pull caddy@sha256:47722ffc694507be1e2f34ca172e292fb5e226ea68d87871300b9d65f543fcce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131421587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4674ac67a52f4d29bc8349e9dcca7db8393d778c97c79d9e2f6e997603a99cd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 08:21:54 GMT
RUN apk add --no-cache ca-certificates
# Sat, 11 Feb 2023 08:21:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:24:10 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:25:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:25:43 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:25:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:25:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:25:44 GMT
WORKDIR /go
# Tue, 14 Feb 2023 19:47:10 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 19:47:10 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:19:27 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:19:28 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 19:19:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 19:19:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 19:19:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d21d5440ebff5aaaaeb115a003f7a4a3897f1866a87de95bc4a21436fc563c`  
		Last Modified: Sat, 11 Feb 2023 08:29:10 GMT  
		Size: 284.8 KB (284816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f790f4c5274f100158d4c23bc5eddf659c1fe93ef4025488f9493d88f1490d88`  
		Last Modified: Tue, 14 Feb 2023 19:31:12 GMT  
		Size: 122.4 MB (122355677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bf170fd9e6726c86c0d4b478d9ec522e82c527a8e708668f48233a4d03f618`  
		Last Modified: Tue, 14 Feb 2023 19:30:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a5d1c1b6ed103f8c7f97c73ed546ff7e767b10473b55c15c0d4e1a13a69481`  
		Last Modified: Tue, 14 Feb 2023 19:47:34 GMT  
		Size: 4.2 MB (4188243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0130eaa2f0b1f7646719d82927743bd84c83ed450eb8be4db5327d280d5e4d0`  
		Last Modified: Wed, 15 Feb 2023 19:20:05 GMT  
		Size: 1.2 MB (1217841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab1f57409241476a86d26944527bc2c6c3903eadb21221b8d96da52120b3109`  
		Last Modified: Wed, 15 Feb 2023 19:20:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ef43980c42cd8a35929f0378a7ecd1918acd54140264da387b01dc7e3d6bea0b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127437368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd812dbbfb10d2a70518b9169ed3ed8f3e00b43a8b7ce2f98f7e72b09d33330`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:49:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 21:49:23 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:54:56 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:57:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:57:12 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:57:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:57:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:57:13 GMT
WORKDIR /go
# Tue, 14 Feb 2023 21:22:55 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 21:22:55 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:49:33 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:49:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:49:33 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:49:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:49:35 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:49:35 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11114cba5e5d7175bb4d5b434db94e1c2bf0f8263c6cf2b8cbf3c1fc853114b5`  
		Last Modified: Fri, 10 Feb 2023 22:00:04 GMT  
		Size: 286.1 KB (286119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbe98122be79c40d67ce24806b19f5bd6a2f3025a18faa3a9e07c836eda77a3`  
		Last Modified: Tue, 14 Feb 2023 20:03:20 GMT  
		Size: 118.7 MB (118722534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2006a6001995de26a92cbdcc7917c763ee43c1f153331e17ed59bc706622a4`  
		Last Modified: Tue, 14 Feb 2023 20:02:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241e307a6c2a59713b29a4001892e4737b03b8bdc797f283f8bfef8e5976a360`  
		Last Modified: Tue, 14 Feb 2023 21:23:46 GMT  
		Size: 4.2 MB (4151224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd6d861ad1e103851af9cad05cca9ddd82af819c16eef77a788212eb48a451a`  
		Last Modified: Wed, 15 Feb 2023 18:50:44 GMT  
		Size: 1.2 MB (1166072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff6cca8082ff38bb36e60b71883dc986b05c54b1322ffe5c5906933155af3db`  
		Last Modified: Wed, 15 Feb 2023 18:50:44 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ae944139e672dc9c4065b2e83f98a2c2522db0397a33f3b287e771e01c90b043
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126518789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b5e54b6cc5a620df577f3659a5f2415b1ab88786c0ee932fd73c5c026786cb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 23:34:00 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 23:34:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 22:43:55 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 22:46:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 22:46:04 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 22:46:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 22:46:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 22:46:05 GMT
WORKDIR /go
# Wed, 15 Feb 2023 01:37:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 15 Feb 2023 01:37:44 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:57:37 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:57:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:57:37 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:57:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:57:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ee22df4e0527c9d317c1729808b4fc333083ad4d5a41645d79beabb64e9415`  
		Last Modified: Fri, 10 Feb 2023 23:50:08 GMT  
		Size: 285.4 KB (285353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0083f2e9af62d9a5b5bcf25401158f3ebb34f9fe9e7e951a52b22e9f6a15f1ed`  
		Last Modified: Tue, 14 Feb 2023 22:54:26 GMT  
		Size: 118.5 MB (118480449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6506d85184bedd4e64bb66e1357511d9dde4bc32c2c99d3183c2cec84f20e7e5`  
		Last Modified: Tue, 14 Feb 2023 22:54:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc4386697a4bb55f0e63b324c4a0b444eec215aff0cffc35d7affc50fff2041`  
		Last Modified: Wed, 15 Feb 2023 01:38:34 GMT  
		Size: 3.7 MB (3720630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03d748e87e34207a999297a575c405a0c36bf6b02a35f1c1b370ae25d1daf26`  
		Last Modified: Wed, 15 Feb 2023 18:58:45 GMT  
		Size: 1.2 MB (1163331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957e61fda37fb7df272efba4e6f8cd0083db173bff77b1e4dbbfad3fba3cd92b`  
		Last Modified: Wed, 15 Feb 2023 18:58:44 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:345963f3560e208ac6bacd024a578f5b7e01f8b734c723eddee3617aa9f0eb48
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125824793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e4189a65557b7e2dd531761f337fa9ebac950fe19c378297b031b64ef548d7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:38:33 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:38:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:43:03 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:44:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:44:06 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:44:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:44:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:44:07 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:05:45 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:05:45 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:39:25 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:39:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:39:26 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:39:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:39:28 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:39:28 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55522c79112429742fe76c795b9509c5cd1e8198e0caa2a1e355c0e60a719576`  
		Last Modified: Fri, 10 Feb 2023 22:44:19 GMT  
		Size: 286.3 KB (286257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a025c151a25ec079b20475bc7d9114a55273ff4768db3589c2a9e3556263ff`  
		Last Modified: Tue, 14 Feb 2023 19:48:57 GMT  
		Size: 116.9 MB (116917630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e172ed32e80e014974dc5c64a3cec7ac2d456fe4b21179f48138df590112cdab`  
		Last Modified: Tue, 14 Feb 2023 19:48:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbab95e946333dfac53de76b5f4cfc1f90fec80107055af4eb888824c147950`  
		Last Modified: Tue, 14 Feb 2023 20:06:09 GMT  
		Size: 4.2 MB (4234639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52ae4d010a784b362566e543eeacafbef900440cdda0b182dc5ea51a53b070c`  
		Last Modified: Wed, 15 Feb 2023 18:40:08 GMT  
		Size: 1.1 MB (1123743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d9033ce04f11b49957c7855096c7e5ed4a4e3ad840dd150fc0823b230b3742`  
		Last Modified: Wed, 15 Feb 2023 18:40:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:8126a0d2b7cc9613f70b6b5375c14cc61dfca5dc1b83adc5be33efab8eacc69f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126579575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da1cd24f35f4106a8a7176a2f2b5656a22982a1787b9204d3eaab9ec535ef58`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:36 GMT
ADD file:ec037a0d4b462d12963ac20d9ec49bb73b4bcaf84d4bc7b364ebf93667e585b0 in / 
# Fri, 10 Feb 2023 21:20:36 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:40:13 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:40:14 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:46:09 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:48:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:48:44 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:48:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:48:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:48:46 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:12:48 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:12:48 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:16:53 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:16:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:16:54 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 19:16:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 19:16:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 19:16:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:aa3c56f9c6f127b6c8f628c95db165741ca400d19bdaef2752d80f093e47451e`  
		Last Modified: Fri, 10 Feb 2023 21:21:37 GMT  
		Size: 3.4 MB (3390750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788962e1689dbb14c760601cbf633ae350e98e3a045f8010924cd585de6b6a3e`  
		Last Modified: Fri, 10 Feb 2023 22:53:32 GMT  
		Size: 286.6 KB (286645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ae39b9ad00c218f9156f0958fa48f3062eb5830b791b8592e5f25fd576c7c5`  
		Last Modified: Tue, 14 Feb 2023 19:56:18 GMT  
		Size: 117.3 MB (117316160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f3bf55d586b31bb5c97f2cbf5167fd359b61336f93bed839c2f4de055ced88`  
		Last Modified: Tue, 14 Feb 2023 19:55:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e012d53123423a5fe128ab31d41596d83d8e48699ad608e9eb58dd0b2322fe0`  
		Last Modified: Tue, 14 Feb 2023 20:13:35 GMT  
		Size: 4.5 MB (4479556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90177e6cf58218f094608b8401f41d0da78a0cf57d95718e48e8c6e2f77c6fae`  
		Last Modified: Wed, 15 Feb 2023 19:18:00 GMT  
		Size: 1.1 MB (1105899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e897949e5a46b09b4606d86b20ecb5684cb43f7e1bed1f208ee9b7e93d208c`  
		Last Modified: Wed, 15 Feb 2023 19:17:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-builder` - linux; s390x

```console
$ docker pull caddy@sha256:777aec044ded48957652f0c6ceac314892e1c892c85a07084f80762791aa55b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129606877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4f36416ff115d90097fe1378fca1a1ded179a50ee13701194f1193833e1d5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:25 GMT
ADD file:03b2fb4d732a294329449ff55c5d84f7d2735e6510985718979469994f3a607b in / 
# Fri, 10 Feb 2023 21:41:26 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:27:44 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:27:44 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:47:34 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:49:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:49:23 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:49:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:49:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:49:24 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:12:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:12:32 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:42:20 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:42:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:42:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:42:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:42:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:42:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:24c4f8de3549a39c64b0edc2cfa68769b373f35138d0f13725100160bb32d4e2`  
		Last Modified: Fri, 10 Feb 2023 21:42:16 GMT  
		Size: 3.2 MB (3175116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affa53ed2f1b70a83e3a15cae881ca47cd40f6ac11060717cdbbd4e405f9d586`  
		Last Modified: Fri, 10 Feb 2023 22:37:18 GMT  
		Size: 285.0 KB (285032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafa18be4ff892e2222424e6e25c36c21c4d94825607e8b840d2384c6ab73651`  
		Last Modified: Tue, 14 Feb 2023 19:54:27 GMT  
		Size: 120.8 MB (120811850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c3965c085d018b012055d834e6c56402c39a086413f83eb42fed0eba26be6`  
		Last Modified: Tue, 14 Feb 2023 19:54:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250c53f2b7534f15112393341635149f8ad756241a7c7979ec7ad6fbd3959ff1`  
		Last Modified: Tue, 14 Feb 2023 20:13:22 GMT  
		Size: 4.2 MB (4163882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11288ef421d5fc2fc1e1a7cd7350fb7f4ad371aa6edad42bb5ffa8f95cb2f2bc`  
		Last Modified: Wed, 15 Feb 2023 18:43:31 GMT  
		Size: 1.2 MB (1170432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b792196575b477b3bd73841238a0c4445026bc982b5e0236ef24a59eec4875`  
		Last Modified: Wed, 15 Feb 2023 18:43:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-builder` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:bff20886c4e50c2ff56c65ce2b8b2f6f861b63544087ebc9828b8283abf3e9ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1893205034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9666c08cd03c61fe14a234d3f8760533430f35e891dccd0f5540cb34fd9834a4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 03:01:55 GMT
ENV GIT_VERSION=2.23.0
# Thu, 12 Jan 2023 03:01:56 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 12 Jan 2023 03:01:57 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 12 Jan 2023 03:01:58 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 12 Jan 2023 03:02:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 03:03:01 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 03:03:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Feb 2023 20:35:10 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 20:39:32 GMT
RUN $url = 'https://dl.google.com/go/go1.19.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8d84af29e46c38b1eec77f9310310517c9e394ac7489e1c7329a94b443b0388d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Feb 2023 20:39:34 GMT
WORKDIR C:\go
# Tue, 14 Feb 2023 21:16:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 21:16:10 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:20:04 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:20:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Feb 2023 19:20:39 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203425975bec1802428fad91a2e5f01172b161062c12eddf729e548bf7e134e0`  
		Last Modified: Thu, 12 Jan 2023 03:48:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80e42e19ab862b4adea06f1995e1f5cbb2c11ad8d68ae4a7bb5d0da5d0e6f38`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be5d5df8cec6d1386f78a342668c3d2cb809372865459c1b35aa8d5a39a463b`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e467d553c4972b55bf8e3d80b16f245e5bb38f28d80b91ca4f9f90c09a6c28d`  
		Last Modified: Thu, 12 Jan 2023 03:48:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97054b77b205167acd5a303c8aa82e380f090ff4e2ded81d3425ec78500139d`  
		Last Modified: Thu, 12 Jan 2023 03:48:14 GMT  
		Size: 25.5 MB (25470784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e150d9e1a1da09e17313cb3b6358d2f16cf2919c51e9addf30500de9d03292ef`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c0d792e2a7942826a61fdc26b6081ab404122751ff4f4dd8f5b8b0eca21399`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 324.5 KB (324466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd89ac843c0479ae40ca8c747e8a676229754549dbfeb9fe7157fdf1a60e685f`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0892c7d4de38540a99ca06e09c0a995b2e119c5ae853eadc2f7558f69bf44bb1`  
		Last Modified: Tue, 14 Feb 2023 20:56:57 GMT  
		Size: 157.8 MB (157805981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b2ec2bef689e3f934369ec3ebb90a5b06c0cbd77b2364e23a776b4da7a68f5`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066daab446064e42a798fe1592cbb9befd18dc7c368cc287f403168c17647f44`  
		Last Modified: Tue, 14 Feb 2023 21:18:46 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ea7fb211a6a6bdf1db9842354942dfaf3dc66bb87b9ce2b1620b897655022d`  
		Last Modified: Tue, 14 Feb 2023 21:18:44 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1a9f71a17b653aeea9897c2da8205709b77073460fc648f6daa323ffffee8d`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53678f100709f21522f2dd0732c10bbb5a70107fa9a4fcdd4895786c68d0bb27`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a973e4e836b19e1ccb3104f7458b2ed9a0aee58d697b6b7a8f7b8800265560f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:53 GMT  
		Size: 1.6 MB (1641852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9b2ad53ca032d7a1d8ef1944923a40be2d6c2fbd4945695a1d7cf5ea708613`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-builder` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:8208748738c8ad71587dbe2fa710487d6ed5a1ef462b3591e30be906145cab13
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1572172924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c99c2ba8e5059d5dc3ad70afada06d399bff99be54c4c7bf3908b0889a8719a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 02:57:40 GMT
ENV GIT_VERSION=2.23.0
# Thu, 12 Jan 2023 02:57:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 12 Jan 2023 02:57:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 12 Jan 2023 02:57:42 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 12 Jan 2023 02:58:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 02:58:23 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 02:58:47 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Feb 2023 20:31:21 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 20:34:49 GMT
RUN $url = 'https://dl.google.com/go/go1.19.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8d84af29e46c38b1eec77f9310310517c9e394ac7489e1c7329a94b443b0388d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Feb 2023 20:34:51 GMT
WORKDIR C:\go
# Tue, 14 Feb 2023 21:17:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 21:17:18 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:20:52 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:20:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:21:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Feb 2023 19:21:22 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2fc8728d9c7bf65edf893fd902f8b1bd780f93623858960c9db79e39922b169`  
		Last Modified: Thu, 12 Jan 2023 03:47:24 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7935a4c648078e79f67a11bcd5908e251110dd6c5a4ee49a607f332dd25af9`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d257f8b122044547f89f00f58661b25aca97c92f3831e7aaa11975639b6e35d4`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95acaa75c1852ba1320c5db382b01f587badb615b6746b59be27eedcf96ab667`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5201ba65043fa621c187729f18aecf4c549cdfa12cd6d8cab7a901d893f3a8a8`  
		Last Modified: Thu, 12 Jan 2023 03:47:29 GMT  
		Size: 25.7 MB (25702230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a317a349bca5ab28ba7c1ce039928a56390f7e7a8d7ddec07efcc1c9883e5d`  
		Last Modified: Thu, 12 Jan 2023 03:47:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8850296b8fbb853a6eb6341f7484cd4bc622e9f679f12c4123eddf08b7f398fb`  
		Last Modified: Thu, 12 Jan 2023 03:47:18 GMT  
		Size: 554.2 KB (554212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b724dc103b7bd177436e0035a2c0eaffd1187dcb978222f4e7c1014ca50ee`  
		Last Modified: Tue, 14 Feb 2023 20:55:01 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f4ea18edcbbc3120e8b270d76ae1a1876db9d493e1b703d25194e08b0896c`  
		Last Modified: Tue, 14 Feb 2023 20:55:55 GMT  
		Size: 158.0 MB (158000355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81da76ff355cb5fcac2247f23ca1fe8dd4256b41f2edd58b34f886fcb74bc6e7`  
		Last Modified: Tue, 14 Feb 2023 20:55:01 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc05ca820f63f78de074bd0a9ffe6889c8e3405b0563cf21ef5013179b8f407`  
		Last Modified: Tue, 14 Feb 2023 21:19:03 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b911bfee9062064c2f989b2acf01493bb3c9ad5989eb456277dfe272c1dcd2`  
		Last Modified: Tue, 14 Feb 2023 21:19:01 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aa3117c7e54c9d38a6d368beb815482c58bd46981294fc7c45046ca02b8d34`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710d1b3e32dd905f2dc2f33df9481f9abdd52cbd0028eadd5d0517fe673c3de1`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df812b30f4c795624a0ff09a18f3ac73987de268d9ee1aa080998e222a6f6e3`  
		Last Modified: Wed, 15 Feb 2023 20:18:10 GMT  
		Size: 1.9 MB (1868549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced4b40932769c58cc0b5348fdc7b4189892820c655d4029b988aafd8692dcd0`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6.4-builder-alpine`

```console
$ docker pull caddy@sha256:ef81823d12a3d4befb8d3dc29929c37f003682cc6a9cc8a7e8ed08442fc2644a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.6.4-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:47722ffc694507be1e2f34ca172e292fb5e226ea68d87871300b9d65f543fcce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131421587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4674ac67a52f4d29bc8349e9dcca7db8393d778c97c79d9e2f6e997603a99cd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 08:21:54 GMT
RUN apk add --no-cache ca-certificates
# Sat, 11 Feb 2023 08:21:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:24:10 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:25:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:25:43 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:25:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:25:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:25:44 GMT
WORKDIR /go
# Tue, 14 Feb 2023 19:47:10 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 19:47:10 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:19:27 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:19:28 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 19:19:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 19:19:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 19:19:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d21d5440ebff5aaaaeb115a003f7a4a3897f1866a87de95bc4a21436fc563c`  
		Last Modified: Sat, 11 Feb 2023 08:29:10 GMT  
		Size: 284.8 KB (284816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f790f4c5274f100158d4c23bc5eddf659c1fe93ef4025488f9493d88f1490d88`  
		Last Modified: Tue, 14 Feb 2023 19:31:12 GMT  
		Size: 122.4 MB (122355677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bf170fd9e6726c86c0d4b478d9ec522e82c527a8e708668f48233a4d03f618`  
		Last Modified: Tue, 14 Feb 2023 19:30:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a5d1c1b6ed103f8c7f97c73ed546ff7e767b10473b55c15c0d4e1a13a69481`  
		Last Modified: Tue, 14 Feb 2023 19:47:34 GMT  
		Size: 4.2 MB (4188243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0130eaa2f0b1f7646719d82927743bd84c83ed450eb8be4db5327d280d5e4d0`  
		Last Modified: Wed, 15 Feb 2023 19:20:05 GMT  
		Size: 1.2 MB (1217841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab1f57409241476a86d26944527bc2c6c3903eadb21221b8d96da52120b3109`  
		Last Modified: Wed, 15 Feb 2023 19:20:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ef43980c42cd8a35929f0378a7ecd1918acd54140264da387b01dc7e3d6bea0b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127437368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd812dbbfb10d2a70518b9169ed3ed8f3e00b43a8b7ce2f98f7e72b09d33330`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:49:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 21:49:23 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:54:56 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:57:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:57:12 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:57:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:57:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:57:13 GMT
WORKDIR /go
# Tue, 14 Feb 2023 21:22:55 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 21:22:55 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:49:33 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:49:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:49:33 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:49:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:49:35 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:49:35 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11114cba5e5d7175bb4d5b434db94e1c2bf0f8263c6cf2b8cbf3c1fc853114b5`  
		Last Modified: Fri, 10 Feb 2023 22:00:04 GMT  
		Size: 286.1 KB (286119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbe98122be79c40d67ce24806b19f5bd6a2f3025a18faa3a9e07c836eda77a3`  
		Last Modified: Tue, 14 Feb 2023 20:03:20 GMT  
		Size: 118.7 MB (118722534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2006a6001995de26a92cbdcc7917c763ee43c1f153331e17ed59bc706622a4`  
		Last Modified: Tue, 14 Feb 2023 20:02:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241e307a6c2a59713b29a4001892e4737b03b8bdc797f283f8bfef8e5976a360`  
		Last Modified: Tue, 14 Feb 2023 21:23:46 GMT  
		Size: 4.2 MB (4151224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd6d861ad1e103851af9cad05cca9ddd82af819c16eef77a788212eb48a451a`  
		Last Modified: Wed, 15 Feb 2023 18:50:44 GMT  
		Size: 1.2 MB (1166072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff6cca8082ff38bb36e60b71883dc986b05c54b1322ffe5c5906933155af3db`  
		Last Modified: Wed, 15 Feb 2023 18:50:44 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ae944139e672dc9c4065b2e83f98a2c2522db0397a33f3b287e771e01c90b043
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126518789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b5e54b6cc5a620df577f3659a5f2415b1ab88786c0ee932fd73c5c026786cb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 23:34:00 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 23:34:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 22:43:55 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 22:46:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 22:46:04 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 22:46:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 22:46:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 22:46:05 GMT
WORKDIR /go
# Wed, 15 Feb 2023 01:37:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 15 Feb 2023 01:37:44 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:57:37 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:57:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:57:37 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:57:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:57:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ee22df4e0527c9d317c1729808b4fc333083ad4d5a41645d79beabb64e9415`  
		Last Modified: Fri, 10 Feb 2023 23:50:08 GMT  
		Size: 285.4 KB (285353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0083f2e9af62d9a5b5bcf25401158f3ebb34f9fe9e7e951a52b22e9f6a15f1ed`  
		Last Modified: Tue, 14 Feb 2023 22:54:26 GMT  
		Size: 118.5 MB (118480449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6506d85184bedd4e64bb66e1357511d9dde4bc32c2c99d3183c2cec84f20e7e5`  
		Last Modified: Tue, 14 Feb 2023 22:54:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc4386697a4bb55f0e63b324c4a0b444eec215aff0cffc35d7affc50fff2041`  
		Last Modified: Wed, 15 Feb 2023 01:38:34 GMT  
		Size: 3.7 MB (3720630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03d748e87e34207a999297a575c405a0c36bf6b02a35f1c1b370ae25d1daf26`  
		Last Modified: Wed, 15 Feb 2023 18:58:45 GMT  
		Size: 1.2 MB (1163331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957e61fda37fb7df272efba4e6f8cd0083db173bff77b1e4dbbfad3fba3cd92b`  
		Last Modified: Wed, 15 Feb 2023 18:58:44 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:345963f3560e208ac6bacd024a578f5b7e01f8b734c723eddee3617aa9f0eb48
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125824793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e4189a65557b7e2dd531761f337fa9ebac950fe19c378297b031b64ef548d7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:38:33 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:38:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:43:03 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:44:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:44:06 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:44:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:44:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:44:07 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:05:45 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:05:45 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:39:25 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:39:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:39:26 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:39:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:39:28 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:39:28 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55522c79112429742fe76c795b9509c5cd1e8198e0caa2a1e355c0e60a719576`  
		Last Modified: Fri, 10 Feb 2023 22:44:19 GMT  
		Size: 286.3 KB (286257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a025c151a25ec079b20475bc7d9114a55273ff4768db3589c2a9e3556263ff`  
		Last Modified: Tue, 14 Feb 2023 19:48:57 GMT  
		Size: 116.9 MB (116917630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e172ed32e80e014974dc5c64a3cec7ac2d456fe4b21179f48138df590112cdab`  
		Last Modified: Tue, 14 Feb 2023 19:48:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbab95e946333dfac53de76b5f4cfc1f90fec80107055af4eb888824c147950`  
		Last Modified: Tue, 14 Feb 2023 20:06:09 GMT  
		Size: 4.2 MB (4234639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52ae4d010a784b362566e543eeacafbef900440cdda0b182dc5ea51a53b070c`  
		Last Modified: Wed, 15 Feb 2023 18:40:08 GMT  
		Size: 1.1 MB (1123743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d9033ce04f11b49957c7855096c7e5ed4a4e3ad840dd150fc0823b230b3742`  
		Last Modified: Wed, 15 Feb 2023 18:40:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:8126a0d2b7cc9613f70b6b5375c14cc61dfca5dc1b83adc5be33efab8eacc69f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126579575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da1cd24f35f4106a8a7176a2f2b5656a22982a1787b9204d3eaab9ec535ef58`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:36 GMT
ADD file:ec037a0d4b462d12963ac20d9ec49bb73b4bcaf84d4bc7b364ebf93667e585b0 in / 
# Fri, 10 Feb 2023 21:20:36 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:40:13 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:40:14 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:46:09 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:48:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:48:44 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:48:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:48:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:48:46 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:12:48 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:12:48 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:16:53 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:16:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:16:54 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 19:16:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 19:16:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 19:16:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:aa3c56f9c6f127b6c8f628c95db165741ca400d19bdaef2752d80f093e47451e`  
		Last Modified: Fri, 10 Feb 2023 21:21:37 GMT  
		Size: 3.4 MB (3390750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788962e1689dbb14c760601cbf633ae350e98e3a045f8010924cd585de6b6a3e`  
		Last Modified: Fri, 10 Feb 2023 22:53:32 GMT  
		Size: 286.6 KB (286645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ae39b9ad00c218f9156f0958fa48f3062eb5830b791b8592e5f25fd576c7c5`  
		Last Modified: Tue, 14 Feb 2023 19:56:18 GMT  
		Size: 117.3 MB (117316160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f3bf55d586b31bb5c97f2cbf5167fd359b61336f93bed839c2f4de055ced88`  
		Last Modified: Tue, 14 Feb 2023 19:55:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e012d53123423a5fe128ab31d41596d83d8e48699ad608e9eb58dd0b2322fe0`  
		Last Modified: Tue, 14 Feb 2023 20:13:35 GMT  
		Size: 4.5 MB (4479556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90177e6cf58218f094608b8401f41d0da78a0cf57d95718e48e8c6e2f77c6fae`  
		Last Modified: Wed, 15 Feb 2023 19:18:00 GMT  
		Size: 1.1 MB (1105899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e897949e5a46b09b4606d86b20ecb5684cb43f7e1bed1f208ee9b7e93d208c`  
		Last Modified: Wed, 15 Feb 2023 19:17:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:777aec044ded48957652f0c6ceac314892e1c892c85a07084f80762791aa55b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129606877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4f36416ff115d90097fe1378fca1a1ded179a50ee13701194f1193833e1d5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:25 GMT
ADD file:03b2fb4d732a294329449ff55c5d84f7d2735e6510985718979469994f3a607b in / 
# Fri, 10 Feb 2023 21:41:26 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:27:44 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:27:44 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:47:34 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:49:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:49:23 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:49:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:49:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:49:24 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:12:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:12:32 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:42:20 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:42:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:42:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:42:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:42:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:42:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:24c4f8de3549a39c64b0edc2cfa68769b373f35138d0f13725100160bb32d4e2`  
		Last Modified: Fri, 10 Feb 2023 21:42:16 GMT  
		Size: 3.2 MB (3175116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affa53ed2f1b70a83e3a15cae881ca47cd40f6ac11060717cdbbd4e405f9d586`  
		Last Modified: Fri, 10 Feb 2023 22:37:18 GMT  
		Size: 285.0 KB (285032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafa18be4ff892e2222424e6e25c36c21c4d94825607e8b840d2384c6ab73651`  
		Last Modified: Tue, 14 Feb 2023 19:54:27 GMT  
		Size: 120.8 MB (120811850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c3965c085d018b012055d834e6c56402c39a086413f83eb42fed0eba26be6`  
		Last Modified: Tue, 14 Feb 2023 19:54:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250c53f2b7534f15112393341635149f8ad756241a7c7979ec7ad6fbd3959ff1`  
		Last Modified: Tue, 14 Feb 2023 20:13:22 GMT  
		Size: 4.2 MB (4163882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11288ef421d5fc2fc1e1a7cd7350fb7f4ad371aa6edad42bb5ffa8f95cb2f2bc`  
		Last Modified: Wed, 15 Feb 2023 18:43:31 GMT  
		Size: 1.2 MB (1170432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b792196575b477b3bd73841238a0c4445026bc982b5e0236ef24a59eec4875`  
		Last Modified: Wed, 15 Feb 2023 18:43:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6.4-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:e4b4bb126038410035c8c6962d643dbf73d0b1d8ee3108c4f005238402a9a0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `caddy:2.6.4-builder-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:bff20886c4e50c2ff56c65ce2b8b2f6f861b63544087ebc9828b8283abf3e9ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1893205034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9666c08cd03c61fe14a234d3f8760533430f35e891dccd0f5540cb34fd9834a4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 03:01:55 GMT
ENV GIT_VERSION=2.23.0
# Thu, 12 Jan 2023 03:01:56 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 12 Jan 2023 03:01:57 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 12 Jan 2023 03:01:58 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 12 Jan 2023 03:02:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 03:03:01 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 03:03:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Feb 2023 20:35:10 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 20:39:32 GMT
RUN $url = 'https://dl.google.com/go/go1.19.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8d84af29e46c38b1eec77f9310310517c9e394ac7489e1c7329a94b443b0388d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Feb 2023 20:39:34 GMT
WORKDIR C:\go
# Tue, 14 Feb 2023 21:16:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 21:16:10 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:20:04 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:20:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Feb 2023 19:20:39 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203425975bec1802428fad91a2e5f01172b161062c12eddf729e548bf7e134e0`  
		Last Modified: Thu, 12 Jan 2023 03:48:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80e42e19ab862b4adea06f1995e1f5cbb2c11ad8d68ae4a7bb5d0da5d0e6f38`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be5d5df8cec6d1386f78a342668c3d2cb809372865459c1b35aa8d5a39a463b`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e467d553c4972b55bf8e3d80b16f245e5bb38f28d80b91ca4f9f90c09a6c28d`  
		Last Modified: Thu, 12 Jan 2023 03:48:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97054b77b205167acd5a303c8aa82e380f090ff4e2ded81d3425ec78500139d`  
		Last Modified: Thu, 12 Jan 2023 03:48:14 GMT  
		Size: 25.5 MB (25470784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e150d9e1a1da09e17313cb3b6358d2f16cf2919c51e9addf30500de9d03292ef`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c0d792e2a7942826a61fdc26b6081ab404122751ff4f4dd8f5b8b0eca21399`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 324.5 KB (324466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd89ac843c0479ae40ca8c747e8a676229754549dbfeb9fe7157fdf1a60e685f`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0892c7d4de38540a99ca06e09c0a995b2e119c5ae853eadc2f7558f69bf44bb1`  
		Last Modified: Tue, 14 Feb 2023 20:56:57 GMT  
		Size: 157.8 MB (157805981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b2ec2bef689e3f934369ec3ebb90a5b06c0cbd77b2364e23a776b4da7a68f5`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066daab446064e42a798fe1592cbb9befd18dc7c368cc287f403168c17647f44`  
		Last Modified: Tue, 14 Feb 2023 21:18:46 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ea7fb211a6a6bdf1db9842354942dfaf3dc66bb87b9ce2b1620b897655022d`  
		Last Modified: Tue, 14 Feb 2023 21:18:44 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1a9f71a17b653aeea9897c2da8205709b77073460fc648f6daa323ffffee8d`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53678f100709f21522f2dd0732c10bbb5a70107fa9a4fcdd4895786c68d0bb27`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a973e4e836b19e1ccb3104f7458b2ed9a0aee58d697b6b7a8f7b8800265560f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:53 GMT  
		Size: 1.6 MB (1641852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9b2ad53ca032d7a1d8ef1944923a40be2d6c2fbd4945695a1d7cf5ea708613`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6.4-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:8bfb22a6d9ad624ddad733879370d4e05a82cc5c15125cdc2365e8f7a4fe79e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `caddy:2.6.4-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:8208748738c8ad71587dbe2fa710487d6ed5a1ef462b3591e30be906145cab13
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1572172924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c99c2ba8e5059d5dc3ad70afada06d399bff99be54c4c7bf3908b0889a8719a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 02:57:40 GMT
ENV GIT_VERSION=2.23.0
# Thu, 12 Jan 2023 02:57:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 12 Jan 2023 02:57:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 12 Jan 2023 02:57:42 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 12 Jan 2023 02:58:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 02:58:23 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 02:58:47 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Feb 2023 20:31:21 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 20:34:49 GMT
RUN $url = 'https://dl.google.com/go/go1.19.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8d84af29e46c38b1eec77f9310310517c9e394ac7489e1c7329a94b443b0388d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Feb 2023 20:34:51 GMT
WORKDIR C:\go
# Tue, 14 Feb 2023 21:17:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 21:17:18 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:20:52 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:20:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:21:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Feb 2023 19:21:22 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2fc8728d9c7bf65edf893fd902f8b1bd780f93623858960c9db79e39922b169`  
		Last Modified: Thu, 12 Jan 2023 03:47:24 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7935a4c648078e79f67a11bcd5908e251110dd6c5a4ee49a607f332dd25af9`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d257f8b122044547f89f00f58661b25aca97c92f3831e7aaa11975639b6e35d4`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95acaa75c1852ba1320c5db382b01f587badb615b6746b59be27eedcf96ab667`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5201ba65043fa621c187729f18aecf4c549cdfa12cd6d8cab7a901d893f3a8a8`  
		Last Modified: Thu, 12 Jan 2023 03:47:29 GMT  
		Size: 25.7 MB (25702230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a317a349bca5ab28ba7c1ce039928a56390f7e7a8d7ddec07efcc1c9883e5d`  
		Last Modified: Thu, 12 Jan 2023 03:47:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8850296b8fbb853a6eb6341f7484cd4bc622e9f679f12c4123eddf08b7f398fb`  
		Last Modified: Thu, 12 Jan 2023 03:47:18 GMT  
		Size: 554.2 KB (554212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b724dc103b7bd177436e0035a2c0eaffd1187dcb978222f4e7c1014ca50ee`  
		Last Modified: Tue, 14 Feb 2023 20:55:01 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f4ea18edcbbc3120e8b270d76ae1a1876db9d493e1b703d25194e08b0896c`  
		Last Modified: Tue, 14 Feb 2023 20:55:55 GMT  
		Size: 158.0 MB (158000355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81da76ff355cb5fcac2247f23ca1fe8dd4256b41f2edd58b34f886fcb74bc6e7`  
		Last Modified: Tue, 14 Feb 2023 20:55:01 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc05ca820f63f78de074bd0a9ffe6889c8e3405b0563cf21ef5013179b8f407`  
		Last Modified: Tue, 14 Feb 2023 21:19:03 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b911bfee9062064c2f989b2acf01493bb3c9ad5989eb456277dfe272c1dcd2`  
		Last Modified: Tue, 14 Feb 2023 21:19:01 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aa3117c7e54c9d38a6d368beb815482c58bd46981294fc7c45046ca02b8d34`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710d1b3e32dd905f2dc2f33df9481f9abdd52cbd0028eadd5d0517fe673c3de1`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df812b30f4c795624a0ff09a18f3ac73987de268d9ee1aa080998e222a6f6e3`  
		Last Modified: Wed, 15 Feb 2023 20:18:10 GMT  
		Size: 1.9 MB (1868549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced4b40932769c58cc0b5348fdc7b4189892820c655d4029b988aafd8692dcd0`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6.4-windowsservercore`

```console
$ docker pull caddy@sha256:a0e880f407bc812d350d220b76e5e9da56ef9a34384f075923fb0eacfc9eef27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.3887; amd64
	-	windows version 10.0.20348.1487; amd64

### `caddy:2.6.4-windowsservercore` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:371255c187169392f30d7caf1e65b8a8708afbdd8520eb74df9c38d973195766
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723380167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa79dce896513046be66642ea60c82eaf2266ff5533f3e8c40a79c7b779c0eca`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:16:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:15:47 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:17:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:17:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:17:11 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:17:12 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:17:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:17:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:17:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:17:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:17:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:17:20 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:17:21 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:17:22 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:17:24 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:17:43 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:17:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47af8a9c9ef8e49d65e53dd207ad0935ce7a2b50b2f253e6a5b037494ae19d0a`  
		Last Modified: Thu, 09 Feb 2023 01:16:50 GMT  
		Size: 401.5 KB (401472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d742cb3ca192278158c048ecc9f358855bc8f2629af70c62b9610a1fc66bbf0a`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859ce744a498d8f5affa0958dae6a0027cd48925c7c0bdf78214019c927eb34b`  
		Last Modified: Wed, 15 Feb 2023 20:17:06 GMT  
		Size: 14.7 MB (14694270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64525df3f764c2e65e711fbd328781c61243029c264aca6b09309e584dbb69b3`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231e1956368caba27b753959bf1fb5d38cf0e798477a45110f2691b063809554`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405677c240161263f0ca900ffca71596061f8d59668d524a80f16957c120f0c`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638a2e8fc9bd411f13b7b5a8b82272fd39024ac9b711d2bc73c28c39314fc3bb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1b8ca9045f120e19c22debd19df59f42aa442b84c073c7cfc2f5a2d0f463cb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c7468bd4bec28c11efd397d435df6a129ffc73265d2d2c4162bb121a336d08`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de41f5feb06b95a77601b9fd09ab7409b567e0d9684c46dfcdc4a067a00adc`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab6a97db0980bf9c94414bfb713b5db0ed7bec52a805303782c4309a6e9f62b`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41271d7026e5d15682fc59b1ac99ac0a67909c591ea0c7ab0885207386064744`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b605f7b22df792b7b41d97cec04cbfb795ba3588fd9e0b44363147a7a02820`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c2c11f6f75de707c6475d6248a27eb983282648b0a923c47e2894db7304e0d`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48461b499cb5763190c69d134f0b96625458bdd69fe78a15ade15efbad156033`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745ffdaac1ecada0622ef6d6ccfe6140992921240b91567821b96a07a72df8b8`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf9895ba16206d3ebb35a3a6e3f615542102d00230528158c62eee814428521`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc57c33625ddac815d78d81c0feb25f7dd3d6ea9f6d4f6238024e4898a15ef3c`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 316.4 KB (316447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31243cdae7d3d8bcf0b00d6c6c0a1f4ec3c2c277ca964f747f8acc133cef56a2`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.6.4-windowsservercore` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:0722e548c2efb29869e87e89dc7cf03de8d31fe33c28e9e61a33f018b0a7a3e4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1401943529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a230b066a2fbe8bdfee6749b8afe9b1655260bb3643408c49082c8754a4cff75`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:18:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:18:03 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:19:13 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:19:14 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:19:15 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:24 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:26 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:27 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:46 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:19:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42eb48143612ee855d99c932e324b1bd035c60554117edeaa805402060613c51`  
		Last Modified: Thu, 09 Feb 2023 01:17:17 GMT  
		Size: 635.9 KB (635943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e120c0944228b4b6623b958c83433bc43f104b64cecccbd1ac7ab250e7a68db7`  
		Last Modified: Wed, 15 Feb 2023 20:17:30 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891cca6ce816bbe4dd40bd862cae84155f0da6f7f13ab15fb80f92c471772be7`  
		Last Modified: Wed, 15 Feb 2023 20:17:34 GMT  
		Size: 14.9 MB (14907106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e4718f6f1c46191ed75eaff08ff294c5ad0f384309aca914d5687324213f83`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0edcd24848e16049bee383e4ae89134f9d07da6079deed1398df66ad8a401ac`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b890b1c144cd00660796b630f5a2b8009a7c8b98a852cc4e645d13d84f4b48`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12054588e533ec29d2f174499ee24489e7b6d7b8527337dcdcc25a6ec29973`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e7efe9a5a718b562e89379f47cd1c2919b05c52ad1a2ceb9525d7f98f2f0d1`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fc39bc9c2bdee1444bb0e46b53cb55da0913be6b115f95bc50f5ed370138e`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d17482a1fa64018a51f2d8467fb3cba2c11aae5e67a689612e314d713ca8b0`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4843586865795ebb5e828c5f7fe6c9f829f9b12d5ad2e0bbf9f302874fc39a27`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd44712296ac1e7d28147c40159638788a75b58c17764de2757fcfda62f5551a`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5344aa95ac41ce0d03e95ae47d07c9ddef532b47bbfeb871053e69eacf5429a6`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf50f2a8532ee01e411b12116a827c2823a5cb2ee71091b4b724c44b6ba0f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b71f209c61027e4688f4e4b109ec883c187ed74b3d4c27e4b11596a4f20a07`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df052fc38d64efbb8657dd2c40cfa28c56f1137efcf1d7751277c1c81626b39e`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266955548153e827efba631ef21036116d523e11f332aae3910c4e6b773896f5`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59f15231c2a3b500e116b42a5254f441985197b1d364bc46a71cd917af38ec9`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 347.4 KB (347422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4a927a917a632a25082f22d95b2df35568f4522d622efe890c6d57457ed461`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6.4-windowsservercore-1809`

```console
$ docker pull caddy@sha256:9b3fc2e9403b99a6fce9d5b94de587e848616342ccad9275d8bbead1a4b8f1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `caddy:2.6.4-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:371255c187169392f30d7caf1e65b8a8708afbdd8520eb74df9c38d973195766
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723380167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa79dce896513046be66642ea60c82eaf2266ff5533f3e8c40a79c7b779c0eca`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:16:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:15:47 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:17:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:17:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:17:11 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:17:12 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:17:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:17:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:17:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:17:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:17:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:17:20 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:17:21 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:17:22 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:17:24 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:17:43 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:17:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47af8a9c9ef8e49d65e53dd207ad0935ce7a2b50b2f253e6a5b037494ae19d0a`  
		Last Modified: Thu, 09 Feb 2023 01:16:50 GMT  
		Size: 401.5 KB (401472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d742cb3ca192278158c048ecc9f358855bc8f2629af70c62b9610a1fc66bbf0a`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859ce744a498d8f5affa0958dae6a0027cd48925c7c0bdf78214019c927eb34b`  
		Last Modified: Wed, 15 Feb 2023 20:17:06 GMT  
		Size: 14.7 MB (14694270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64525df3f764c2e65e711fbd328781c61243029c264aca6b09309e584dbb69b3`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231e1956368caba27b753959bf1fb5d38cf0e798477a45110f2691b063809554`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405677c240161263f0ca900ffca71596061f8d59668d524a80f16957c120f0c`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638a2e8fc9bd411f13b7b5a8b82272fd39024ac9b711d2bc73c28c39314fc3bb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1b8ca9045f120e19c22debd19df59f42aa442b84c073c7cfc2f5a2d0f463cb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c7468bd4bec28c11efd397d435df6a129ffc73265d2d2c4162bb121a336d08`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de41f5feb06b95a77601b9fd09ab7409b567e0d9684c46dfcdc4a067a00adc`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab6a97db0980bf9c94414bfb713b5db0ed7bec52a805303782c4309a6e9f62b`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41271d7026e5d15682fc59b1ac99ac0a67909c591ea0c7ab0885207386064744`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b605f7b22df792b7b41d97cec04cbfb795ba3588fd9e0b44363147a7a02820`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c2c11f6f75de707c6475d6248a27eb983282648b0a923c47e2894db7304e0d`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48461b499cb5763190c69d134f0b96625458bdd69fe78a15ade15efbad156033`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745ffdaac1ecada0622ef6d6ccfe6140992921240b91567821b96a07a72df8b8`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf9895ba16206d3ebb35a3a6e3f615542102d00230528158c62eee814428521`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc57c33625ddac815d78d81c0feb25f7dd3d6ea9f6d4f6238024e4898a15ef3c`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 316.4 KB (316447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31243cdae7d3d8bcf0b00d6c6c0a1f4ec3c2c277ca964f747f8acc133cef56a2`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.6.4-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:113f187a1100da96770eeaecc6e118b4be7ef33cb4d01611de3e3045ed3a4acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `caddy:2.6.4-windowsservercore-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:0722e548c2efb29869e87e89dc7cf03de8d31fe33c28e9e61a33f018b0a7a3e4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1401943529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a230b066a2fbe8bdfee6749b8afe9b1655260bb3643408c49082c8754a4cff75`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:18:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:18:03 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:19:13 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:19:14 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:19:15 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:24 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:26 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:27 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:46 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:19:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42eb48143612ee855d99c932e324b1bd035c60554117edeaa805402060613c51`  
		Last Modified: Thu, 09 Feb 2023 01:17:17 GMT  
		Size: 635.9 KB (635943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e120c0944228b4b6623b958c83433bc43f104b64cecccbd1ac7ab250e7a68db7`  
		Last Modified: Wed, 15 Feb 2023 20:17:30 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891cca6ce816bbe4dd40bd862cae84155f0da6f7f13ab15fb80f92c471772be7`  
		Last Modified: Wed, 15 Feb 2023 20:17:34 GMT  
		Size: 14.9 MB (14907106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e4718f6f1c46191ed75eaff08ff294c5ad0f384309aca914d5687324213f83`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0edcd24848e16049bee383e4ae89134f9d07da6079deed1398df66ad8a401ac`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b890b1c144cd00660796b630f5a2b8009a7c8b98a852cc4e645d13d84f4b48`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12054588e533ec29d2f174499ee24489e7b6d7b8527337dcdcc25a6ec29973`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e7efe9a5a718b562e89379f47cd1c2919b05c52ad1a2ceb9525d7f98f2f0d1`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fc39bc9c2bdee1444bb0e46b53cb55da0913be6b115f95bc50f5ed370138e`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d17482a1fa64018a51f2d8467fb3cba2c11aae5e67a689612e314d713ca8b0`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4843586865795ebb5e828c5f7fe6c9f829f9b12d5ad2e0bbf9f302874fc39a27`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd44712296ac1e7d28147c40159638788a75b58c17764de2757fcfda62f5551a`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5344aa95ac41ce0d03e95ae47d07c9ddef532b47bbfeb871053e69eacf5429a6`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf50f2a8532ee01e411b12116a827c2823a5cb2ee71091b4b724c44b6ba0f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b71f209c61027e4688f4e4b109ec883c187ed74b3d4c27e4b11596a4f20a07`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df052fc38d64efbb8657dd2c40cfa28c56f1137efcf1d7751277c1c81626b39e`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266955548153e827efba631ef21036116d523e11f332aae3910c4e6b773896f5`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59f15231c2a3b500e116b42a5254f441985197b1d364bc46a71cd917af38ec9`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 347.4 KB (347422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4a927a917a632a25082f22d95b2df35568f4522d622efe890c6d57457ed461`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:alpine`

```console
$ docker pull caddy@sha256:aacae65cfdcf61777306cf7c131fb968f67bb7fab8dfd683aa073e8b99867e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:alpine` - linux; amd64

```console
$ docker pull caddy@sha256:36ba71b44afa613ecf0aadce8e4b9e3f56e0c4b0a78c8edf4e8c2485f21b35ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17449113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8464e23f16f9a82426bbdc3ac8c94270a84453ddc86b9147505a2378a7c2fd0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:38:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 11 Feb 2023 07:38:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 19:19:21 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 19:19:23 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 19:19:24 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:25 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 19:19:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e3e797818bc929d95bae8220b7b6034b559c217ef5bf622dc7fedc8d270a48`  
		Last Modified: Sat, 11 Feb 2023 07:39:01 GMT  
		Size: 351.2 KB (351178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cebb4c80b3906a9b751ee9a512c1581331b1fd691c84f575c01a29e28403dde`  
		Last Modified: Sat, 11 Feb 2023 07:39:00 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90648ba22c191b969d8db393bf6138e7d6ecc1b70b3865d1717ec4d663192d89`  
		Last Modified: Wed, 15 Feb 2023 19:19:52 GMT  
		Size: 14.3 MB (14282621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5b39c4c37396031351c9753e4c7df6f2114d0ef588953b97c668d0ec7e2f1e50
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16582274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ffa8388ed5f7f62ab116b850faa63ff3214dea5fb007a77196a8efd0023832`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:28:54 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 21:28:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:49:22 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:49:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:49:26 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:49:26 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:49:27 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:49:28 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:49:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a400dcba29ff44f8e5bf01493def4f19629aca6d103cb2a66ca87c457f7414`  
		Last Modified: Fri, 10 Feb 2023 21:29:47 GMT  
		Size: 345.8 KB (345811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b946768825eb5ed2fc6f932fdb0b0c552f4c35c39dada07eddd70ce4a535953`  
		Last Modified: Fri, 10 Feb 2023 21:29:47 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f11ff5bb8d752ef2e91afa46770077fd62ddc9e78f280c00e796bf841c9d49f`  
		Last Modified: Wed, 15 Feb 2023 18:50:25 GMT  
		Size: 13.6 MB (13612205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:21302c9acb44ea61fccba3ef765712da93fede2d928aaafc8f7bd77a35d91953
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16365562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600d5193b2ba5875b66a6579717ec1aab50be117445a5a657045572141d1187c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:37 GMT
ADD file:193f48d48ed2e90a0e81663757e372f59806151c17e82113f03443db0ef723c3 in / 
# Fri, 10 Feb 2023 21:51:37 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:37:19 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:37:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:57:27 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:57:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:57:30 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:57:30 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:57:31 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:57:32 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:beefe5ad637c7db32e6afc68103fc4e779630219979216a625338ab55f7d191c`  
		Last Modified: Fri, 10 Feb 2023 21:52:51 GMT  
		Size: 2.4 MB (2420494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2ab4edb1f0a14b28a55f050d62d8e54111075639a0fa8f173448814ba0d00`  
		Last Modified: Fri, 10 Feb 2023 22:38:25 GMT  
		Size: 342.6 KB (342588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0580184dd0082f009564a7a3923731f202cbe4bd8b857dbca2c77da8e7434815`  
		Last Modified: Fri, 10 Feb 2023 22:38:25 GMT  
		Size: 7.5 KB (7479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8682e09bc231d5c9076b76cb92cb3b1185b870277da03dbd7e87d7981ff6147a`  
		Last Modified: Wed, 15 Feb 2023 18:58:28 GMT  
		Size: 13.6 MB (13595001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:6c2623f6bf30798be5c37fc7484e45ecc288d493fb657883f59ddb27ed714ad8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16130997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a38afdc517ef4cff6b6b51a1c6a633c2826599b07feb1e88380d0f783e35cf1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:00:35 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:00:37 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:39:20 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:39:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:39:22 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:39:22 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:39:23 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:39:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70730e8e2fb933ec157ec87f2a4fb4ad45e8e578b8f7c76cc4846631d773554`  
		Last Modified: Fri, 10 Feb 2023 22:01:02 GMT  
		Size: 350.2 KB (350153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a4b7390d269477c225f1d03e825d2d8bdf6b4d87b5f7bb8811b341e56b7d36`  
		Last Modified: Fri, 10 Feb 2023 22:01:02 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2743d2ef53ee6edb0e39c89bf16957e3a00990410b2d1a126dca1b2d196182`  
		Last Modified: Wed, 15 Feb 2023 18:39:53 GMT  
		Size: 13.1 MB (13063787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:8861ab3ae3d0c180e38142c2f7482f9ce1773419eb29ed9d6d18308246858093
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15955172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5819f0ab4928a30c29293a27299a3b44371cd3bd97df91432ef7b3f43b692d8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:13:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:13:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 19:16:26 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:16:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 19:16:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 19:16:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 19:16:42 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:16:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:16:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:16:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:16:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:16:47 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:16:47 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 19:16:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782bd0321e6539bb7dac8574fd36bad22059ef06bb63dc842165f69d0a821572`  
		Last Modified: Fri, 10 Feb 2023 22:14:16 GMT  
		Size: 363.1 KB (363088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb806b2600b0209a73fc7175ab778d0224661034b2f722bd1a0aec1eb9eabe3d`  
		Last Modified: Fri, 10 Feb 2023 22:14:15 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd7c8ae860931dd79dea76d33bc21bb11d89cd4d133cdb41078b040afc6633e`  
		Last Modified: Wed, 15 Feb 2023 19:17:41 GMT  
		Size: 12.8 MB (12779898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:4e1ed99f133abf02d6a7c77849978bb621f748e18c9cb9f7a1dbf88480ddb8d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16792756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45cd164da734310b788dcbd4f6c94bccff6e48705fe4d42ecca07a54e9459a9c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:14:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:41:48 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:41:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:41:59 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:41:59 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:42:00 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:42:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:42:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:42:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:42:03 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:42:04 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:42:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:42:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:42:05 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:42:06 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:42:07 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:42:07 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:42:08 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:42:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e6ec82400496ce74e37120e1655955b79303daaa5b8ca7e956e3cd96ddd6e9`  
		Last Modified: Fri, 10 Feb 2023 22:15:05 GMT  
		Size: 352.8 KB (352801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5b992687f93ced3715ad97bd95ab37daef5685b784e195209caefbc48f14e9`  
		Last Modified: Fri, 10 Feb 2023 22:15:05 GMT  
		Size: 7.6 KB (7557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccc40924ce2df3343fa5465a92ccaa4ed80e0883190a99d3f468c60f9ddbcf8`  
		Last Modified: Wed, 15 Feb 2023 18:43:19 GMT  
		Size: 13.8 MB (13838817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:f3ac019c2a9615cd1adc2555d81ba8eb0412bfea8c34290fc0adfc7d77a468e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.3887; amd64
	-	windows version 10.0.20348.1487; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:47722ffc694507be1e2f34ca172e292fb5e226ea68d87871300b9d65f543fcce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131421587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4674ac67a52f4d29bc8349e9dcca7db8393d778c97c79d9e2f6e997603a99cd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 08:21:54 GMT
RUN apk add --no-cache ca-certificates
# Sat, 11 Feb 2023 08:21:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:24:10 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:25:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:25:43 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:25:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:25:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:25:44 GMT
WORKDIR /go
# Tue, 14 Feb 2023 19:47:10 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 19:47:10 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:19:27 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:19:28 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 19:19:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 19:19:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 19:19:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d21d5440ebff5aaaaeb115a003f7a4a3897f1866a87de95bc4a21436fc563c`  
		Last Modified: Sat, 11 Feb 2023 08:29:10 GMT  
		Size: 284.8 KB (284816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f790f4c5274f100158d4c23bc5eddf659c1fe93ef4025488f9493d88f1490d88`  
		Last Modified: Tue, 14 Feb 2023 19:31:12 GMT  
		Size: 122.4 MB (122355677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bf170fd9e6726c86c0d4b478d9ec522e82c527a8e708668f48233a4d03f618`  
		Last Modified: Tue, 14 Feb 2023 19:30:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a5d1c1b6ed103f8c7f97c73ed546ff7e767b10473b55c15c0d4e1a13a69481`  
		Last Modified: Tue, 14 Feb 2023 19:47:34 GMT  
		Size: 4.2 MB (4188243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0130eaa2f0b1f7646719d82927743bd84c83ed450eb8be4db5327d280d5e4d0`  
		Last Modified: Wed, 15 Feb 2023 19:20:05 GMT  
		Size: 1.2 MB (1217841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab1f57409241476a86d26944527bc2c6c3903eadb21221b8d96da52120b3109`  
		Last Modified: Wed, 15 Feb 2023 19:20:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ef43980c42cd8a35929f0378a7ecd1918acd54140264da387b01dc7e3d6bea0b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127437368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd812dbbfb10d2a70518b9169ed3ed8f3e00b43a8b7ce2f98f7e72b09d33330`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:49:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 21:49:23 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:54:56 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:57:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:57:12 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:57:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:57:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:57:13 GMT
WORKDIR /go
# Tue, 14 Feb 2023 21:22:55 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 21:22:55 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:49:33 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:49:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:49:33 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:49:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:49:35 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:49:35 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11114cba5e5d7175bb4d5b434db94e1c2bf0f8263c6cf2b8cbf3c1fc853114b5`  
		Last Modified: Fri, 10 Feb 2023 22:00:04 GMT  
		Size: 286.1 KB (286119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbe98122be79c40d67ce24806b19f5bd6a2f3025a18faa3a9e07c836eda77a3`  
		Last Modified: Tue, 14 Feb 2023 20:03:20 GMT  
		Size: 118.7 MB (118722534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2006a6001995de26a92cbdcc7917c763ee43c1f153331e17ed59bc706622a4`  
		Last Modified: Tue, 14 Feb 2023 20:02:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241e307a6c2a59713b29a4001892e4737b03b8bdc797f283f8bfef8e5976a360`  
		Last Modified: Tue, 14 Feb 2023 21:23:46 GMT  
		Size: 4.2 MB (4151224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd6d861ad1e103851af9cad05cca9ddd82af819c16eef77a788212eb48a451a`  
		Last Modified: Wed, 15 Feb 2023 18:50:44 GMT  
		Size: 1.2 MB (1166072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff6cca8082ff38bb36e60b71883dc986b05c54b1322ffe5c5906933155af3db`  
		Last Modified: Wed, 15 Feb 2023 18:50:44 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ae944139e672dc9c4065b2e83f98a2c2522db0397a33f3b287e771e01c90b043
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126518789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b5e54b6cc5a620df577f3659a5f2415b1ab88786c0ee932fd73c5c026786cb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 23:34:00 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 23:34:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 22:43:55 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 22:46:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 22:46:04 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 22:46:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 22:46:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 22:46:05 GMT
WORKDIR /go
# Wed, 15 Feb 2023 01:37:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 15 Feb 2023 01:37:44 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:57:37 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:57:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:57:37 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:57:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:57:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ee22df4e0527c9d317c1729808b4fc333083ad4d5a41645d79beabb64e9415`  
		Last Modified: Fri, 10 Feb 2023 23:50:08 GMT  
		Size: 285.4 KB (285353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0083f2e9af62d9a5b5bcf25401158f3ebb34f9fe9e7e951a52b22e9f6a15f1ed`  
		Last Modified: Tue, 14 Feb 2023 22:54:26 GMT  
		Size: 118.5 MB (118480449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6506d85184bedd4e64bb66e1357511d9dde4bc32c2c99d3183c2cec84f20e7e5`  
		Last Modified: Tue, 14 Feb 2023 22:54:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc4386697a4bb55f0e63b324c4a0b444eec215aff0cffc35d7affc50fff2041`  
		Last Modified: Wed, 15 Feb 2023 01:38:34 GMT  
		Size: 3.7 MB (3720630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03d748e87e34207a999297a575c405a0c36bf6b02a35f1c1b370ae25d1daf26`  
		Last Modified: Wed, 15 Feb 2023 18:58:45 GMT  
		Size: 1.2 MB (1163331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957e61fda37fb7df272efba4e6f8cd0083db173bff77b1e4dbbfad3fba3cd92b`  
		Last Modified: Wed, 15 Feb 2023 18:58:44 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:345963f3560e208ac6bacd024a578f5b7e01f8b734c723eddee3617aa9f0eb48
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125824793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e4189a65557b7e2dd531761f337fa9ebac950fe19c378297b031b64ef548d7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:38:33 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:38:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:43:03 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:44:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:44:06 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:44:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:44:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:44:07 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:05:45 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:05:45 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:39:25 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:39:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:39:26 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:39:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:39:28 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:39:28 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55522c79112429742fe76c795b9509c5cd1e8198e0caa2a1e355c0e60a719576`  
		Last Modified: Fri, 10 Feb 2023 22:44:19 GMT  
		Size: 286.3 KB (286257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a025c151a25ec079b20475bc7d9114a55273ff4768db3589c2a9e3556263ff`  
		Last Modified: Tue, 14 Feb 2023 19:48:57 GMT  
		Size: 116.9 MB (116917630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e172ed32e80e014974dc5c64a3cec7ac2d456fe4b21179f48138df590112cdab`  
		Last Modified: Tue, 14 Feb 2023 19:48:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbab95e946333dfac53de76b5f4cfc1f90fec80107055af4eb888824c147950`  
		Last Modified: Tue, 14 Feb 2023 20:06:09 GMT  
		Size: 4.2 MB (4234639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52ae4d010a784b362566e543eeacafbef900440cdda0b182dc5ea51a53b070c`  
		Last Modified: Wed, 15 Feb 2023 18:40:08 GMT  
		Size: 1.1 MB (1123743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d9033ce04f11b49957c7855096c7e5ed4a4e3ad840dd150fc0823b230b3742`  
		Last Modified: Wed, 15 Feb 2023 18:40:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:8126a0d2b7cc9613f70b6b5375c14cc61dfca5dc1b83adc5be33efab8eacc69f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126579575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da1cd24f35f4106a8a7176a2f2b5656a22982a1787b9204d3eaab9ec535ef58`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:36 GMT
ADD file:ec037a0d4b462d12963ac20d9ec49bb73b4bcaf84d4bc7b364ebf93667e585b0 in / 
# Fri, 10 Feb 2023 21:20:36 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:40:13 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:40:14 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:46:09 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:48:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:48:44 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:48:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:48:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:48:46 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:12:48 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:12:48 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:16:53 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:16:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:16:54 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 19:16:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 19:16:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 19:16:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:aa3c56f9c6f127b6c8f628c95db165741ca400d19bdaef2752d80f093e47451e`  
		Last Modified: Fri, 10 Feb 2023 21:21:37 GMT  
		Size: 3.4 MB (3390750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788962e1689dbb14c760601cbf633ae350e98e3a045f8010924cd585de6b6a3e`  
		Last Modified: Fri, 10 Feb 2023 22:53:32 GMT  
		Size: 286.6 KB (286645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ae39b9ad00c218f9156f0958fa48f3062eb5830b791b8592e5f25fd576c7c5`  
		Last Modified: Tue, 14 Feb 2023 19:56:18 GMT  
		Size: 117.3 MB (117316160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f3bf55d586b31bb5c97f2cbf5167fd359b61336f93bed839c2f4de055ced88`  
		Last Modified: Tue, 14 Feb 2023 19:55:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e012d53123423a5fe128ab31d41596d83d8e48699ad608e9eb58dd0b2322fe0`  
		Last Modified: Tue, 14 Feb 2023 20:13:35 GMT  
		Size: 4.5 MB (4479556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90177e6cf58218f094608b8401f41d0da78a0cf57d95718e48e8c6e2f77c6fae`  
		Last Modified: Wed, 15 Feb 2023 19:18:00 GMT  
		Size: 1.1 MB (1105899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e897949e5a46b09b4606d86b20ecb5684cb43f7e1bed1f208ee9b7e93d208c`  
		Last Modified: Wed, 15 Feb 2023 19:17:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:777aec044ded48957652f0c6ceac314892e1c892c85a07084f80762791aa55b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129606877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4f36416ff115d90097fe1378fca1a1ded179a50ee13701194f1193833e1d5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:25 GMT
ADD file:03b2fb4d732a294329449ff55c5d84f7d2735e6510985718979469994f3a607b in / 
# Fri, 10 Feb 2023 21:41:26 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:27:44 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:27:44 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:47:34 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:49:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:49:23 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:49:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:49:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:49:24 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:12:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:12:32 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:42:20 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:42:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:42:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:42:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:42:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:42:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:24c4f8de3549a39c64b0edc2cfa68769b373f35138d0f13725100160bb32d4e2`  
		Last Modified: Fri, 10 Feb 2023 21:42:16 GMT  
		Size: 3.2 MB (3175116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affa53ed2f1b70a83e3a15cae881ca47cd40f6ac11060717cdbbd4e405f9d586`  
		Last Modified: Fri, 10 Feb 2023 22:37:18 GMT  
		Size: 285.0 KB (285032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafa18be4ff892e2222424e6e25c36c21c4d94825607e8b840d2384c6ab73651`  
		Last Modified: Tue, 14 Feb 2023 19:54:27 GMT  
		Size: 120.8 MB (120811850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c3965c085d018b012055d834e6c56402c39a086413f83eb42fed0eba26be6`  
		Last Modified: Tue, 14 Feb 2023 19:54:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250c53f2b7534f15112393341635149f8ad756241a7c7979ec7ad6fbd3959ff1`  
		Last Modified: Tue, 14 Feb 2023 20:13:22 GMT  
		Size: 4.2 MB (4163882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11288ef421d5fc2fc1e1a7cd7350fb7f4ad371aa6edad42bb5ffa8f95cb2f2bc`  
		Last Modified: Wed, 15 Feb 2023 18:43:31 GMT  
		Size: 1.2 MB (1170432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b792196575b477b3bd73841238a0c4445026bc982b5e0236ef24a59eec4875`  
		Last Modified: Wed, 15 Feb 2023 18:43:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:bff20886c4e50c2ff56c65ce2b8b2f6f861b63544087ebc9828b8283abf3e9ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1893205034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9666c08cd03c61fe14a234d3f8760533430f35e891dccd0f5540cb34fd9834a4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 03:01:55 GMT
ENV GIT_VERSION=2.23.0
# Thu, 12 Jan 2023 03:01:56 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 12 Jan 2023 03:01:57 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 12 Jan 2023 03:01:58 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 12 Jan 2023 03:02:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 03:03:01 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 03:03:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Feb 2023 20:35:10 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 20:39:32 GMT
RUN $url = 'https://dl.google.com/go/go1.19.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8d84af29e46c38b1eec77f9310310517c9e394ac7489e1c7329a94b443b0388d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Feb 2023 20:39:34 GMT
WORKDIR C:\go
# Tue, 14 Feb 2023 21:16:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 21:16:10 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:20:04 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:20:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Feb 2023 19:20:39 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203425975bec1802428fad91a2e5f01172b161062c12eddf729e548bf7e134e0`  
		Last Modified: Thu, 12 Jan 2023 03:48:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80e42e19ab862b4adea06f1995e1f5cbb2c11ad8d68ae4a7bb5d0da5d0e6f38`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be5d5df8cec6d1386f78a342668c3d2cb809372865459c1b35aa8d5a39a463b`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e467d553c4972b55bf8e3d80b16f245e5bb38f28d80b91ca4f9f90c09a6c28d`  
		Last Modified: Thu, 12 Jan 2023 03:48:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97054b77b205167acd5a303c8aa82e380f090ff4e2ded81d3425ec78500139d`  
		Last Modified: Thu, 12 Jan 2023 03:48:14 GMT  
		Size: 25.5 MB (25470784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e150d9e1a1da09e17313cb3b6358d2f16cf2919c51e9addf30500de9d03292ef`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c0d792e2a7942826a61fdc26b6081ab404122751ff4f4dd8f5b8b0eca21399`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 324.5 KB (324466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd89ac843c0479ae40ca8c747e8a676229754549dbfeb9fe7157fdf1a60e685f`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0892c7d4de38540a99ca06e09c0a995b2e119c5ae853eadc2f7558f69bf44bb1`  
		Last Modified: Tue, 14 Feb 2023 20:56:57 GMT  
		Size: 157.8 MB (157805981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b2ec2bef689e3f934369ec3ebb90a5b06c0cbd77b2364e23a776b4da7a68f5`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066daab446064e42a798fe1592cbb9befd18dc7c368cc287f403168c17647f44`  
		Last Modified: Tue, 14 Feb 2023 21:18:46 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ea7fb211a6a6bdf1db9842354942dfaf3dc66bb87b9ce2b1620b897655022d`  
		Last Modified: Tue, 14 Feb 2023 21:18:44 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1a9f71a17b653aeea9897c2da8205709b77073460fc648f6daa323ffffee8d`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53678f100709f21522f2dd0732c10bbb5a70107fa9a4fcdd4895786c68d0bb27`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a973e4e836b19e1ccb3104f7458b2ed9a0aee58d697b6b7a8f7b8800265560f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:53 GMT  
		Size: 1.6 MB (1641852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9b2ad53ca032d7a1d8ef1944923a40be2d6c2fbd4945695a1d7cf5ea708613`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:8208748738c8ad71587dbe2fa710487d6ed5a1ef462b3591e30be906145cab13
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1572172924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c99c2ba8e5059d5dc3ad70afada06d399bff99be54c4c7bf3908b0889a8719a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 02:57:40 GMT
ENV GIT_VERSION=2.23.0
# Thu, 12 Jan 2023 02:57:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 12 Jan 2023 02:57:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 12 Jan 2023 02:57:42 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 12 Jan 2023 02:58:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 02:58:23 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 02:58:47 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Feb 2023 20:31:21 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 20:34:49 GMT
RUN $url = 'https://dl.google.com/go/go1.19.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8d84af29e46c38b1eec77f9310310517c9e394ac7489e1c7329a94b443b0388d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Feb 2023 20:34:51 GMT
WORKDIR C:\go
# Tue, 14 Feb 2023 21:17:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 21:17:18 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:20:52 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:20:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:21:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Feb 2023 19:21:22 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2fc8728d9c7bf65edf893fd902f8b1bd780f93623858960c9db79e39922b169`  
		Last Modified: Thu, 12 Jan 2023 03:47:24 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7935a4c648078e79f67a11bcd5908e251110dd6c5a4ee49a607f332dd25af9`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d257f8b122044547f89f00f58661b25aca97c92f3831e7aaa11975639b6e35d4`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95acaa75c1852ba1320c5db382b01f587badb615b6746b59be27eedcf96ab667`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5201ba65043fa621c187729f18aecf4c549cdfa12cd6d8cab7a901d893f3a8a8`  
		Last Modified: Thu, 12 Jan 2023 03:47:29 GMT  
		Size: 25.7 MB (25702230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a317a349bca5ab28ba7c1ce039928a56390f7e7a8d7ddec07efcc1c9883e5d`  
		Last Modified: Thu, 12 Jan 2023 03:47:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8850296b8fbb853a6eb6341f7484cd4bc622e9f679f12c4123eddf08b7f398fb`  
		Last Modified: Thu, 12 Jan 2023 03:47:18 GMT  
		Size: 554.2 KB (554212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b724dc103b7bd177436e0035a2c0eaffd1187dcb978222f4e7c1014ca50ee`  
		Last Modified: Tue, 14 Feb 2023 20:55:01 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f4ea18edcbbc3120e8b270d76ae1a1876db9d493e1b703d25194e08b0896c`  
		Last Modified: Tue, 14 Feb 2023 20:55:55 GMT  
		Size: 158.0 MB (158000355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81da76ff355cb5fcac2247f23ca1fe8dd4256b41f2edd58b34f886fcb74bc6e7`  
		Last Modified: Tue, 14 Feb 2023 20:55:01 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc05ca820f63f78de074bd0a9ffe6889c8e3405b0563cf21ef5013179b8f407`  
		Last Modified: Tue, 14 Feb 2023 21:19:03 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b911bfee9062064c2f989b2acf01493bb3c9ad5989eb456277dfe272c1dcd2`  
		Last Modified: Tue, 14 Feb 2023 21:19:01 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aa3117c7e54c9d38a6d368beb815482c58bd46981294fc7c45046ca02b8d34`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710d1b3e32dd905f2dc2f33df9481f9abdd52cbd0028eadd5d0517fe673c3de1`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df812b30f4c795624a0ff09a18f3ac73987de268d9ee1aa080998e222a6f6e3`  
		Last Modified: Wed, 15 Feb 2023 20:18:10 GMT  
		Size: 1.9 MB (1868549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced4b40932769c58cc0b5348fdc7b4189892820c655d4029b988aafd8692dcd0`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:ef81823d12a3d4befb8d3dc29929c37f003682cc6a9cc8a7e8ed08442fc2644a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:47722ffc694507be1e2f34ca172e292fb5e226ea68d87871300b9d65f543fcce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131421587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4674ac67a52f4d29bc8349e9dcca7db8393d778c97c79d9e2f6e997603a99cd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 08:21:54 GMT
RUN apk add --no-cache ca-certificates
# Sat, 11 Feb 2023 08:21:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:24:10 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:25:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:25:43 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:25:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:25:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:25:44 GMT
WORKDIR /go
# Tue, 14 Feb 2023 19:47:10 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 19:47:10 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:19:27 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:19:28 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 19:19:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 19:19:29 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 19:19:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d21d5440ebff5aaaaeb115a003f7a4a3897f1866a87de95bc4a21436fc563c`  
		Last Modified: Sat, 11 Feb 2023 08:29:10 GMT  
		Size: 284.8 KB (284816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f790f4c5274f100158d4c23bc5eddf659c1fe93ef4025488f9493d88f1490d88`  
		Last Modified: Tue, 14 Feb 2023 19:31:12 GMT  
		Size: 122.4 MB (122355677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bf170fd9e6726c86c0d4b478d9ec522e82c527a8e708668f48233a4d03f618`  
		Last Modified: Tue, 14 Feb 2023 19:30:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a5d1c1b6ed103f8c7f97c73ed546ff7e767b10473b55c15c0d4e1a13a69481`  
		Last Modified: Tue, 14 Feb 2023 19:47:34 GMT  
		Size: 4.2 MB (4188243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0130eaa2f0b1f7646719d82927743bd84c83ed450eb8be4db5327d280d5e4d0`  
		Last Modified: Wed, 15 Feb 2023 19:20:05 GMT  
		Size: 1.2 MB (1217841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab1f57409241476a86d26944527bc2c6c3903eadb21221b8d96da52120b3109`  
		Last Modified: Wed, 15 Feb 2023 19:20:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ef43980c42cd8a35929f0378a7ecd1918acd54140264da387b01dc7e3d6bea0b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127437368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd812dbbfb10d2a70518b9169ed3ed8f3e00b43a8b7ce2f98f7e72b09d33330`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:49:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 21:49:23 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:54:56 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:57:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:57:12 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:57:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:57:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:57:13 GMT
WORKDIR /go
# Tue, 14 Feb 2023 21:22:55 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 21:22:55 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:49:33 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:49:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:49:33 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:49:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:49:35 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:49:35 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11114cba5e5d7175bb4d5b434db94e1c2bf0f8263c6cf2b8cbf3c1fc853114b5`  
		Last Modified: Fri, 10 Feb 2023 22:00:04 GMT  
		Size: 286.1 KB (286119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbe98122be79c40d67ce24806b19f5bd6a2f3025a18faa3a9e07c836eda77a3`  
		Last Modified: Tue, 14 Feb 2023 20:03:20 GMT  
		Size: 118.7 MB (118722534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2006a6001995de26a92cbdcc7917c763ee43c1f153331e17ed59bc706622a4`  
		Last Modified: Tue, 14 Feb 2023 20:02:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241e307a6c2a59713b29a4001892e4737b03b8bdc797f283f8bfef8e5976a360`  
		Last Modified: Tue, 14 Feb 2023 21:23:46 GMT  
		Size: 4.2 MB (4151224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd6d861ad1e103851af9cad05cca9ddd82af819c16eef77a788212eb48a451a`  
		Last Modified: Wed, 15 Feb 2023 18:50:44 GMT  
		Size: 1.2 MB (1166072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff6cca8082ff38bb36e60b71883dc986b05c54b1322ffe5c5906933155af3db`  
		Last Modified: Wed, 15 Feb 2023 18:50:44 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ae944139e672dc9c4065b2e83f98a2c2522db0397a33f3b287e771e01c90b043
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126518789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b5e54b6cc5a620df577f3659a5f2415b1ab88786c0ee932fd73c5c026786cb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 23:34:00 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 23:34:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 22:43:55 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 22:46:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 22:46:04 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 22:46:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 22:46:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 22:46:05 GMT
WORKDIR /go
# Wed, 15 Feb 2023 01:37:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 15 Feb 2023 01:37:44 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:57:37 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:57:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:57:37 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:57:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:57:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ee22df4e0527c9d317c1729808b4fc333083ad4d5a41645d79beabb64e9415`  
		Last Modified: Fri, 10 Feb 2023 23:50:08 GMT  
		Size: 285.4 KB (285353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0083f2e9af62d9a5b5bcf25401158f3ebb34f9fe9e7e951a52b22e9f6a15f1ed`  
		Last Modified: Tue, 14 Feb 2023 22:54:26 GMT  
		Size: 118.5 MB (118480449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6506d85184bedd4e64bb66e1357511d9dde4bc32c2c99d3183c2cec84f20e7e5`  
		Last Modified: Tue, 14 Feb 2023 22:54:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc4386697a4bb55f0e63b324c4a0b444eec215aff0cffc35d7affc50fff2041`  
		Last Modified: Wed, 15 Feb 2023 01:38:34 GMT  
		Size: 3.7 MB (3720630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03d748e87e34207a999297a575c405a0c36bf6b02a35f1c1b370ae25d1daf26`  
		Last Modified: Wed, 15 Feb 2023 18:58:45 GMT  
		Size: 1.2 MB (1163331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957e61fda37fb7df272efba4e6f8cd0083db173bff77b1e4dbbfad3fba3cd92b`  
		Last Modified: Wed, 15 Feb 2023 18:58:44 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:345963f3560e208ac6bacd024a578f5b7e01f8b734c723eddee3617aa9f0eb48
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125824793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e4189a65557b7e2dd531761f337fa9ebac950fe19c378297b031b64ef548d7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:38:33 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:38:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:43:03 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:44:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:44:06 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:44:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:44:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:44:07 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:05:45 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:05:45 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:39:25 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:39:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:39:26 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:39:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:39:28 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:39:28 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55522c79112429742fe76c795b9509c5cd1e8198e0caa2a1e355c0e60a719576`  
		Last Modified: Fri, 10 Feb 2023 22:44:19 GMT  
		Size: 286.3 KB (286257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a025c151a25ec079b20475bc7d9114a55273ff4768db3589c2a9e3556263ff`  
		Last Modified: Tue, 14 Feb 2023 19:48:57 GMT  
		Size: 116.9 MB (116917630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e172ed32e80e014974dc5c64a3cec7ac2d456fe4b21179f48138df590112cdab`  
		Last Modified: Tue, 14 Feb 2023 19:48:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbab95e946333dfac53de76b5f4cfc1f90fec80107055af4eb888824c147950`  
		Last Modified: Tue, 14 Feb 2023 20:06:09 GMT  
		Size: 4.2 MB (4234639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52ae4d010a784b362566e543eeacafbef900440cdda0b182dc5ea51a53b070c`  
		Last Modified: Wed, 15 Feb 2023 18:40:08 GMT  
		Size: 1.1 MB (1123743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d9033ce04f11b49957c7855096c7e5ed4a4e3ad840dd150fc0823b230b3742`  
		Last Modified: Wed, 15 Feb 2023 18:40:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:8126a0d2b7cc9613f70b6b5375c14cc61dfca5dc1b83adc5be33efab8eacc69f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126579575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da1cd24f35f4106a8a7176a2f2b5656a22982a1787b9204d3eaab9ec535ef58`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:36 GMT
ADD file:ec037a0d4b462d12963ac20d9ec49bb73b4bcaf84d4bc7b364ebf93667e585b0 in / 
# Fri, 10 Feb 2023 21:20:36 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:40:13 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:40:14 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:46:09 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:48:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:48:44 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:48:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:48:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:48:46 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:12:48 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:12:48 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:16:53 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:16:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:16:54 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 19:16:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 19:16:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 19:16:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:aa3c56f9c6f127b6c8f628c95db165741ca400d19bdaef2752d80f093e47451e`  
		Last Modified: Fri, 10 Feb 2023 21:21:37 GMT  
		Size: 3.4 MB (3390750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788962e1689dbb14c760601cbf633ae350e98e3a045f8010924cd585de6b6a3e`  
		Last Modified: Fri, 10 Feb 2023 22:53:32 GMT  
		Size: 286.6 KB (286645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ae39b9ad00c218f9156f0958fa48f3062eb5830b791b8592e5f25fd576c7c5`  
		Last Modified: Tue, 14 Feb 2023 19:56:18 GMT  
		Size: 117.3 MB (117316160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f3bf55d586b31bb5c97f2cbf5167fd359b61336f93bed839c2f4de055ced88`  
		Last Modified: Tue, 14 Feb 2023 19:55:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e012d53123423a5fe128ab31d41596d83d8e48699ad608e9eb58dd0b2322fe0`  
		Last Modified: Tue, 14 Feb 2023 20:13:35 GMT  
		Size: 4.5 MB (4479556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90177e6cf58218f094608b8401f41d0da78a0cf57d95718e48e8c6e2f77c6fae`  
		Last Modified: Wed, 15 Feb 2023 19:18:00 GMT  
		Size: 1.1 MB (1105899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e897949e5a46b09b4606d86b20ecb5684cb43f7e1bed1f208ee9b7e93d208c`  
		Last Modified: Wed, 15 Feb 2023 19:17:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:777aec044ded48957652f0c6ceac314892e1c892c85a07084f80762791aa55b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129606877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4f36416ff115d90097fe1378fca1a1ded179a50ee13701194f1193833e1d5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:25 GMT
ADD file:03b2fb4d732a294329449ff55c5d84f7d2735e6510985718979469994f3a607b in / 
# Fri, 10 Feb 2023 21:41:26 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:27:44 GMT
RUN apk add --no-cache ca-certificates
# Fri, 10 Feb 2023 22:27:44 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:47:34 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 19:49:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.6.src.tar.gz'; 		sha256='d7f0013f82e6d7f862cc6cb5c8cdb48eef5f2e239b35baa97e2f1a7466043767'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 14 Feb 2023 19:49:23 GMT
ENV GOPATH=/go
# Tue, 14 Feb 2023 19:49:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Feb 2023 19:49:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 14 Feb 2023 19:49:24 GMT
WORKDIR /go
# Tue, 14 Feb 2023 20:12:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 14 Feb 2023 20:12:32 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 18:42:20 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:42:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 18:42:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Feb 2023 18:42:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='2538d080f065cf1c5a41c9c14dd6acd55783e004c7ea3fdd6e1bc07c4d846a85b78d5de1111391fda71d48cad9d542a0741593e5b25ea9826faaee74577d8a98' ;; 		armhf)   binArch='armv6'; checksum='5bd99dfc28d867253275c2a6753425a1e8445385449cd5414c8bb14fdf7b513f468c69e0ae8ba431cf4b5e2b5f77666dda2a6811fbe8a1718cae377387319b36' ;; 		armv7)   binArch='armv7'; checksum='e8ea697bcbe029c81ce183b5ec44d095d8919f62a7170a0697dd7531d5a87c980b9aac1442638bf4dee1e60abe0ad698dfa56bed222fe9329ff274f5973f12fe' ;; 		aarch64) binArch='arm64'; checksum='afbf26528c4238a7d6eaa375c1367d213f7d3359e97193b996a896b89fb852531d33581b8cef6432bd866d1488f5f98ed43a198732c45d5b9d008eb9316d36ab' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='519e8d7575507e49ddd7d58d168c6223802b94a8954284956db4b72133bf3027de03f9bfc0dc578373ebcb49d668a140fcd54d90888c17cdbbef6ab182a8b511' ;; 		s390x)   binArch='s390x'; checksum='b95078a4231acd54bd56c70d110709c9e290089200855c9448259621c983fa5ecfa925a1e6ab59459750bc6abb936422433543b6079fa547dea4dc08d5daabf9' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 15 Feb 2023 18:42:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 15 Feb 2023 18:42:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:24c4f8de3549a39c64b0edc2cfa68769b373f35138d0f13725100160bb32d4e2`  
		Last Modified: Fri, 10 Feb 2023 21:42:16 GMT  
		Size: 3.2 MB (3175116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affa53ed2f1b70a83e3a15cae881ca47cd40f6ac11060717cdbbd4e405f9d586`  
		Last Modified: Fri, 10 Feb 2023 22:37:18 GMT  
		Size: 285.0 KB (285032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafa18be4ff892e2222424e6e25c36c21c4d94825607e8b840d2384c6ab73651`  
		Last Modified: Tue, 14 Feb 2023 19:54:27 GMT  
		Size: 120.8 MB (120811850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c3965c085d018b012055d834e6c56402c39a086413f83eb42fed0eba26be6`  
		Last Modified: Tue, 14 Feb 2023 19:54:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250c53f2b7534f15112393341635149f8ad756241a7c7979ec7ad6fbd3959ff1`  
		Last Modified: Tue, 14 Feb 2023 20:13:22 GMT  
		Size: 4.2 MB (4163882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11288ef421d5fc2fc1e1a7cd7350fb7f4ad371aa6edad42bb5ffa8f95cb2f2bc`  
		Last Modified: Wed, 15 Feb 2023 18:43:31 GMT  
		Size: 1.2 MB (1170432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b792196575b477b3bd73841238a0c4445026bc982b5e0236ef24a59eec4875`  
		Last Modified: Wed, 15 Feb 2023 18:43:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:e4b4bb126038410035c8c6962d643dbf73d0b1d8ee3108c4f005238402a9a0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:bff20886c4e50c2ff56c65ce2b8b2f6f861b63544087ebc9828b8283abf3e9ea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1893205034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9666c08cd03c61fe14a234d3f8760533430f35e891dccd0f5540cb34fd9834a4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 03:01:55 GMT
ENV GIT_VERSION=2.23.0
# Thu, 12 Jan 2023 03:01:56 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 12 Jan 2023 03:01:57 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 12 Jan 2023 03:01:58 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 12 Jan 2023 03:02:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 03:03:01 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 03:03:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Feb 2023 20:35:10 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 20:39:32 GMT
RUN $url = 'https://dl.google.com/go/go1.19.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8d84af29e46c38b1eec77f9310310517c9e394ac7489e1c7329a94b443b0388d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Feb 2023 20:39:34 GMT
WORKDIR C:\go
# Tue, 14 Feb 2023 21:16:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 21:16:10 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:20:04 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:20:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Feb 2023 19:20:39 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203425975bec1802428fad91a2e5f01172b161062c12eddf729e548bf7e134e0`  
		Last Modified: Thu, 12 Jan 2023 03:48:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80e42e19ab862b4adea06f1995e1f5cbb2c11ad8d68ae4a7bb5d0da5d0e6f38`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be5d5df8cec6d1386f78a342668c3d2cb809372865459c1b35aa8d5a39a463b`  
		Last Modified: Thu, 12 Jan 2023 03:48:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e467d553c4972b55bf8e3d80b16f245e5bb38f28d80b91ca4f9f90c09a6c28d`  
		Last Modified: Thu, 12 Jan 2023 03:48:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97054b77b205167acd5a303c8aa82e380f090ff4e2ded81d3425ec78500139d`  
		Last Modified: Thu, 12 Jan 2023 03:48:14 GMT  
		Size: 25.5 MB (25470784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e150d9e1a1da09e17313cb3b6358d2f16cf2919c51e9addf30500de9d03292ef`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c0d792e2a7942826a61fdc26b6081ab404122751ff4f4dd8f5b8b0eca21399`  
		Last Modified: Thu, 12 Jan 2023 03:48:03 GMT  
		Size: 324.5 KB (324466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd89ac843c0479ae40ca8c747e8a676229754549dbfeb9fe7157fdf1a60e685f`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0892c7d4de38540a99ca06e09c0a995b2e119c5ae853eadc2f7558f69bf44bb1`  
		Last Modified: Tue, 14 Feb 2023 20:56:57 GMT  
		Size: 157.8 MB (157805981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b2ec2bef689e3f934369ec3ebb90a5b06c0cbd77b2364e23a776b4da7a68f5`  
		Last Modified: Tue, 14 Feb 2023 20:56:05 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066daab446064e42a798fe1592cbb9befd18dc7c368cc287f403168c17647f44`  
		Last Modified: Tue, 14 Feb 2023 21:18:46 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ea7fb211a6a6bdf1db9842354942dfaf3dc66bb87b9ce2b1620b897655022d`  
		Last Modified: Tue, 14 Feb 2023 21:18:44 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1a9f71a17b653aeea9897c2da8205709b77073460fc648f6daa323ffffee8d`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53678f100709f21522f2dd0732c10bbb5a70107fa9a4fcdd4895786c68d0bb27`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a973e4e836b19e1ccb3104f7458b2ed9a0aee58d697b6b7a8f7b8800265560f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:53 GMT  
		Size: 1.6 MB (1641852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9b2ad53ca032d7a1d8ef1944923a40be2d6c2fbd4945695a1d7cf5ea708613`  
		Last Modified: Wed, 15 Feb 2023 20:17:52 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:8bfb22a6d9ad624ddad733879370d4e05a82cc5c15125cdc2365e8f7a4fe79e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:8208748738c8ad71587dbe2fa710487d6ed5a1ef462b3591e30be906145cab13
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1572172924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c99c2ba8e5059d5dc3ad70afada06d399bff99be54c4c7bf3908b0889a8719a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 02:57:40 GMT
ENV GIT_VERSION=2.23.0
# Thu, 12 Jan 2023 02:57:41 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 12 Jan 2023 02:57:42 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 12 Jan 2023 02:57:42 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 12 Jan 2023 02:58:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 12 Jan 2023 02:58:23 GMT
ENV GOPATH=C:\go
# Thu, 12 Jan 2023 02:58:47 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Feb 2023 20:31:21 GMT
ENV GOLANG_VERSION=1.19.6
# Tue, 14 Feb 2023 20:34:49 GMT
RUN $url = 'https://dl.google.com/go/go1.19.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '8d84af29e46c38b1eec77f9310310517c9e394ac7489e1c7329a94b443b0388d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Feb 2023 20:34:51 GMT
WORKDIR C:\go
# Tue, 14 Feb 2023 21:17:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 21:17:18 GMT
ENV XCADDY_VERSION=v0.3.2
# Wed, 15 Feb 2023 19:20:52 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:20:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Feb 2023 19:21:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.2/xcaddy_0.3.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8de1cb65e555e8d7f1124d384904cd53a37d1914106af6ec1cef92f1975bd66b5a1f0e066c2c6b68c85d67de54d52f170f539dff117ce97f4166d8e984a728ba')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Feb 2023 19:21:22 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2fc8728d9c7bf65edf893fd902f8b1bd780f93623858960c9db79e39922b169`  
		Last Modified: Thu, 12 Jan 2023 03:47:24 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7935a4c648078e79f67a11bcd5908e251110dd6c5a4ee49a607f332dd25af9`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d257f8b122044547f89f00f58661b25aca97c92f3831e7aaa11975639b6e35d4`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95acaa75c1852ba1320c5db382b01f587badb615b6746b59be27eedcf96ab667`  
		Last Modified: Thu, 12 Jan 2023 03:47:20 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5201ba65043fa621c187729f18aecf4c549cdfa12cd6d8cab7a901d893f3a8a8`  
		Last Modified: Thu, 12 Jan 2023 03:47:29 GMT  
		Size: 25.7 MB (25702230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a317a349bca5ab28ba7c1ce039928a56390f7e7a8d7ddec07efcc1c9883e5d`  
		Last Modified: Thu, 12 Jan 2023 03:47:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8850296b8fbb853a6eb6341f7484cd4bc622e9f679f12c4123eddf08b7f398fb`  
		Last Modified: Thu, 12 Jan 2023 03:47:18 GMT  
		Size: 554.2 KB (554212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81b724dc103b7bd177436e0035a2c0eaffd1187dcb978222f4e7c1014ca50ee`  
		Last Modified: Tue, 14 Feb 2023 20:55:01 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7f4ea18edcbbc3120e8b270d76ae1a1876db9d493e1b703d25194e08b0896c`  
		Last Modified: Tue, 14 Feb 2023 20:55:55 GMT  
		Size: 158.0 MB (158000355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81da76ff355cb5fcac2247f23ca1fe8dd4256b41f2edd58b34f886fcb74bc6e7`  
		Last Modified: Tue, 14 Feb 2023 20:55:01 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc05ca820f63f78de074bd0a9ffe6889c8e3405b0563cf21ef5013179b8f407`  
		Last Modified: Tue, 14 Feb 2023 21:19:03 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b911bfee9062064c2f989b2acf01493bb3c9ad5989eb456277dfe272c1dcd2`  
		Last Modified: Tue, 14 Feb 2023 21:19:01 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aa3117c7e54c9d38a6d368beb815482c58bd46981294fc7c45046ca02b8d34`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710d1b3e32dd905f2dc2f33df9481f9abdd52cbd0028eadd5d0517fe673c3de1`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df812b30f4c795624a0ff09a18f3ac73987de268d9ee1aa080998e222a6f6e3`  
		Last Modified: Wed, 15 Feb 2023 20:18:10 GMT  
		Size: 1.9 MB (1868549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced4b40932769c58cc0b5348fdc7b4189892820c655d4029b988aafd8692dcd0`  
		Last Modified: Wed, 15 Feb 2023 20:18:09 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:236163a87c5609986ce7ddead7d8aaf992314f031699ddde2a400597640965e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.3887; amd64
	-	windows version 10.0.20348.1487; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:36ba71b44afa613ecf0aadce8e4b9e3f56e0c4b0a78c8edf4e8c2485f21b35ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17449113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8464e23f16f9a82426bbdc3ac8c94270a84453ddc86b9147505a2378a7c2fd0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:38:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 11 Feb 2023 07:38:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 19:19:21 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 19:19:23 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 19:19:24 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:25 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 19:19:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e3e797818bc929d95bae8220b7b6034b559c217ef5bf622dc7fedc8d270a48`  
		Last Modified: Sat, 11 Feb 2023 07:39:01 GMT  
		Size: 351.2 KB (351178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cebb4c80b3906a9b751ee9a512c1581331b1fd691c84f575c01a29e28403dde`  
		Last Modified: Sat, 11 Feb 2023 07:39:00 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90648ba22c191b969d8db393bf6138e7d6ecc1b70b3865d1717ec4d663192d89`  
		Last Modified: Wed, 15 Feb 2023 19:19:52 GMT  
		Size: 14.3 MB (14282621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5b39c4c37396031351c9753e4c7df6f2114d0ef588953b97c668d0ec7e2f1e50
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16582274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ffa8388ed5f7f62ab116b850faa63ff3214dea5fb007a77196a8efd0023832`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:28:54 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 21:28:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:49:22 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:49:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:49:26 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:49:26 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:49:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:49:27 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:49:28 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:49:28 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:49:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a400dcba29ff44f8e5bf01493def4f19629aca6d103cb2a66ca87c457f7414`  
		Last Modified: Fri, 10 Feb 2023 21:29:47 GMT  
		Size: 345.8 KB (345811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b946768825eb5ed2fc6f932fdb0b0c552f4c35c39dada07eddd70ce4a535953`  
		Last Modified: Fri, 10 Feb 2023 21:29:47 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f11ff5bb8d752ef2e91afa46770077fd62ddc9e78f280c00e796bf841c9d49f`  
		Last Modified: Wed, 15 Feb 2023 18:50:25 GMT  
		Size: 13.6 MB (13612205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:21302c9acb44ea61fccba3ef765712da93fede2d928aaafc8f7bd77a35d91953
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16365562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600d5193b2ba5875b66a6579717ec1aab50be117445a5a657045572141d1187c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:37 GMT
ADD file:193f48d48ed2e90a0e81663757e372f59806151c17e82113f03443db0ef723c3 in / 
# Fri, 10 Feb 2023 21:51:37 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:37:19 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:37:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:57:27 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:57:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:57:30 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:57:30 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:57:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:57:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:57:31 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:57:31 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:57:32 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:beefe5ad637c7db32e6afc68103fc4e779630219979216a625338ab55f7d191c`  
		Last Modified: Fri, 10 Feb 2023 21:52:51 GMT  
		Size: 2.4 MB (2420494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec2ab4edb1f0a14b28a55f050d62d8e54111075639a0fa8f173448814ba0d00`  
		Last Modified: Fri, 10 Feb 2023 22:38:25 GMT  
		Size: 342.6 KB (342588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0580184dd0082f009564a7a3923731f202cbe4bd8b857dbca2c77da8e7434815`  
		Last Modified: Fri, 10 Feb 2023 22:38:25 GMT  
		Size: 7.5 KB (7479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8682e09bc231d5c9076b76cb92cb3b1185b870277da03dbd7e87d7981ff6147a`  
		Last Modified: Wed, 15 Feb 2023 18:58:28 GMT  
		Size: 13.6 MB (13595001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:6c2623f6bf30798be5c37fc7484e45ecc288d493fb657883f59ddb27ed714ad8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16130997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a38afdc517ef4cff6b6b51a1c6a633c2826599b07feb1e88380d0f783e35cf1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:00:35 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:00:37 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:39:20 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:39:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:39:22 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:39:22 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:39:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:39:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:39:23 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:39:23 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:39:23 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70730e8e2fb933ec157ec87f2a4fb4ad45e8e578b8f7c76cc4846631d773554`  
		Last Modified: Fri, 10 Feb 2023 22:01:02 GMT  
		Size: 350.2 KB (350153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a4b7390d269477c225f1d03e825d2d8bdf6b4d87b5f7bb8811b341e56b7d36`  
		Last Modified: Fri, 10 Feb 2023 22:01:02 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2743d2ef53ee6edb0e39c89bf16957e3a00990410b2d1a126dca1b2d196182`  
		Last Modified: Wed, 15 Feb 2023 18:39:53 GMT  
		Size: 13.1 MB (13063787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:8861ab3ae3d0c180e38142c2f7482f9ce1773419eb29ed9d6d18308246858093
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15955172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5819f0ab4928a30c29293a27299a3b44371cd3bd97df91432ef7b3f43b692d8c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:13:21 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:13:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 19:16:26 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:16:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 19:16:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 19:16:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 19:16:42 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:16:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:16:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:16:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:16:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:16:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:16:46 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:16:47 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:16:47 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 19:16:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782bd0321e6539bb7dac8574fd36bad22059ef06bb63dc842165f69d0a821572`  
		Last Modified: Fri, 10 Feb 2023 22:14:16 GMT  
		Size: 363.1 KB (363088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb806b2600b0209a73fc7175ab778d0224661034b2f722bd1a0aec1eb9eabe3d`  
		Last Modified: Fri, 10 Feb 2023 22:14:15 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd7c8ae860931dd79dea76d33bc21bb11d89cd4d133cdb41078b040afc6633e`  
		Last Modified: Wed, 15 Feb 2023 19:17:41 GMT  
		Size: 12.8 MB (12779898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:4e1ed99f133abf02d6a7c77849978bb621f748e18c9cb9f7a1dbf88480ddb8d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16792756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45cd164da734310b788dcbd4f6c94bccff6e48705fe4d42ecca07a54e9459a9c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 10 Feb 2023 22:14:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"
# Wed, 15 Feb 2023 18:41:48 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 18:41:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='eed413b035ffacedfaf751a8431285c5d9a0a81a2a861444f4b95dd4c7508eabe2f3fcba6c5b8e6c70e30c9351dfa96ba39def47fa0879334d965dae3a869f1a' ;; 		armhf)   binArch='armv6'; checksum='72ab7c0bd627415cafcf3cc1adebdff0dcb2bb8f81e8969da356f741ae91289c231e20b29dbe268d501f252402adde151dcf7f3acfaf886c0b2dc02143fe5c01' ;; 		armv7)   binArch='armv7'; checksum='de8cb9cfb7d81e822d06ab55059d76dd285ed6d9b2861cd7ee5334622cf5938c61e0f0efcc4c6ccff0847b1c485752c670aa8d672fce5ca36edfd9c0714dc40c' ;; 		aarch64) binArch='arm64'; checksum='6513d40365c0570ff72c751db2d5f898d4ee9abe9241e73c3ad1062e21128745071b4efd3cc3443fc04fae2da49b69f06f70aadbe79d6a5327cc677fb86fb982' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='0341763653017b530a7b0137b6d1296101b21bec7a81b6320ed70479c342dc671d8a538dc07913b9b834e798b95097b4d9190986a296eed7f1a612bfa33fd752' ;; 		s390x)   binArch='s390x'; checksum='3d9779898401cbf37c3e5f1cfdbe253739340f2446d464e421db063c674e6a0ca355ae3c2a8374454ef470eed13f17493b40d259d3073775843bd5a1e47a7dc6' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Feb 2023 18:41:59 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Feb 2023 18:41:59 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Feb 2023 18:42:00 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 18:42:01 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 18:42:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 18:42:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 18:42:03 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 18:42:04 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 18:42:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 18:42:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 18:42:05 GMT
EXPOSE 80
# Wed, 15 Feb 2023 18:42:06 GMT
EXPOSE 443
# Wed, 15 Feb 2023 18:42:07 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 18:42:07 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 18:42:08 GMT
WORKDIR /srv
# Wed, 15 Feb 2023 18:42:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e6ec82400496ce74e37120e1655955b79303daaa5b8ca7e956e3cd96ddd6e9`  
		Last Modified: Fri, 10 Feb 2023 22:15:05 GMT  
		Size: 352.8 KB (352801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5b992687f93ced3715ad97bd95ab37daef5685b784e195209caefbc48f14e9`  
		Last Modified: Fri, 10 Feb 2023 22:15:05 GMT  
		Size: 7.6 KB (7557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccc40924ce2df3343fa5465a92ccaa4ed80e0883190a99d3f468c60f9ddbcf8`  
		Last Modified: Wed, 15 Feb 2023 18:43:19 GMT  
		Size: 13.8 MB (13838817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:371255c187169392f30d7caf1e65b8a8708afbdd8520eb74df9c38d973195766
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723380167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa79dce896513046be66642ea60c82eaf2266ff5533f3e8c40a79c7b779c0eca`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:16:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:15:47 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:17:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:17:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:17:11 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:17:12 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:17:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:17:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:17:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:17:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:17:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:17:20 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:17:21 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:17:22 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:17:24 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:17:43 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:17:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47af8a9c9ef8e49d65e53dd207ad0935ce7a2b50b2f253e6a5b037494ae19d0a`  
		Last Modified: Thu, 09 Feb 2023 01:16:50 GMT  
		Size: 401.5 KB (401472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d742cb3ca192278158c048ecc9f358855bc8f2629af70c62b9610a1fc66bbf0a`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859ce744a498d8f5affa0958dae6a0027cd48925c7c0bdf78214019c927eb34b`  
		Last Modified: Wed, 15 Feb 2023 20:17:06 GMT  
		Size: 14.7 MB (14694270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64525df3f764c2e65e711fbd328781c61243029c264aca6b09309e584dbb69b3`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231e1956368caba27b753959bf1fb5d38cf0e798477a45110f2691b063809554`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405677c240161263f0ca900ffca71596061f8d59668d524a80f16957c120f0c`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638a2e8fc9bd411f13b7b5a8b82272fd39024ac9b711d2bc73c28c39314fc3bb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1b8ca9045f120e19c22debd19df59f42aa442b84c073c7cfc2f5a2d0f463cb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c7468bd4bec28c11efd397d435df6a129ffc73265d2d2c4162bb121a336d08`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de41f5feb06b95a77601b9fd09ab7409b567e0d9684c46dfcdc4a067a00adc`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab6a97db0980bf9c94414bfb713b5db0ed7bec52a805303782c4309a6e9f62b`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41271d7026e5d15682fc59b1ac99ac0a67909c591ea0c7ab0885207386064744`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b605f7b22df792b7b41d97cec04cbfb795ba3588fd9e0b44363147a7a02820`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c2c11f6f75de707c6475d6248a27eb983282648b0a923c47e2894db7304e0d`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48461b499cb5763190c69d134f0b96625458bdd69fe78a15ade15efbad156033`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745ffdaac1ecada0622ef6d6ccfe6140992921240b91567821b96a07a72df8b8`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf9895ba16206d3ebb35a3a6e3f615542102d00230528158c62eee814428521`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc57c33625ddac815d78d81c0feb25f7dd3d6ea9f6d4f6238024e4898a15ef3c`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 316.4 KB (316447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31243cdae7d3d8bcf0b00d6c6c0a1f4ec3c2c277ca964f747f8acc133cef56a2`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:0722e548c2efb29869e87e89dc7cf03de8d31fe33c28e9e61a33f018b0a7a3e4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1401943529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a230b066a2fbe8bdfee6749b8afe9b1655260bb3643408c49082c8754a4cff75`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:18:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:18:03 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:19:13 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:19:14 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:19:15 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:24 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:26 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:27 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:46 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:19:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42eb48143612ee855d99c932e324b1bd035c60554117edeaa805402060613c51`  
		Last Modified: Thu, 09 Feb 2023 01:17:17 GMT  
		Size: 635.9 KB (635943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e120c0944228b4b6623b958c83433bc43f104b64cecccbd1ac7ab250e7a68db7`  
		Last Modified: Wed, 15 Feb 2023 20:17:30 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891cca6ce816bbe4dd40bd862cae84155f0da6f7f13ab15fb80f92c471772be7`  
		Last Modified: Wed, 15 Feb 2023 20:17:34 GMT  
		Size: 14.9 MB (14907106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e4718f6f1c46191ed75eaff08ff294c5ad0f384309aca914d5687324213f83`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0edcd24848e16049bee383e4ae89134f9d07da6079deed1398df66ad8a401ac`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b890b1c144cd00660796b630f5a2b8009a7c8b98a852cc4e645d13d84f4b48`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12054588e533ec29d2f174499ee24489e7b6d7b8527337dcdcc25a6ec29973`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e7efe9a5a718b562e89379f47cd1c2919b05c52ad1a2ceb9525d7f98f2f0d1`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fc39bc9c2bdee1444bb0e46b53cb55da0913be6b115f95bc50f5ed370138e`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d17482a1fa64018a51f2d8467fb3cba2c11aae5e67a689612e314d713ca8b0`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4843586865795ebb5e828c5f7fe6c9f829f9b12d5ad2e0bbf9f302874fc39a27`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd44712296ac1e7d28147c40159638788a75b58c17764de2757fcfda62f5551a`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5344aa95ac41ce0d03e95ae47d07c9ddef532b47bbfeb871053e69eacf5429a6`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf50f2a8532ee01e411b12116a827c2823a5cb2ee71091b4b724c44b6ba0f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b71f209c61027e4688f4e4b109ec883c187ed74b3d4c27e4b11596a4f20a07`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df052fc38d64efbb8657dd2c40cfa28c56f1137efcf1d7751277c1c81626b39e`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266955548153e827efba631ef21036116d523e11f332aae3910c4e6b773896f5`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59f15231c2a3b500e116b42a5254f441985197b1d364bc46a71cd917af38ec9`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 347.4 KB (347422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4a927a917a632a25082f22d95b2df35568f4522d622efe890c6d57457ed461`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:a0e880f407bc812d350d220b76e5e9da56ef9a34384f075923fb0eacfc9eef27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.3887; amd64
	-	windows version 10.0.20348.1487; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:371255c187169392f30d7caf1e65b8a8708afbdd8520eb74df9c38d973195766
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723380167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa79dce896513046be66642ea60c82eaf2266ff5533f3e8c40a79c7b779c0eca`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:16:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:15:47 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:17:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:17:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:17:11 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:17:12 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:17:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:17:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:17:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:17:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:17:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:17:20 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:17:21 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:17:22 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:17:24 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:17:43 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:17:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47af8a9c9ef8e49d65e53dd207ad0935ce7a2b50b2f253e6a5b037494ae19d0a`  
		Last Modified: Thu, 09 Feb 2023 01:16:50 GMT  
		Size: 401.5 KB (401472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d742cb3ca192278158c048ecc9f358855bc8f2629af70c62b9610a1fc66bbf0a`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859ce744a498d8f5affa0958dae6a0027cd48925c7c0bdf78214019c927eb34b`  
		Last Modified: Wed, 15 Feb 2023 20:17:06 GMT  
		Size: 14.7 MB (14694270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64525df3f764c2e65e711fbd328781c61243029c264aca6b09309e584dbb69b3`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231e1956368caba27b753959bf1fb5d38cf0e798477a45110f2691b063809554`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405677c240161263f0ca900ffca71596061f8d59668d524a80f16957c120f0c`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638a2e8fc9bd411f13b7b5a8b82272fd39024ac9b711d2bc73c28c39314fc3bb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1b8ca9045f120e19c22debd19df59f42aa442b84c073c7cfc2f5a2d0f463cb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c7468bd4bec28c11efd397d435df6a129ffc73265d2d2c4162bb121a336d08`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de41f5feb06b95a77601b9fd09ab7409b567e0d9684c46dfcdc4a067a00adc`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab6a97db0980bf9c94414bfb713b5db0ed7bec52a805303782c4309a6e9f62b`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41271d7026e5d15682fc59b1ac99ac0a67909c591ea0c7ab0885207386064744`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b605f7b22df792b7b41d97cec04cbfb795ba3588fd9e0b44363147a7a02820`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c2c11f6f75de707c6475d6248a27eb983282648b0a923c47e2894db7304e0d`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48461b499cb5763190c69d134f0b96625458bdd69fe78a15ade15efbad156033`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745ffdaac1ecada0622ef6d6ccfe6140992921240b91567821b96a07a72df8b8`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf9895ba16206d3ebb35a3a6e3f615542102d00230528158c62eee814428521`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc57c33625ddac815d78d81c0feb25f7dd3d6ea9f6d4f6238024e4898a15ef3c`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 316.4 KB (316447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31243cdae7d3d8bcf0b00d6c6c0a1f4ec3c2c277ca964f747f8acc133cef56a2`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:0722e548c2efb29869e87e89dc7cf03de8d31fe33c28e9e61a33f018b0a7a3e4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1401943529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a230b066a2fbe8bdfee6749b8afe9b1655260bb3643408c49082c8754a4cff75`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:18:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:18:03 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:19:13 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:19:14 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:19:15 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:24 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:26 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:27 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:46 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:19:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42eb48143612ee855d99c932e324b1bd035c60554117edeaa805402060613c51`  
		Last Modified: Thu, 09 Feb 2023 01:17:17 GMT  
		Size: 635.9 KB (635943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e120c0944228b4b6623b958c83433bc43f104b64cecccbd1ac7ab250e7a68db7`  
		Last Modified: Wed, 15 Feb 2023 20:17:30 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891cca6ce816bbe4dd40bd862cae84155f0da6f7f13ab15fb80f92c471772be7`  
		Last Modified: Wed, 15 Feb 2023 20:17:34 GMT  
		Size: 14.9 MB (14907106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e4718f6f1c46191ed75eaff08ff294c5ad0f384309aca914d5687324213f83`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0edcd24848e16049bee383e4ae89134f9d07da6079deed1398df66ad8a401ac`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b890b1c144cd00660796b630f5a2b8009a7c8b98a852cc4e645d13d84f4b48`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12054588e533ec29d2f174499ee24489e7b6d7b8527337dcdcc25a6ec29973`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e7efe9a5a718b562e89379f47cd1c2919b05c52ad1a2ceb9525d7f98f2f0d1`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fc39bc9c2bdee1444bb0e46b53cb55da0913be6b115f95bc50f5ed370138e`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d17482a1fa64018a51f2d8467fb3cba2c11aae5e67a689612e314d713ca8b0`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4843586865795ebb5e828c5f7fe6c9f829f9b12d5ad2e0bbf9f302874fc39a27`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd44712296ac1e7d28147c40159638788a75b58c17764de2757fcfda62f5551a`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5344aa95ac41ce0d03e95ae47d07c9ddef532b47bbfeb871053e69eacf5429a6`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf50f2a8532ee01e411b12116a827c2823a5cb2ee71091b4b724c44b6ba0f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b71f209c61027e4688f4e4b109ec883c187ed74b3d4c27e4b11596a4f20a07`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df052fc38d64efbb8657dd2c40cfa28c56f1137efcf1d7751277c1c81626b39e`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266955548153e827efba631ef21036116d523e11f332aae3910c4e6b773896f5`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59f15231c2a3b500e116b42a5254f441985197b1d364bc46a71cd917af38ec9`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 347.4 KB (347422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4a927a917a632a25082f22d95b2df35568f4522d622efe890c6d57457ed461`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:9b3fc2e9403b99a6fce9d5b94de587e848616342ccad9275d8bbead1a4b8f1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull caddy@sha256:371255c187169392f30d7caf1e65b8a8708afbdd8520eb74df9c38d973195766
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723380167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa79dce896513046be66642ea60c82eaf2266ff5533f3e8c40a79c7b779c0eca`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:16:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:15:47 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:17:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:17:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:17:11 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:17:12 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:17:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:17:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:17:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:17:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:17:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:17:20 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:17:21 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:17:22 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:17:24 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:17:43 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:17:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47af8a9c9ef8e49d65e53dd207ad0935ce7a2b50b2f253e6a5b037494ae19d0a`  
		Last Modified: Thu, 09 Feb 2023 01:16:50 GMT  
		Size: 401.5 KB (401472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d742cb3ca192278158c048ecc9f358855bc8f2629af70c62b9610a1fc66bbf0a`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859ce744a498d8f5affa0958dae6a0027cd48925c7c0bdf78214019c927eb34b`  
		Last Modified: Wed, 15 Feb 2023 20:17:06 GMT  
		Size: 14.7 MB (14694270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64525df3f764c2e65e711fbd328781c61243029c264aca6b09309e584dbb69b3`  
		Last Modified: Wed, 15 Feb 2023 20:17:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231e1956368caba27b753959bf1fb5d38cf0e798477a45110f2691b063809554`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405677c240161263f0ca900ffca71596061f8d59668d524a80f16957c120f0c`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638a2e8fc9bd411f13b7b5a8b82272fd39024ac9b711d2bc73c28c39314fc3bb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1b8ca9045f120e19c22debd19df59f42aa442b84c073c7cfc2f5a2d0f463cb`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c7468bd4bec28c11efd397d435df6a129ffc73265d2d2c4162bb121a336d08`  
		Last Modified: Wed, 15 Feb 2023 20:17:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de41f5feb06b95a77601b9fd09ab7409b567e0d9684c46dfcdc4a067a00adc`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab6a97db0980bf9c94414bfb713b5db0ed7bec52a805303782c4309a6e9f62b`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41271d7026e5d15682fc59b1ac99ac0a67909c591ea0c7ab0885207386064744`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b605f7b22df792b7b41d97cec04cbfb795ba3588fd9e0b44363147a7a02820`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c2c11f6f75de707c6475d6248a27eb983282648b0a923c47e2894db7304e0d`  
		Last Modified: Wed, 15 Feb 2023 20:16:59 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48461b499cb5763190c69d134f0b96625458bdd69fe78a15ade15efbad156033`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745ffdaac1ecada0622ef6d6ccfe6140992921240b91567821b96a07a72df8b8`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf9895ba16206d3ebb35a3a6e3f615542102d00230528158c62eee814428521`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc57c33625ddac815d78d81c0feb25f7dd3d6ea9f6d4f6238024e4898a15ef3c`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 316.4 KB (316447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31243cdae7d3d8bcf0b00d6c6c0a1f4ec3c2c277ca964f747f8acc133cef56a2`  
		Last Modified: Wed, 15 Feb 2023 20:16:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:113f187a1100da96770eeaecc6e118b4be7ef33cb4d01611de3e3045ed3a4acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:0722e548c2efb29869e87e89dc7cf03de8d31fe33c28e9e61a33f018b0a7a3e4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1401943529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a230b066a2fbe8bdfee6749b8afe9b1655260bb3643408c49082c8754a4cff75`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:18:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 15 Feb 2023 19:18:03 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 15 Feb 2023 19:19:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.4/caddy_2.6.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e2a9a708786cc498cf4b12c0aaf2c9731cc89ccef71a7da4c2be60e18d730675890c2d6bbddd3d8347e5f89f348d5e74fbfbf339ed1ec280f5caf69c3849a243')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 15 Feb 2023 19:19:13 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 15 Feb 2023 19:19:14 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 15 Feb 2023 19:19:15 GMT
LABEL org.opencontainers.image.version=v2.6.4
# Wed, 15 Feb 2023 19:19:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Feb 2023 19:19:17 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Feb 2023 19:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Feb 2023 19:19:19 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Feb 2023 19:19:20 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Feb 2023 19:19:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Feb 2023 19:19:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Feb 2023 19:19:24 GMT
EXPOSE 80
# Wed, 15 Feb 2023 19:19:25 GMT
EXPOSE 443
# Wed, 15 Feb 2023 19:19:26 GMT
EXPOSE 443/udp
# Wed, 15 Feb 2023 19:19:27 GMT
EXPOSE 2019
# Wed, 15 Feb 2023 19:19:46 GMT
RUN caddy version
# Wed, 15 Feb 2023 19:19:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42eb48143612ee855d99c932e324b1bd035c60554117edeaa805402060613c51`  
		Last Modified: Thu, 09 Feb 2023 01:17:17 GMT  
		Size: 635.9 KB (635943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e120c0944228b4b6623b958c83433bc43f104b64cecccbd1ac7ab250e7a68db7`  
		Last Modified: Wed, 15 Feb 2023 20:17:30 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891cca6ce816bbe4dd40bd862cae84155f0da6f7f13ab15fb80f92c471772be7`  
		Last Modified: Wed, 15 Feb 2023 20:17:34 GMT  
		Size: 14.9 MB (14907106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e4718f6f1c46191ed75eaff08ff294c5ad0f384309aca914d5687324213f83`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0edcd24848e16049bee383e4ae89134f9d07da6079deed1398df66ad8a401ac`  
		Last Modified: Wed, 15 Feb 2023 20:17:29 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b890b1c144cd00660796b630f5a2b8009a7c8b98a852cc4e645d13d84f4b48`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12054588e533ec29d2f174499ee24489e7b6d7b8527337dcdcc25a6ec29973`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e7efe9a5a718b562e89379f47cd1c2919b05c52ad1a2ceb9525d7f98f2f0d1`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3fc39bc9c2bdee1444bb0e46b53cb55da0913be6b115f95bc50f5ed370138e`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d17482a1fa64018a51f2d8467fb3cba2c11aae5e67a689612e314d713ca8b0`  
		Last Modified: Wed, 15 Feb 2023 20:17:28 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4843586865795ebb5e828c5f7fe6c9f829f9b12d5ad2e0bbf9f302874fc39a27`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd44712296ac1e7d28147c40159638788a75b58c17764de2757fcfda62f5551a`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5344aa95ac41ce0d03e95ae47d07c9ddef532b47bbfeb871053e69eacf5429a6`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf50f2a8532ee01e411b12116a827c2823a5cb2ee71091b4b724c44b6ba0f4`  
		Last Modified: Wed, 15 Feb 2023 20:17:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b71f209c61027e4688f4e4b109ec883c187ed74b3d4c27e4b11596a4f20a07`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df052fc38d64efbb8657dd2c40cfa28c56f1137efcf1d7751277c1c81626b39e`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266955548153e827efba631ef21036116d523e11f332aae3910c4e6b773896f5`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59f15231c2a3b500e116b42a5254f441985197b1d364bc46a71cd917af38ec9`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 347.4 KB (347422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4a927a917a632a25082f22d95b2df35568f4522d622efe890c6d57457ed461`  
		Last Modified: Wed, 15 Feb 2023 20:17:24 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
