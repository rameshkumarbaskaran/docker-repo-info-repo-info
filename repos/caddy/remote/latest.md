## `caddy:latest`

```console
$ docker pull caddy@sha256:485ce30fa5075d97efb05d2e0bc6f59a0e8d6a8ab975d99f8f89d02df0be5aee
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
$ docker pull caddy@sha256:6426c9377b7ab9773e33b920b9baf37c887c7da85884b32d04fe96b96d699779
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17443255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4120819d2095ee6936abc77c4e0a77b849f8b879967e9df5f17aa4c6e74e517a`
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
# Sat, 11 Feb 2023 07:38:36 GMT
ENV CADDY_VERSION=v2.6.3
# Sat, 11 Feb 2023 07:38:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='788fd38ad7b600f0b4bf6d0493da1b319f9b9fcb9099693b4fefed9ab6d8f007fb438ae082c46dc12abc4dacb467d7dbdf4cc200819aa4a502d8b47b805fea1b' ;; 		armhf)   binArch='armv6'; checksum='a5b3ab1b8d8e637c87ca2b5ed0e9bed28d4fe3fc214aad94212253098cd6d121453f3c325d2b27ec87bb84300daf2a9f2145948a7bf85573ca3f90ea9bca4c18' ;; 		armv7)   binArch='armv7'; checksum='4e060e33ffcaf60bd70216618d71379be0add74ee9ede7867934ff61b1412915e468c7a9a478fa302ae7c270fbb0d9e6609afcf52841cf6ea9394e11a8216741' ;; 		aarch64) binArch='arm64'; checksum='eafd3842a1df5900d46f4b0db0bcca2cc598ecd5beb555e14a15e0df9984158de3b46f1595d3bd4264d7094a0681be1f38c0dbad4e125fc3ab0481881636199a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='1b898890e1d9e46b93b740ac1af9d96232f7fbab1e0bbc94505626e7f6ce00150ed8c7b5117f076e8c11664c65fa4e39bea34e48ef75efd1a14c30d9b477e3ed' ;; 		s390x)   binArch='s390x'; checksum='5c1c4fcf13078a464aa6a15edc407b87f2dfd6da284abba8d895efcfe195a8fd123da1e29c1c70629d1118fdf590e4c8970d3351623eac4da1cdd31a3b75a8b3' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.3/caddy_2.6.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 11 Feb 2023 07:38:38 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 11 Feb 2023 07:38:38 GMT
ENV XDG_DATA_HOME=/data
# Sat, 11 Feb 2023 07:38:39 GMT
LABEL org.opencontainers.image.version=v2.6.3
# Sat, 11 Feb 2023 07:38:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 11 Feb 2023 07:38:39 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 11 Feb 2023 07:38:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 11 Feb 2023 07:38:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 11 Feb 2023 07:38:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 11 Feb 2023 07:38:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 11 Feb 2023 07:38:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 11 Feb 2023 07:38:39 GMT
EXPOSE 80
# Sat, 11 Feb 2023 07:38:39 GMT
EXPOSE 443
# Sat, 11 Feb 2023 07:38:40 GMT
EXPOSE 443/udp
# Sat, 11 Feb 2023 07:38:40 GMT
EXPOSE 2019
# Sat, 11 Feb 2023 07:38:40 GMT
WORKDIR /srv
# Sat, 11 Feb 2023 07:38:40 GMT
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
	-	`sha256:6b7e311d8ad654014c4cbf3afda85d0961d32598019e17499c49c8db7be07589`  
		Last Modified: Sat, 11 Feb 2023 07:39:03 GMT  
		Size: 14.3 MB (14276763 bytes)  
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
$ docker pull caddy@sha256:50a289625f0ef1adfc05773b5ec8a30f001be347a84f24e1106e351f230758b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15949909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b11b3ee451004883e1f9089fc132ee1ecc849a2d96ef0ff4731334c8279cfa`
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
# Fri, 10 Feb 2023 22:13:23 GMT
ENV CADDY_VERSION=v2.6.3
# Fri, 10 Feb 2023 22:13:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='788fd38ad7b600f0b4bf6d0493da1b319f9b9fcb9099693b4fefed9ab6d8f007fb438ae082c46dc12abc4dacb467d7dbdf4cc200819aa4a502d8b47b805fea1b' ;; 		armhf)   binArch='armv6'; checksum='a5b3ab1b8d8e637c87ca2b5ed0e9bed28d4fe3fc214aad94212253098cd6d121453f3c325d2b27ec87bb84300daf2a9f2145948a7bf85573ca3f90ea9bca4c18' ;; 		armv7)   binArch='armv7'; checksum='4e060e33ffcaf60bd70216618d71379be0add74ee9ede7867934ff61b1412915e468c7a9a478fa302ae7c270fbb0d9e6609afcf52841cf6ea9394e11a8216741' ;; 		aarch64) binArch='arm64'; checksum='eafd3842a1df5900d46f4b0db0bcca2cc598ecd5beb555e14a15e0df9984158de3b46f1595d3bd4264d7094a0681be1f38c0dbad4e125fc3ab0481881636199a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='1b898890e1d9e46b93b740ac1af9d96232f7fbab1e0bbc94505626e7f6ce00150ed8c7b5117f076e8c11664c65fa4e39bea34e48ef75efd1a14c30d9b477e3ed' ;; 		s390x)   binArch='s390x'; checksum='5c1c4fcf13078a464aa6a15edc407b87f2dfd6da284abba8d895efcfe195a8fd123da1e29c1c70629d1118fdf590e4c8970d3351623eac4da1cdd31a3b75a8b3' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.6.3/caddy_2.6.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 10 Feb 2023 22:13:28 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 10 Feb 2023 22:13:28 GMT
ENV XDG_DATA_HOME=/data
# Fri, 10 Feb 2023 22:13:29 GMT
LABEL org.opencontainers.image.version=v2.6.3
# Fri, 10 Feb 2023 22:13:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 10 Feb 2023 22:13:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 10 Feb 2023 22:13:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 10 Feb 2023 22:13:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 10 Feb 2023 22:13:30 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 10 Feb 2023 22:13:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 10 Feb 2023 22:13:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 10 Feb 2023 22:13:32 GMT
EXPOSE 80
# Fri, 10 Feb 2023 22:13:32 GMT
EXPOSE 443
# Fri, 10 Feb 2023 22:13:32 GMT
EXPOSE 443/udp
# Fri, 10 Feb 2023 22:13:33 GMT
EXPOSE 2019
# Fri, 10 Feb 2023 22:13:33 GMT
WORKDIR /srv
# Fri, 10 Feb 2023 22:13:33 GMT
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
	-	`sha256:2ecc7ec17344834a2337d83b9b7be44f97f0c0b55dfea5e1d8af80c8d5c32221`  
		Last Modified: Fri, 10 Feb 2023 22:14:19 GMT  
		Size: 12.8 MB (12774635 bytes)  
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
$ docker pull caddy@sha256:935d1f4349cc551dfe9b76d6ba5fe6355414519a3037a7689fe765033ae8dcd6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723388621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1deb1aecac8501d9afe22abd2fc90f15552c63366f8016ad2e6d1602be5cdf6d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:16:35 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 09 Feb 2023 00:16:36 GMT
ENV CADDY_VERSION=v2.6.3
# Thu, 09 Feb 2023 00:17:19 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.3/caddy_2.6.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('5529a43f9d91b02bc4b8dc89e3c60b59395d1725079a46e8477a105ecb809da54e4ffed5698f4083dba397745c160511c07630d38c2d2695380c75ffb7e6afd1')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 09 Feb 2023 00:17:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 09 Feb 2023 00:17:21 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 09 Feb 2023 00:17:22 GMT
LABEL org.opencontainers.image.version=v2.6.3
# Thu, 09 Feb 2023 00:17:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 09 Feb 2023 00:17:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 09 Feb 2023 00:17:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 09 Feb 2023 00:17:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 09 Feb 2023 00:17:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 09 Feb 2023 00:17:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 09 Feb 2023 00:17:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 09 Feb 2023 00:17:31 GMT
EXPOSE 80
# Thu, 09 Feb 2023 00:17:32 GMT
EXPOSE 443
# Thu, 09 Feb 2023 00:17:33 GMT
EXPOSE 443/udp
# Thu, 09 Feb 2023 00:17:34 GMT
EXPOSE 2019
# Thu, 09 Feb 2023 00:17:53 GMT
RUN caddy version
# Thu, 09 Feb 2023 00:17:54 GMT
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
	-	`sha256:9e5841cb6343add9dd7b89906610425117976b050c0634eedbc5c38302aa024e`  
		Last Modified: Thu, 09 Feb 2023 01:16:50 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d760049e5c9f1fb1d7ec05a3eea55088808f484912e87cda07f3709363fe3c2c`  
		Last Modified: Thu, 09 Feb 2023 01:16:53 GMT  
		Size: 14.7 MB (14680484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3239225b5bad52e6004b638bd356e7d29e7fded5d31d90541907e1a769a115`  
		Last Modified: Thu, 09 Feb 2023 01:16:49 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6823ad091829bc6d98a58a18b075e20c551bde81d504bdbfda09b5a3d7c5d0`  
		Last Modified: Thu, 09 Feb 2023 01:16:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4873a8802163accb90dd2318bd05ddfa4f94692b2731d6e23095e3bb46b98fd`  
		Last Modified: Thu, 09 Feb 2023 01:16:48 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eabf39e152fd5c18e0c3ac503e054c36e2775512f9fa7bb11b9221442b2bc1fa`  
		Last Modified: Thu, 09 Feb 2023 01:16:47 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af12dc4018ba87a8e25003874e2d8e959a25b1c19932553daec8f4c410ebd61f`  
		Last Modified: Thu, 09 Feb 2023 01:16:47 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefa1f82e39e2af863b13609d78d966746d852af0cea54dcb17f45a8386c39d6`  
		Last Modified: Thu, 09 Feb 2023 01:16:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d5b41708aea61714f00bc0f35ea1efc60db85c04ab6754e4d6b4485dc59a28`  
		Last Modified: Thu, 09 Feb 2023 01:16:46 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a8b1cf8bcc4175323f7feaa280e3122f03aa7f9d35666fcc55c6b7d1e628ae`  
		Last Modified: Thu, 09 Feb 2023 01:16:46 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6c3f865e552649c436d5ffc0f3c83a3b5ba3026b2cff2ab3f381a5cdf2e2f2`  
		Last Modified: Thu, 09 Feb 2023 01:16:45 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201cfdbfc1583e2ea070418e6aad0ec6604fb52c68117460b1a4c5b511b56ecc`  
		Last Modified: Thu, 09 Feb 2023 01:16:45 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef83199fb67566ea043dbf7fab6f54754a4d0496655be1157819973573247bb`  
		Last Modified: Thu, 09 Feb 2023 01:16:45 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45db789a3d9786dea133341e2c9f16e14b23a664297ad7f9a371961a0c21588`  
		Last Modified: Thu, 09 Feb 2023 01:16:43 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4e021c112717a1fee7cd62cdc17d41521f3514f10bf8ec30457b95aaf44fa`  
		Last Modified: Thu, 09 Feb 2023 01:16:43 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4c0327054bc1f199339822d4074ee176c4184b9357ec28d9250f27f0c12e26`  
		Last Modified: Thu, 09 Feb 2023 01:16:43 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63a4d912695117a127068d20ceefbaa19e41c8a42d65788d37915d737d998d6`  
		Last Modified: Thu, 09 Feb 2023 01:16:44 GMT  
		Size: 338.6 KB (338620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421719fbbf536a3651d6762e36406f19dd0b5601f4a300d9c47af9ccfa3573d2`  
		Last Modified: Thu, 09 Feb 2023 01:16:43 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.20348.1487; amd64

```console
$ docker pull caddy@sha256:22cdfda624195707c05f1d681c1cdd97b504f06b282d981718e1b716b2dc6bfb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1401937005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7c6af6ec202266d95f15726fee733430a631c6c4eddfd9cc7d000b817a0f19`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Feb 2023 00:18:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/305fe484cc8a9ac72900e8cc172d652102a87240/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 09 Feb 2023 00:18:44 GMT
ENV CADDY_VERSION=v2.6.3
# Thu, 09 Feb 2023 00:19:15 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.6.3/caddy_2.6.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('5529a43f9d91b02bc4b8dc89e3c60b59395d1725079a46e8477a105ecb809da54e4ffed5698f4083dba397745c160511c07630d38c2d2695380c75ffb7e6afd1')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 09 Feb 2023 00:19:16 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 09 Feb 2023 00:19:17 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 09 Feb 2023 00:19:18 GMT
LABEL org.opencontainers.image.version=v2.6.3
# Thu, 09 Feb 2023 00:19:19 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 09 Feb 2023 00:19:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 09 Feb 2023 00:19:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 09 Feb 2023 00:19:22 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 09 Feb 2023 00:19:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 09 Feb 2023 00:19:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 09 Feb 2023 00:19:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 09 Feb 2023 00:19:26 GMT
EXPOSE 80
# Thu, 09 Feb 2023 00:19:27 GMT
EXPOSE 443
# Thu, 09 Feb 2023 00:19:29 GMT
EXPOSE 443/udp
# Thu, 09 Feb 2023 00:19:30 GMT
EXPOSE 2019
# Thu, 09 Feb 2023 00:19:47 GMT
RUN caddy version
# Thu, 09 Feb 2023 00:19:48 GMT
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
	-	`sha256:b714ae92cb5dac0e72097d35b932125b5ea3f03214de78e03119a4517be6fd10`  
		Last Modified: Thu, 09 Feb 2023 01:17:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a5533d3ddbff5ea35dbb0e11b10fe817ce3ef1a3fd7f44706cb1b6288e0406`  
		Last Modified: Thu, 09 Feb 2023 01:17:20 GMT  
		Size: 14.9 MB (14899830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e59c8f0dc8d987210bdfe89eaded536b0ef8ac727eb7d75b76aea9c296208a`  
		Last Modified: Thu, 09 Feb 2023 01:17:16 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22bfc3588219a43ce294aab21751b407ae75504bf3ddcee69f42498672b6c46`  
		Last Modified: Thu, 09 Feb 2023 01:17:14 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f7db57dc0a0b0126433f60d3d0005f9aaa0d405fe63cfc3b4e15388fdfa010`  
		Last Modified: Thu, 09 Feb 2023 01:17:14 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7b9e3a2510b5ab3b7ac4103d653c8efd12e95b63327d5c5fb81b6ea341e2b5`  
		Last Modified: Thu, 09 Feb 2023 01:17:14 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4109b3b0ca73b5355a12ee74b7c32b4015a6208fdb279fd0ab60074247e22309`  
		Last Modified: Thu, 09 Feb 2023 01:17:14 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3c568a1866d44483984b2be40142a55371adf3b8dc991bdb5ab4c45c0be3d4`  
		Last Modified: Thu, 09 Feb 2023 01:17:14 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6221c7c14444b318e798e231adeeb83ea155c157283e9def018c43415238aa7`  
		Last Modified: Thu, 09 Feb 2023 01:17:12 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e81980463382095586f78276db5cd808400136543fc1a0f522af1f3eaee034`  
		Last Modified: Thu, 09 Feb 2023 01:17:12 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f0d8afe85320b7cf4542ad649671660bbb8e74ec3ad3067408e79fb21dbf77`  
		Last Modified: Thu, 09 Feb 2023 01:17:12 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7def0e2b3dd94a350c82bb6a4903fdfc65d1d3d9772dd8195a5eb14ba766c45`  
		Last Modified: Thu, 09 Feb 2023 01:17:12 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0b51c8090bf08cc2ae3a9fc340c9b70ba1e077f32b7d7d025b7d9fb472d978`  
		Last Modified: Thu, 09 Feb 2023 01:17:12 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3653016f515e293fc93892b9e021e05a6a183ad3dcdaf243311513e222534c7`  
		Last Modified: Thu, 09 Feb 2023 01:17:10 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d1dafd3fbb7403b7f093ed63553863bd9904f6010b1b91f98d9bfba9c4d8bb`  
		Last Modified: Thu, 09 Feb 2023 01:17:10 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92817327253aaae4d632a75ff38a01dbebfe11f9105c4db828c52f221262ce4`  
		Last Modified: Thu, 09 Feb 2023 01:17:10 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43bce457643a143e82e49e57d9b8a69a416e254d2439f30d7e4dd25c84e43c0`  
		Last Modified: Thu, 09 Feb 2023 01:17:10 GMT  
		Size: 348.1 KB (348138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a0e899ab4c995de79522a5022b8cca4765559a4de2d5c728821d947b497de1`  
		Last Modified: Thu, 09 Feb 2023 01:17:10 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
