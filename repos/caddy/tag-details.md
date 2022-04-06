<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `caddy`

-	[`caddy:2`](#caddy2)
-	[`caddy:2-alpine`](#caddy2-alpine)
-	[`caddy:2-builder`](#caddy2-builder)
-	[`caddy:2-builder-alpine`](#caddy2-builder-alpine)
-	[`caddy:2-builder-windowsservercore-1809`](#caddy2-builder-windowsservercore-1809)
-	[`caddy:2-windowsservercore`](#caddy2-windowsservercore)
-	[`caddy:2-windowsservercore-1809`](#caddy2-windowsservercore-1809)
-	[`caddy:2.4.6`](#caddy246)
-	[`caddy:2.4.6-alpine`](#caddy246-alpine)
-	[`caddy:2.4.6-builder`](#caddy246-builder)
-	[`caddy:2.4.6-builder-alpine`](#caddy246-builder-alpine)
-	[`caddy:2.4.6-builder-windowsservercore-1809`](#caddy246-builder-windowsservercore-1809)
-	[`caddy:2.4.6-windowsservercore`](#caddy246-windowsservercore)
-	[`caddy:2.4.6-windowsservercore-1809`](#caddy246-windowsservercore-1809)
-	[`caddy:2.5.0-beta.1`](#caddy250-beta1)
-	[`caddy:2.5.0-beta.1-alpine`](#caddy250-beta1-alpine)
-	[`caddy:2.5.0-beta.1-builder`](#caddy250-beta1-builder)
-	[`caddy:2.5.0-beta.1-builder-alpine`](#caddy250-beta1-builder-alpine)
-	[`caddy:2.5.0-beta.1-builder-windowsservercore-1809`](#caddy250-beta1-builder-windowsservercore-1809)
-	[`caddy:2.5.0-beta.1-builder-windowsservercore-ltsc2022`](#caddy250-beta1-builder-windowsservercore-ltsc2022)
-	[`caddy:2.5.0-beta.1-windowsservercore`](#caddy250-beta1-windowsservercore)
-	[`caddy:2.5.0-beta.1-windowsservercore-1809`](#caddy250-beta1-windowsservercore-1809)
-	[`caddy:2.5.0-beta.1-windowsservercore-ltsc2022`](#caddy250-beta1-windowsservercore-ltsc2022)
-	[`caddy:alpine`](#caddyalpine)
-	[`caddy:builder`](#caddybuilder)
-	[`caddy:builder-alpine`](#caddybuilder-alpine)
-	[`caddy:builder-windowsservercore-1809`](#caddybuilder-windowsservercore-1809)
-	[`caddy:latest`](#caddylatest)
-	[`caddy:windowsservercore`](#caddywindowsservercore)
-	[`caddy:windowsservercore-1809`](#caddywindowsservercore-1809)

## `caddy:2`

```console
$ docker pull caddy@sha256:50a38e32a96b709de9e5112eb1909b7f03fab16959929da71f342c5bdb114641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2686; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:c8555e2ca66576a4404c2b5f31d843a5378dea6134acb500502901b563efebcf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14842034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ace180df3e668bd7937be4555305fdb7686c68acf2b5514665e2bac99bd266a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:24:48 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 04:24:50 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 04:24:50 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 04:24:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 04:24:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:24:52 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 04:24:52 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 04:24:52 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 04:24:53 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 80
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 443
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 04:24:54 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 04:24:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe024ea85c2d7fb47ce4f044038d4227cee2a982bca3e26a0ea4772b8b652f9a`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 291.2 KB (291230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438e4a77a6e9c40c3bf1fb392618ac596307733f97d294edb86383ce8ff7e51d`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6d2ebbfc8548ecc1dbf4c7568459e52549b81522cb450d42ada1bf82513a8d`  
		Last Modified: Tue, 05 Apr 2022 04:25:34 GMT  
		Size: 11.7 MB (11726452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c5f60dbd2d0286f964c9769a4a3396935a60d0d71ac0e3f8eea5c4c20711fb`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:01ed10f530dfa4af76fa0f13bcdde451a934fbd3a2d77e4cfa72dbc5587ac6f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14049473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c322930340bb73e0796df576638a0214eda5499c8f9b79e4f9af61aeb4da4d2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:14:11 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:14:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 03:14:14 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 03:14:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 03:14:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 03:14:20 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 03:14:21 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 03:14:21 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 03:14:22 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 03:14:22 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 03:14:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 03:14:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 03:14:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 03:14:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 03:14:26 GMT
EXPOSE 80
# Tue, 05 Apr 2022 03:14:26 GMT
EXPOSE 443
# Tue, 05 Apr 2022 03:14:27 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 03:14:27 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 03:14:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d650105deec735ac6dce2611f274a6cf2d9f60fc811167dd6d644e281a38f5`  
		Last Modified: Tue, 05 Apr 2022 03:17:39 GMT  
		Size: 291.7 KB (291653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f3d66a6432942b556bf7a077c220319708b7fc75279695b4b05fa25166fbaf`  
		Last Modified: Tue, 05 Apr 2022 03:17:38 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5d8162ee509e3528dd82e497c4057d40064d43d532acc589b4408c08d2b144`  
		Last Modified: Tue, 05 Apr 2022 03:17:46 GMT  
		Size: 11.1 MB (11125784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0ebc13031265ef07e50f9c7658d00ce8d28c00affdf202b6dd849558f06ad6`  
		Last Modified: Tue, 05 Apr 2022 03:17:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:80bf5252e7e8c04e9ff83dd861f7ee4e81bad7b2b52b5c78a43abf0c95818cf7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dddbbfbbc47ddc2ad3b96622c35ee55ec3eecd5e37cde28c3dfe807ac0827ba`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:52 GMT
ADD file:97f7b59ed0e40e7771daab294820763a7bb86c843317be55725baf1cab39aa12 in / 
# Mon, 04 Apr 2022 23:57:52 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:32:17 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:32:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 06:32:20 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 06:32:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 06:32:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:32:26 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 06:32:26 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 06:32:27 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 06:32:27 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 06:32:28 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 06:32:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 06:32:30 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 06:32:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 06:32:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 06:32:31 GMT
EXPOSE 80
# Tue, 05 Apr 2022 06:32:32 GMT
EXPOSE 443
# Tue, 05 Apr 2022 06:32:32 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 06:32:33 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 06:32:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:380010979fdd8a9a4b0bf397034a27ec6cabe61d36e9e6d460ea986f0ddaef38`  
		Last Modified: Mon, 04 Apr 2022 23:59:45 GMT  
		Size: 2.4 MB (2427969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0decd23e3d353b46346bc943e7c39f406496ebc5b14731e4575f770563ddef21`  
		Last Modified: Tue, 05 Apr 2022 06:34:41 GMT  
		Size: 290.6 KB (290637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf30d07056a9a35092dc8a190963a5d19c14fce0543c6f6cfed98fc9a687dc5f`  
		Last Modified: Tue, 05 Apr 2022 06:34:40 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbde61fe85af3ebca0218d5ca1f9b5b6d095a57aedc0d7a827ba511e2143629`  
		Last Modified: Tue, 05 Apr 2022 06:34:48 GMT  
		Size: 11.1 MB (11106715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9e55ef38253194b94160973edf2d58fbb2df74561e28d5e7894a3865f9daf8`  
		Last Modified: Tue, 05 Apr 2022 06:34:40 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:e526f540c45973c7a3a4585918890beceac9f0916e124daea3bf4e8b7a1e09b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13753199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2982d1a58becf38a1cf55541dcd74c1b096e8a02bb2060c30540fd3246e46e4f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:11:38 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:11:40 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 03:11:41 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 03:11:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 03:11:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 03:11:45 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 03:11:46 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 03:11:47 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 03:11:48 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 03:11:49 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 03:11:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 03:11:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 03:11:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 03:11:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 03:11:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 03:11:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 03:11:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 03:11:57 GMT
EXPOSE 80
# Tue, 05 Apr 2022 03:11:58 GMT
EXPOSE 443
# Tue, 05 Apr 2022 03:11:59 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 03:12:00 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 03:12:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b907f83114020e794129b34363890abf552785b8d964dbd3546272cc805702ce`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 291.3 KB (291281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988559859d9a4661992cbcefddba5b3d7a16de6c22547a962024f04767e6debf`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 5.7 KB (5748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7769260cde91250d6c68897788b078fea0a63b1254082d2923affeb859224a92`  
		Last Modified: Tue, 05 Apr 2022 03:13:22 GMT  
		Size: 10.7 MB (10738627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0143e63583cae9b0bc2b0048073b6c52476761cbeffa8e6aeca59d227ae0ee2`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:0f4502864c2fae9298130a48ec4ca4351af0787bee15fd4cb5307b7b83e87dd8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13416150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b308dba8382e868224f828f88958151f9c1af01332da44ca296967f8bf09d40b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:44 GMT
ADD file:0b9367758b91930d9d69fd3901262e3a696f7a9f6d9e209e35da83ea6e785837 in / 
# Tue, 05 Apr 2022 00:23:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:07:02 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 07:07:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 07:07:12 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 07:07:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 07:07:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:07:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 07:07:31 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 07:07:33 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 07:07:36 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 07:07:40 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 07:07:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 07:07:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 07:07:47 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 07:07:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 07:07:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 07:07:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 07:07:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 07:08:03 GMT
EXPOSE 80
# Tue, 05 Apr 2022 07:08:06 GMT
EXPOSE 443
# Tue, 05 Apr 2022 07:08:08 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 07:08:10 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 07:08:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ee5f6345565e7aeda814a5c097612cacb0a74186b1f01bf5199e1b812b5d3065`  
		Last Modified: Tue, 05 Apr 2022 00:25:06 GMT  
		Size: 2.8 MB (2814167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8affbe739a71e3875810f257750034ec7a6ee3f2f2c0094f3bcb3ed8a45520b`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 293.7 KB (293710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc927cb41936aaa5bfefa5dc4d654b7193fd568f619707120a5491c620906fc1`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8646c35213c358f518a4d76b75742b5930acec5d12cbd6c75d0a7e217698cee`  
		Last Modified: Tue, 05 Apr 2022 07:11:06 GMT  
		Size: 10.3 MB (10302288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346269e52424a62ec14d10c3e1db1aeb9cefe58f0bf6021855044138396bc074`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:4bdb0834a42c22fa543fe4497215113db9aa55197d55597fb16c6cfd2a7ec22a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14225578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0631ff02e5e01fcee0ebd5387c53f8dca8198463556fd98f569e3454b0bab`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:47 GMT
ADD file:0f70e0f0075bee67acb44e5ef01bf6b9df1f69a25b7aa6fd15bd5bb6ec5bcc9f in / 
# Mon, 04 Apr 2022 23:41:48 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:19:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:19:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 06:19:20 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 06:19:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 06:19:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:19:22 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 06:19:23 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 06:19:23 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 06:19:23 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 80
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 443
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 06:19:25 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 06:19:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6f6a6c77b1bd5dfb3e759efaa292f964f197ae4b96be74d80ef059f87317997a`  
		Last Modified: Mon, 04 Apr 2022 23:42:47 GMT  
		Size: 2.6 MB (2604075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46276fc79092fffc5c0d503ca8733315c8e4002c4e7da79b2383f14c70565746`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 291.8 KB (291788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2e4510a7572a45fad3f051c23678f720057b3bb38d17381f62903aa621c6eb`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf64cfe3d9d0d01f6a1856e4850cd31a634fbb44641472deac6358fdc04352ea`  
		Last Modified: Tue, 05 Apr 2022 06:20:34 GMT  
		Size: 11.3 MB (11323733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363873546085e9612ff25fa067fed8e0038220696a865e645e8046a79035fc99`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:15e576e7d00b1f41a648c5295a03677c24da5fede09131edcb1e6d809c7dc8aa
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
$ docker pull caddy@sha256:c8555e2ca66576a4404c2b5f31d843a5378dea6134acb500502901b563efebcf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14842034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ace180df3e668bd7937be4555305fdb7686c68acf2b5514665e2bac99bd266a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:24:48 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 04:24:50 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 04:24:50 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 04:24:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 04:24:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:24:52 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 04:24:52 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 04:24:52 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 04:24:53 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 80
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 443
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 04:24:54 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 04:24:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe024ea85c2d7fb47ce4f044038d4227cee2a982bca3e26a0ea4772b8b652f9a`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 291.2 KB (291230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438e4a77a6e9c40c3bf1fb392618ac596307733f97d294edb86383ce8ff7e51d`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6d2ebbfc8548ecc1dbf4c7568459e52549b81522cb450d42ada1bf82513a8d`  
		Last Modified: Tue, 05 Apr 2022 04:25:34 GMT  
		Size: 11.7 MB (11726452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c5f60dbd2d0286f964c9769a4a3396935a60d0d71ac0e3f8eea5c4c20711fb`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:01ed10f530dfa4af76fa0f13bcdde451a934fbd3a2d77e4cfa72dbc5587ac6f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14049473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c322930340bb73e0796df576638a0214eda5499c8f9b79e4f9af61aeb4da4d2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:14:11 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:14:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 03:14:14 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 03:14:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 03:14:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 03:14:20 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 03:14:21 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 03:14:21 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 03:14:22 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 03:14:22 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 03:14:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 03:14:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 03:14:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 03:14:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 03:14:26 GMT
EXPOSE 80
# Tue, 05 Apr 2022 03:14:26 GMT
EXPOSE 443
# Tue, 05 Apr 2022 03:14:27 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 03:14:27 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 03:14:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d650105deec735ac6dce2611f274a6cf2d9f60fc811167dd6d644e281a38f5`  
		Last Modified: Tue, 05 Apr 2022 03:17:39 GMT  
		Size: 291.7 KB (291653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f3d66a6432942b556bf7a077c220319708b7fc75279695b4b05fa25166fbaf`  
		Last Modified: Tue, 05 Apr 2022 03:17:38 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5d8162ee509e3528dd82e497c4057d40064d43d532acc589b4408c08d2b144`  
		Last Modified: Tue, 05 Apr 2022 03:17:46 GMT  
		Size: 11.1 MB (11125784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0ebc13031265ef07e50f9c7658d00ce8d28c00affdf202b6dd849558f06ad6`  
		Last Modified: Tue, 05 Apr 2022 03:17:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:80bf5252e7e8c04e9ff83dd861f7ee4e81bad7b2b52b5c78a43abf0c95818cf7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dddbbfbbc47ddc2ad3b96622c35ee55ec3eecd5e37cde28c3dfe807ac0827ba`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:52 GMT
ADD file:97f7b59ed0e40e7771daab294820763a7bb86c843317be55725baf1cab39aa12 in / 
# Mon, 04 Apr 2022 23:57:52 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:32:17 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:32:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 06:32:20 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 06:32:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 06:32:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:32:26 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 06:32:26 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 06:32:27 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 06:32:27 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 06:32:28 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 06:32:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 06:32:30 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 06:32:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 06:32:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 06:32:31 GMT
EXPOSE 80
# Tue, 05 Apr 2022 06:32:32 GMT
EXPOSE 443
# Tue, 05 Apr 2022 06:32:32 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 06:32:33 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 06:32:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:380010979fdd8a9a4b0bf397034a27ec6cabe61d36e9e6d460ea986f0ddaef38`  
		Last Modified: Mon, 04 Apr 2022 23:59:45 GMT  
		Size: 2.4 MB (2427969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0decd23e3d353b46346bc943e7c39f406496ebc5b14731e4575f770563ddef21`  
		Last Modified: Tue, 05 Apr 2022 06:34:41 GMT  
		Size: 290.6 KB (290637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf30d07056a9a35092dc8a190963a5d19c14fce0543c6f6cfed98fc9a687dc5f`  
		Last Modified: Tue, 05 Apr 2022 06:34:40 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbde61fe85af3ebca0218d5ca1f9b5b6d095a57aedc0d7a827ba511e2143629`  
		Last Modified: Tue, 05 Apr 2022 06:34:48 GMT  
		Size: 11.1 MB (11106715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9e55ef38253194b94160973edf2d58fbb2df74561e28d5e7894a3865f9daf8`  
		Last Modified: Tue, 05 Apr 2022 06:34:40 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:e526f540c45973c7a3a4585918890beceac9f0916e124daea3bf4e8b7a1e09b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13753199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2982d1a58becf38a1cf55541dcd74c1b096e8a02bb2060c30540fd3246e46e4f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:11:38 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:11:40 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 03:11:41 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 03:11:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 03:11:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 03:11:45 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 03:11:46 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 03:11:47 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 03:11:48 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 03:11:49 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 03:11:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 03:11:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 03:11:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 03:11:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 03:11:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 03:11:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 03:11:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 03:11:57 GMT
EXPOSE 80
# Tue, 05 Apr 2022 03:11:58 GMT
EXPOSE 443
# Tue, 05 Apr 2022 03:11:59 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 03:12:00 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 03:12:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b907f83114020e794129b34363890abf552785b8d964dbd3546272cc805702ce`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 291.3 KB (291281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988559859d9a4661992cbcefddba5b3d7a16de6c22547a962024f04767e6debf`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 5.7 KB (5748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7769260cde91250d6c68897788b078fea0a63b1254082d2923affeb859224a92`  
		Last Modified: Tue, 05 Apr 2022 03:13:22 GMT  
		Size: 10.7 MB (10738627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0143e63583cae9b0bc2b0048073b6c52476761cbeffa8e6aeca59d227ae0ee2`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:0f4502864c2fae9298130a48ec4ca4351af0787bee15fd4cb5307b7b83e87dd8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13416150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b308dba8382e868224f828f88958151f9c1af01332da44ca296967f8bf09d40b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:44 GMT
ADD file:0b9367758b91930d9d69fd3901262e3a696f7a9f6d9e209e35da83ea6e785837 in / 
# Tue, 05 Apr 2022 00:23:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:07:02 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 07:07:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 07:07:12 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 07:07:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 07:07:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:07:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 07:07:31 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 07:07:33 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 07:07:36 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 07:07:40 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 07:07:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 07:07:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 07:07:47 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 07:07:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 07:07:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 07:07:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 07:07:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 07:08:03 GMT
EXPOSE 80
# Tue, 05 Apr 2022 07:08:06 GMT
EXPOSE 443
# Tue, 05 Apr 2022 07:08:08 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 07:08:10 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 07:08:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ee5f6345565e7aeda814a5c097612cacb0a74186b1f01bf5199e1b812b5d3065`  
		Last Modified: Tue, 05 Apr 2022 00:25:06 GMT  
		Size: 2.8 MB (2814167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8affbe739a71e3875810f257750034ec7a6ee3f2f2c0094f3bcb3ed8a45520b`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 293.7 KB (293710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc927cb41936aaa5bfefa5dc4d654b7193fd568f619707120a5491c620906fc1`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8646c35213c358f518a4d76b75742b5930acec5d12cbd6c75d0a7e217698cee`  
		Last Modified: Tue, 05 Apr 2022 07:11:06 GMT  
		Size: 10.3 MB (10302288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346269e52424a62ec14d10c3e1db1aeb9cefe58f0bf6021855044138396bc074`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:4bdb0834a42c22fa543fe4497215113db9aa55197d55597fb16c6cfd2a7ec22a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14225578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0631ff02e5e01fcee0ebd5387c53f8dca8198463556fd98f569e3454b0bab`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:47 GMT
ADD file:0f70e0f0075bee67acb44e5ef01bf6b9df1f69a25b7aa6fd15bd5bb6ec5bcc9f in / 
# Mon, 04 Apr 2022 23:41:48 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:19:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:19:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 06:19:20 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 06:19:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 06:19:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:19:22 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 06:19:23 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 06:19:23 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 06:19:23 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 80
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 443
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 06:19:25 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 06:19:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6f6a6c77b1bd5dfb3e759efaa292f964f197ae4b96be74d80ef059f87317997a`  
		Last Modified: Mon, 04 Apr 2022 23:42:47 GMT  
		Size: 2.6 MB (2604075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46276fc79092fffc5c0d503ca8733315c8e4002c4e7da79b2383f14c70565746`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 291.8 KB (291788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2e4510a7572a45fad3f051c23678f720057b3bb38d17381f62903aa621c6eb`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf64cfe3d9d0d01f6a1856e4850cd31a634fbb44641472deac6358fdc04352ea`  
		Last Modified: Tue, 05 Apr 2022 06:20:34 GMT  
		Size: 11.3 MB (11323733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363873546085e9612ff25fa067fed8e0038220696a865e645e8046a79035fc99`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:7330e2d325fa6b9d0f64526b31373722f60520a8e29131ef0c48537273d15a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2686; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:80234a9cd66af5a747785958e8dc683a43dfe946b9b98c9ffe2806fa4ac5422e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121342541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa54d86d06fba28c500cfe838c151623b997c5e35b2af29ea8b70b6a92a7fb8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:32:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 05:32:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 05:32:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:37:30 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 05:39:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 05:39:29 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 05:39:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:39:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 05:39:30 GMT
WORKDIR /go
# Tue, 05 Apr 2022 15:45:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 15:45:54 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 15:45:54 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 15:45:54 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 15:45:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 15:45:55 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 15:45:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc419b0ee22d1bb5f3b95a57b2edc733b7b585277f8101db7b2c9b53605c1b`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 272.0 KB (271965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc292e5bacdd8b97a1632a82d0fd0ee6c2692409bd4b35cb9e7e652efbc7c8`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dea7a3ad9148616176ac7fd686181a6e3c4eaac3746166e678a11017e4d32d9`  
		Last Modified: Tue, 05 Apr 2022 05:43:55 GMT  
		Size: 110.2 MB (110188123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35228ee6d672a4ef2501b746851ae8dc63cdc2612057a726a7affcd9d7d9f08`  
		Last Modified: Tue, 05 Apr 2022 05:43:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431098d05c7f64b1b215f6e58d58584efa1b85c22de1e46eabdf9f41c9a31550`  
		Last Modified: Tue, 05 Apr 2022 15:46:24 GMT  
		Size: 6.8 MB (6821467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16611ed52579f2526e4c8ef7d32963cc52bdf84706c195aaea01082575369d8d`  
		Last Modified: Tue, 05 Apr 2022 15:46:23 GMT  
		Size: 1.2 MB (1245713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56bc9474ab53335737725ec3c82362fd8d085309b54710629fec01fac471c3d`  
		Last Modified: Tue, 05 Apr 2022 15:46:22 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:dcf5e840b541953183c28551fb8ad10bcb3a75ad0eb6010cf518751eb246cdb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115819309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b820bb6f118cf0da95b1daa66e903131e906c6f7937eeb823bea92880a827ed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:39:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 11:59:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 11:59:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 12:07:43 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 12:10:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 12:10:56 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 12:10:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 12:10:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 12:10:58 GMT
WORKDIR /go
# Tue, 05 Apr 2022 18:47:17 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 18:47:18 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 18:47:18 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 18:47:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 18:47:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 18:47:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 18:47:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560305eea4784da98378676b22f9871093d6a4d7eb88292accc17f0cfd6b12ea`  
		Last Modified: Tue, 05 Apr 2022 11:40:22 GMT  
		Size: 272.1 KB (272138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145a805e932abbcca6b77ad458c7ac26275ff4f23af9912d2c4d3dac9eef4cf8`  
		Last Modified: Tue, 05 Apr 2022 12:15:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc18cdc5d172f77e8e9ab98b63b490a7ee5597737555f86ab3df9580d7603038`  
		Last Modified: Tue, 05 Apr 2022 12:20:29 GMT  
		Size: 105.1 MB (105068577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a00aaf29b7cc08e00fa3ad26938794099e739101e45a4efbd80da84b4b59e8`  
		Last Modified: Tue, 05 Apr 2022 12:19:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce9447fafc122cfcae03e938e9b3bf3750eda3436a83625bc1229d67e6f3526`  
		Last Modified: Tue, 05 Apr 2022 18:49:07 GMT  
		Size: 6.7 MB (6677398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb4981b5917a068228e1b12e5afe118826c4ebb0880a39e0de01773e1a9b6b`  
		Last Modified: Tue, 05 Apr 2022 18:49:04 GMT  
		Size: 1.2 MB (1178510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50ceda04f269611e045f72b6f59cd9458e489675973c2a26d9ba4c92417c110`  
		Last Modified: Tue, 05 Apr 2022 18:49:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:f067c336bf9a0f6755735e5dbd07fdbce24f00d4ded39ae414599dd0707f5909
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114678400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e18d0d8561f2864f5ae2184d369b7ed78f855c8098e12b18e3e66e9ed1d702`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:19:56 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:19:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:19:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:28:26 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 09:31:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 09:31:38 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 09:31:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:31:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 09:31:40 GMT
WORKDIR /go
# Wed, 06 Apr 2022 02:23:29 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 06 Apr 2022 02:23:29 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 06 Apr 2022 02:23:30 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 06 Apr 2022 02:23:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Apr 2022 02:23:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 06 Apr 2022 02:23:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 06 Apr 2022 02:23:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f68dacdb1dfe1ed299ab3e43e478a27f0977380bbefc4c7ca5723758dbac6`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 271.1 KB (271116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431ad618c287090e481554b57afdc0383f065b5bbfc0ccdcefc6518e1a8331e`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1c19e6ea71a7140e1f92aaf1ca20998b7875298f5f0aecdad1849acea539e9`  
		Last Modified: Tue, 05 Apr 2022 09:43:01 GMT  
		Size: 104.9 MB (104853355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d18ca61f70738e42fc01d4076606b8ef68be3c58058c1922e2b44987e87a15`  
		Last Modified: Tue, 05 Apr 2022 09:41:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d951a4c4c0e205bd2d3656382822e0ad97c4ee98c7cc185614d9363d5b7b18df`  
		Last Modified: Wed, 06 Apr 2022 02:25:20 GMT  
		Size: 6.0 MB (5952176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b38ba848bdb94dd4baa0c3e1ed84c6c0f039346dbd2904d5e257b874558a07`  
		Last Modified: Wed, 06 Apr 2022 02:25:18 GMT  
		Size: 1.2 MB (1176713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426c201900d8690c727d61a628a8540811cafc07c1ed656aeb066b7745707c7b`  
		Last Modified: Wed, 06 Apr 2022 02:25:18 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:7b6beab6198241afad1f6660a5083478efd4f1e92ff2edccc566bca27905c310
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115488051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ee73e0e2ed794915b2af927e5458f4bad17835e41f615dab40db89f343bdf0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:38:07 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 07:38:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:38:08 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:41:43 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 07:43:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 07:43:02 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 07:43:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 07:43:05 GMT
WORKDIR /go
# Tue, 05 Apr 2022 17:39:06 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 17:39:07 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 17:39:08 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 17:39:09 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 17:39:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 17:39:13 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 17:39:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7637d0a7b497b253b73e807a5e676ba3f0750afafa9e1a4c61260513feb321f`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 271.8 KB (271764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda57b85efde0ed435315f4f74625e7a055107aa29e8c91a313ca6d525fb709c`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d20097de21a08b3879d9d8acda7ea55af524f6cb8cf3d8526c7ad583992e7f`  
		Last Modified: Tue, 05 Apr 2022 07:47:32 GMT  
		Size: 104.4 MB (104424495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662c5a329cf0f527093cef90725754463b5ab87a23be5a91edff92a844e76c37`  
		Last Modified: Tue, 05 Apr 2022 07:47:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f1e21bd0bbbfa99416af4431f653df5121e14b29364c870d86362268419104`  
		Last Modified: Tue, 05 Apr 2022 17:40:06 GMT  
		Size: 6.9 MB (6925952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e5c2ce8d4fcaae75fbb7497ef4b24c4b192aafbb3384f7a8221b0c1213401`  
		Last Modified: Tue, 05 Apr 2022 17:40:05 GMT  
		Size: 1.1 MB (1148677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4162b5640fb2e218682c6e2bfb93a2f2ad6c9ffbe57ecec50ca91554eefefa`  
		Last Modified: Tue, 05 Apr 2022 17:40:05 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:f0523e893e89caa4a62fb934156846b72fa1e93191eb22fe3e2648b4416da80e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114312516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066aed791277682729d033b831d7ce9039dba3849abd6e0cf881b8992fd75b70`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:50:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:50:19 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:50:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:57:52 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 10:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 10:00:43 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 10:00:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 10:00:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 10:00:55 GMT
WORKDIR /go
# Wed, 06 Apr 2022 02:52:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 06 Apr 2022 02:53:02 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 06 Apr 2022 02:53:05 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 06 Apr 2022 02:53:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Apr 2022 02:53:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 06 Apr 2022 02:53:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 06 Apr 2022 02:53:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcdc2e904e95f788aa4c66c5ce746890d6a02abca4c94711443f5c688b61ebf`  
		Last Modified: Tue, 05 Apr 2022 10:06:11 GMT  
		Size: 274.2 KB (274171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04802687d9aa11413122df45eb15c7d7f85937270997b441d1c6a09001730453`  
		Last Modified: Tue, 05 Apr 2022 10:06:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce62b250e0aee7f0aec0715e9113355ac5a4781c1eaf0d4bea6fcdf4073068f8`  
		Last Modified: Tue, 05 Apr 2022 10:08:01 GMT  
		Size: 102.8 MB (102784652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c7dcfaac085766cdaa5fce90fb5c664130f22fa3f6005b3cebddf45a4e2b9b`  
		Last Modified: Tue, 05 Apr 2022 10:07:43 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7a86ae8bfd11a7525de064d7143eed347098156c965551db06b0da1fab2f67`  
		Last Modified: Wed, 06 Apr 2022 02:54:45 GMT  
		Size: 7.3 MB (7320952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33cc607466c85109d67b2a8aefc6a137b9aebe631f8e33435b2618033bb3737`  
		Last Modified: Wed, 06 Apr 2022 02:54:45 GMT  
		Size: 1.1 MB (1120840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3107bf51b5f81e988fc6b01377bdab7efc085a95bfa0b866d40cd7c18bb23a6d`  
		Last Modified: Wed, 06 Apr 2022 02:54:44 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:7862e378800416206aa5844ed260f8cb64c1537299e481e5004521024727c011
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118747451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d95993f92df472d91942633064b5db1e229654fbf9e15e574f235f732d2171`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:08:51 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 06:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:44:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:48:26 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 06:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 06:49:56 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 06:49:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:49:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 06:49:57 GMT
WORKDIR /go
# Tue, 05 Apr 2022 14:02:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 14:02:02 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 14:02:02 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 14:02:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 14:02:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 14:02:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 14:02:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72593bb761a2ce336603e9e84973d1e284f39e0188e758ad8bc22c45cd9b6395`  
		Last Modified: Tue, 05 Apr 2022 06:09:13 GMT  
		Size: 272.3 KB (272267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf480933488ffcb2c9c9269292e2e3d643bea6eeb04cf948790ca50666a61c8`  
		Last Modified: Tue, 05 Apr 2022 06:53:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b3e51e0eff0c3e6118a6448425ada0b8e1725d738559d5b5e29ef58c570e8d`  
		Last Modified: Tue, 05 Apr 2022 06:54:30 GMT  
		Size: 107.7 MB (107739421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86765c73189fadce4ca276af5f7d9440213d5986a9687b648a51d45978e3a8c4`  
		Last Modified: Tue, 05 Apr 2022 06:54:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f50aeaf488b81d4c5d54c453b47637b6fbdfae9ca014728018463ce30aa78b`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 6.9 MB (6930892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca74c757745c5b39f811e1b5ed2a0fe0b8f2de2ab52b23dd01d8aaa71540d27b`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 1.2 MB (1203782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e4f898506aece97cc68bfd9e1a347bd072242e4672eee262eae303b3e0b6e9`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:568847e6f37af8e2f55d5d780b100e1dbfcbb9178896eb9d8f2b57ecf966d39c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888394051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20261b1174a82d98f801248da692dc2862f133c7cea9e52758b2c17b3567abc3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 13:17:25 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Mar 2022 13:17:26 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Mar 2022 13:17:27 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Mar 2022 13:17:28 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Mar 2022 13:19:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:19:56 GMT
ENV GOPATH=C:\go
# Wed, 09 Mar 2022 13:20:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Mar 2022 13:35:10 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 09 Mar 2022 13:38:26 GMT
RUN $url = 'https://dl.google.com/go/go1.17.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '85ccf2608dca6ea9a46b6538c9e75e7cf2aebdf502379843b248e26b8bb110be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:38:28 GMT
WORKDIR C:\go
# Wed, 09 Mar 2022 18:27:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Mar 2022 23:14:28 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 23:14:29 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 23:14:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 23:15:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('fc6f2a7feb8f0936a0e04d3c9ea26d0404c2f4907eb436eb60e33152c22c1211f851c46606573fcb5c3334f8cc4f7f810b28b917a9f313f6454d1c5cd0f50f8a')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 10 Mar 2022 23:15:41 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7705bbffd7dc00934e935de0e00e09a7b0da55d66c596622f094495478dd71`  
		Last Modified: Wed, 09 Mar 2022 14:04:13 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be7ff0bb187d149a5cf3c76e1ec444d0e07c6606f67b2c921c67ec91829ea03`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876223f25b257577440a80fdee021b43c33ce3c56be9a20b2ddeaede95240522`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991eea244b9c3a1849c84748425dd9e9fbf9ec359ad9329796131b929239ffa4`  
		Last Modified: Wed, 09 Mar 2022 14:04:11 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b4c7c9740eb99bf626b312aa69396db3d186c5bd0e092b01c078ca7248e386`  
		Last Modified: Wed, 09 Mar 2022 14:04:40 GMT  
		Size: 25.5 MB (25454695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6c8a4d4848c21636a48a69a569a5372ec4890ea029f1f620dda76078bdcef`  
		Last Modified: Wed, 09 Mar 2022 14:04:09 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac6d527939082add6d21652ba4888acc5a6e7607365168d8e61fb1485339cb`  
		Last Modified: Wed, 09 Mar 2022 14:04:10 GMT  
		Size: 313.6 KB (313592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37aeceb8c2e5bb3c500129bcf20c3f8aea8c68c353e6714a63a225ed1546e8a1`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d88cd595dc7580d72420b7288c52d4b32201045a13dda1a7b943d9a3468adef`  
		Last Modified: Wed, 09 Mar 2022 14:13:05 GMT  
		Size: 145.5 MB (145488847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be492983ee2b2c9128ce0c732c441ae5fbd203cdb71c94faa253c24b01750c90`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa7b09ca61eb1fbafacee427b430b0879ad4da23e62e430a3fe6a66f181f642`  
		Last Modified: Wed, 09 Mar 2022 18:30:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74014ffde8e1a1677cd81e965bcd2b1f5287bcbf682bbce3bdd125052cd04f29`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43e7b3a6c47e8c9bba8e4ba91d722cd9e491f2df12d5e277356e2b8fc070ba8`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceffc29f93380b6942a245303d5af87875d60351e4c897405f358f018b61b863`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae9e05c08471d9a54c2b46c4f892226ab1eab63b6efd326c44b50bceffb11f2`  
		Last Modified: Thu, 10 Mar 2022 23:22:56 GMT  
		Size: 1.7 MB (1665933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd386d40eef8a252639d03e1486ff30ff8f77cef626bf0592cc7853eb633c7d`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:54e2deab0aa5245b222cba916d21cb85acb53793dbb1651e3c7a6e7eb6240089
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
$ docker pull caddy@sha256:80234a9cd66af5a747785958e8dc683a43dfe946b9b98c9ffe2806fa4ac5422e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121342541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa54d86d06fba28c500cfe838c151623b997c5e35b2af29ea8b70b6a92a7fb8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:32:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 05:32:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 05:32:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:37:30 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 05:39:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 05:39:29 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 05:39:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:39:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 05:39:30 GMT
WORKDIR /go
# Tue, 05 Apr 2022 15:45:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 15:45:54 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 15:45:54 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 15:45:54 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 15:45:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 15:45:55 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 15:45:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc419b0ee22d1bb5f3b95a57b2edc733b7b585277f8101db7b2c9b53605c1b`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 272.0 KB (271965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc292e5bacdd8b97a1632a82d0fd0ee6c2692409bd4b35cb9e7e652efbc7c8`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dea7a3ad9148616176ac7fd686181a6e3c4eaac3746166e678a11017e4d32d9`  
		Last Modified: Tue, 05 Apr 2022 05:43:55 GMT  
		Size: 110.2 MB (110188123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35228ee6d672a4ef2501b746851ae8dc63cdc2612057a726a7affcd9d7d9f08`  
		Last Modified: Tue, 05 Apr 2022 05:43:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431098d05c7f64b1b215f6e58d58584efa1b85c22de1e46eabdf9f41c9a31550`  
		Last Modified: Tue, 05 Apr 2022 15:46:24 GMT  
		Size: 6.8 MB (6821467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16611ed52579f2526e4c8ef7d32963cc52bdf84706c195aaea01082575369d8d`  
		Last Modified: Tue, 05 Apr 2022 15:46:23 GMT  
		Size: 1.2 MB (1245713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56bc9474ab53335737725ec3c82362fd8d085309b54710629fec01fac471c3d`  
		Last Modified: Tue, 05 Apr 2022 15:46:22 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:dcf5e840b541953183c28551fb8ad10bcb3a75ad0eb6010cf518751eb246cdb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115819309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b820bb6f118cf0da95b1daa66e903131e906c6f7937eeb823bea92880a827ed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:39:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 11:59:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 11:59:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 12:07:43 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 12:10:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 12:10:56 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 12:10:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 12:10:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 12:10:58 GMT
WORKDIR /go
# Tue, 05 Apr 2022 18:47:17 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 18:47:18 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 18:47:18 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 18:47:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 18:47:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 18:47:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 18:47:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560305eea4784da98378676b22f9871093d6a4d7eb88292accc17f0cfd6b12ea`  
		Last Modified: Tue, 05 Apr 2022 11:40:22 GMT  
		Size: 272.1 KB (272138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145a805e932abbcca6b77ad458c7ac26275ff4f23af9912d2c4d3dac9eef4cf8`  
		Last Modified: Tue, 05 Apr 2022 12:15:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc18cdc5d172f77e8e9ab98b63b490a7ee5597737555f86ab3df9580d7603038`  
		Last Modified: Tue, 05 Apr 2022 12:20:29 GMT  
		Size: 105.1 MB (105068577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a00aaf29b7cc08e00fa3ad26938794099e739101e45a4efbd80da84b4b59e8`  
		Last Modified: Tue, 05 Apr 2022 12:19:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce9447fafc122cfcae03e938e9b3bf3750eda3436a83625bc1229d67e6f3526`  
		Last Modified: Tue, 05 Apr 2022 18:49:07 GMT  
		Size: 6.7 MB (6677398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb4981b5917a068228e1b12e5afe118826c4ebb0880a39e0de01773e1a9b6b`  
		Last Modified: Tue, 05 Apr 2022 18:49:04 GMT  
		Size: 1.2 MB (1178510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50ceda04f269611e045f72b6f59cd9458e489675973c2a26d9ba4c92417c110`  
		Last Modified: Tue, 05 Apr 2022 18:49:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:f067c336bf9a0f6755735e5dbd07fdbce24f00d4ded39ae414599dd0707f5909
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114678400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e18d0d8561f2864f5ae2184d369b7ed78f855c8098e12b18e3e66e9ed1d702`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:19:56 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:19:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:19:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:28:26 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 09:31:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 09:31:38 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 09:31:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:31:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 09:31:40 GMT
WORKDIR /go
# Wed, 06 Apr 2022 02:23:29 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 06 Apr 2022 02:23:29 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 06 Apr 2022 02:23:30 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 06 Apr 2022 02:23:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Apr 2022 02:23:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 06 Apr 2022 02:23:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 06 Apr 2022 02:23:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f68dacdb1dfe1ed299ab3e43e478a27f0977380bbefc4c7ca5723758dbac6`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 271.1 KB (271116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431ad618c287090e481554b57afdc0383f065b5bbfc0ccdcefc6518e1a8331e`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1c19e6ea71a7140e1f92aaf1ca20998b7875298f5f0aecdad1849acea539e9`  
		Last Modified: Tue, 05 Apr 2022 09:43:01 GMT  
		Size: 104.9 MB (104853355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d18ca61f70738e42fc01d4076606b8ef68be3c58058c1922e2b44987e87a15`  
		Last Modified: Tue, 05 Apr 2022 09:41:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d951a4c4c0e205bd2d3656382822e0ad97c4ee98c7cc185614d9363d5b7b18df`  
		Last Modified: Wed, 06 Apr 2022 02:25:20 GMT  
		Size: 6.0 MB (5952176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b38ba848bdb94dd4baa0c3e1ed84c6c0f039346dbd2904d5e257b874558a07`  
		Last Modified: Wed, 06 Apr 2022 02:25:18 GMT  
		Size: 1.2 MB (1176713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426c201900d8690c727d61a628a8540811cafc07c1ed656aeb066b7745707c7b`  
		Last Modified: Wed, 06 Apr 2022 02:25:18 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:7b6beab6198241afad1f6660a5083478efd4f1e92ff2edccc566bca27905c310
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115488051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ee73e0e2ed794915b2af927e5458f4bad17835e41f615dab40db89f343bdf0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:38:07 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 07:38:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:38:08 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:41:43 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 07:43:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 07:43:02 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 07:43:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 07:43:05 GMT
WORKDIR /go
# Tue, 05 Apr 2022 17:39:06 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 17:39:07 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 17:39:08 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 17:39:09 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 17:39:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 17:39:13 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 17:39:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7637d0a7b497b253b73e807a5e676ba3f0750afafa9e1a4c61260513feb321f`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 271.8 KB (271764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda57b85efde0ed435315f4f74625e7a055107aa29e8c91a313ca6d525fb709c`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d20097de21a08b3879d9d8acda7ea55af524f6cb8cf3d8526c7ad583992e7f`  
		Last Modified: Tue, 05 Apr 2022 07:47:32 GMT  
		Size: 104.4 MB (104424495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662c5a329cf0f527093cef90725754463b5ab87a23be5a91edff92a844e76c37`  
		Last Modified: Tue, 05 Apr 2022 07:47:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f1e21bd0bbbfa99416af4431f653df5121e14b29364c870d86362268419104`  
		Last Modified: Tue, 05 Apr 2022 17:40:06 GMT  
		Size: 6.9 MB (6925952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e5c2ce8d4fcaae75fbb7497ef4b24c4b192aafbb3384f7a8221b0c1213401`  
		Last Modified: Tue, 05 Apr 2022 17:40:05 GMT  
		Size: 1.1 MB (1148677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4162b5640fb2e218682c6e2bfb93a2f2ad6c9ffbe57ecec50ca91554eefefa`  
		Last Modified: Tue, 05 Apr 2022 17:40:05 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:f0523e893e89caa4a62fb934156846b72fa1e93191eb22fe3e2648b4416da80e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114312516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066aed791277682729d033b831d7ce9039dba3849abd6e0cf881b8992fd75b70`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:50:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:50:19 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:50:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:57:52 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 10:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 10:00:43 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 10:00:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 10:00:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 10:00:55 GMT
WORKDIR /go
# Wed, 06 Apr 2022 02:52:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 06 Apr 2022 02:53:02 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 06 Apr 2022 02:53:05 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 06 Apr 2022 02:53:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Apr 2022 02:53:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 06 Apr 2022 02:53:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 06 Apr 2022 02:53:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcdc2e904e95f788aa4c66c5ce746890d6a02abca4c94711443f5c688b61ebf`  
		Last Modified: Tue, 05 Apr 2022 10:06:11 GMT  
		Size: 274.2 KB (274171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04802687d9aa11413122df45eb15c7d7f85937270997b441d1c6a09001730453`  
		Last Modified: Tue, 05 Apr 2022 10:06:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce62b250e0aee7f0aec0715e9113355ac5a4781c1eaf0d4bea6fcdf4073068f8`  
		Last Modified: Tue, 05 Apr 2022 10:08:01 GMT  
		Size: 102.8 MB (102784652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c7dcfaac085766cdaa5fce90fb5c664130f22fa3f6005b3cebddf45a4e2b9b`  
		Last Modified: Tue, 05 Apr 2022 10:07:43 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7a86ae8bfd11a7525de064d7143eed347098156c965551db06b0da1fab2f67`  
		Last Modified: Wed, 06 Apr 2022 02:54:45 GMT  
		Size: 7.3 MB (7320952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33cc607466c85109d67b2a8aefc6a137b9aebe631f8e33435b2618033bb3737`  
		Last Modified: Wed, 06 Apr 2022 02:54:45 GMT  
		Size: 1.1 MB (1120840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3107bf51b5f81e988fc6b01377bdab7efc085a95bfa0b866d40cd7c18bb23a6d`  
		Last Modified: Wed, 06 Apr 2022 02:54:44 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:7862e378800416206aa5844ed260f8cb64c1537299e481e5004521024727c011
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118747451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d95993f92df472d91942633064b5db1e229654fbf9e15e574f235f732d2171`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:08:51 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 06:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:44:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:48:26 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 06:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 06:49:56 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 06:49:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:49:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 06:49:57 GMT
WORKDIR /go
# Tue, 05 Apr 2022 14:02:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 14:02:02 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 14:02:02 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 14:02:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 14:02:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 14:02:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 14:02:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72593bb761a2ce336603e9e84973d1e284f39e0188e758ad8bc22c45cd9b6395`  
		Last Modified: Tue, 05 Apr 2022 06:09:13 GMT  
		Size: 272.3 KB (272267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf480933488ffcb2c9c9269292e2e3d643bea6eeb04cf948790ca50666a61c8`  
		Last Modified: Tue, 05 Apr 2022 06:53:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b3e51e0eff0c3e6118a6448425ada0b8e1725d738559d5b5e29ef58c570e8d`  
		Last Modified: Tue, 05 Apr 2022 06:54:30 GMT  
		Size: 107.7 MB (107739421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86765c73189fadce4ca276af5f7d9440213d5986a9687b648a51d45978e3a8c4`  
		Last Modified: Tue, 05 Apr 2022 06:54:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f50aeaf488b81d4c5d54c453b47637b6fbdfae9ca014728018463ce30aa78b`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 6.9 MB (6930892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca74c757745c5b39f811e1b5ed2a0fe0b8f2de2ab52b23dd01d8aaa71540d27b`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 1.2 MB (1203782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e4f898506aece97cc68bfd9e1a347bd072242e4672eee262eae303b3e0b6e9`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:276530503290de9ae8be7471e975d5db1e0d286e99d48317b675cec03c7c2fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:568847e6f37af8e2f55d5d780b100e1dbfcbb9178896eb9d8f2b57ecf966d39c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888394051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20261b1174a82d98f801248da692dc2862f133c7cea9e52758b2c17b3567abc3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 13:17:25 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Mar 2022 13:17:26 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Mar 2022 13:17:27 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Mar 2022 13:17:28 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Mar 2022 13:19:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:19:56 GMT
ENV GOPATH=C:\go
# Wed, 09 Mar 2022 13:20:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Mar 2022 13:35:10 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 09 Mar 2022 13:38:26 GMT
RUN $url = 'https://dl.google.com/go/go1.17.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '85ccf2608dca6ea9a46b6538c9e75e7cf2aebdf502379843b248e26b8bb110be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:38:28 GMT
WORKDIR C:\go
# Wed, 09 Mar 2022 18:27:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Mar 2022 23:14:28 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 23:14:29 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 23:14:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 23:15:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('fc6f2a7feb8f0936a0e04d3c9ea26d0404c2f4907eb436eb60e33152c22c1211f851c46606573fcb5c3334f8cc4f7f810b28b917a9f313f6454d1c5cd0f50f8a')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 10 Mar 2022 23:15:41 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7705bbffd7dc00934e935de0e00e09a7b0da55d66c596622f094495478dd71`  
		Last Modified: Wed, 09 Mar 2022 14:04:13 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be7ff0bb187d149a5cf3c76e1ec444d0e07c6606f67b2c921c67ec91829ea03`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876223f25b257577440a80fdee021b43c33ce3c56be9a20b2ddeaede95240522`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991eea244b9c3a1849c84748425dd9e9fbf9ec359ad9329796131b929239ffa4`  
		Last Modified: Wed, 09 Mar 2022 14:04:11 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b4c7c9740eb99bf626b312aa69396db3d186c5bd0e092b01c078ca7248e386`  
		Last Modified: Wed, 09 Mar 2022 14:04:40 GMT  
		Size: 25.5 MB (25454695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6c8a4d4848c21636a48a69a569a5372ec4890ea029f1f620dda76078bdcef`  
		Last Modified: Wed, 09 Mar 2022 14:04:09 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac6d527939082add6d21652ba4888acc5a6e7607365168d8e61fb1485339cb`  
		Last Modified: Wed, 09 Mar 2022 14:04:10 GMT  
		Size: 313.6 KB (313592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37aeceb8c2e5bb3c500129bcf20c3f8aea8c68c353e6714a63a225ed1546e8a1`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d88cd595dc7580d72420b7288c52d4b32201045a13dda1a7b943d9a3468adef`  
		Last Modified: Wed, 09 Mar 2022 14:13:05 GMT  
		Size: 145.5 MB (145488847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be492983ee2b2c9128ce0c732c441ae5fbd203cdb71c94faa253c24b01750c90`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa7b09ca61eb1fbafacee427b430b0879ad4da23e62e430a3fe6a66f181f642`  
		Last Modified: Wed, 09 Mar 2022 18:30:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74014ffde8e1a1677cd81e965bcd2b1f5287bcbf682bbce3bdd125052cd04f29`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43e7b3a6c47e8c9bba8e4ba91d722cd9e491f2df12d5e277356e2b8fc070ba8`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceffc29f93380b6942a245303d5af87875d60351e4c897405f358f018b61b863`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae9e05c08471d9a54c2b46c4f892226ab1eab63b6efd326c44b50bceffb11f2`  
		Last Modified: Thu, 10 Mar 2022 23:22:56 GMT  
		Size: 1.7 MB (1665933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd386d40eef8a252639d03e1486ff30ff8f77cef626bf0592cc7853eb633c7d`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:a3ba1d80239cc342421e0b3a6a6adba859191852e94c30047402f2ac1cc24407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:a3ba1d80239cc342421e0b3a6a6adba859191852e94c30047402f2ac1cc24407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6`

```console
$ docker pull caddy@sha256:50a38e32a96b709de9e5112eb1909b7f03fab16959929da71f342c5bdb114641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2686; amd64

### `caddy:2.4.6` - linux; amd64

```console
$ docker pull caddy@sha256:c8555e2ca66576a4404c2b5f31d843a5378dea6134acb500502901b563efebcf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14842034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ace180df3e668bd7937be4555305fdb7686c68acf2b5514665e2bac99bd266a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:24:48 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 04:24:50 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 04:24:50 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 04:24:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 04:24:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:24:52 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 04:24:52 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 04:24:52 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 04:24:53 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 80
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 443
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 04:24:54 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 04:24:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe024ea85c2d7fb47ce4f044038d4227cee2a982bca3e26a0ea4772b8b652f9a`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 291.2 KB (291230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438e4a77a6e9c40c3bf1fb392618ac596307733f97d294edb86383ce8ff7e51d`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6d2ebbfc8548ecc1dbf4c7568459e52549b81522cb450d42ada1bf82513a8d`  
		Last Modified: Tue, 05 Apr 2022 04:25:34 GMT  
		Size: 11.7 MB (11726452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c5f60dbd2d0286f964c9769a4a3396935a60d0d71ac0e3f8eea5c4c20711fb`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; arm variant v6

```console
$ docker pull caddy@sha256:01ed10f530dfa4af76fa0f13bcdde451a934fbd3a2d77e4cfa72dbc5587ac6f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14049473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c322930340bb73e0796df576638a0214eda5499c8f9b79e4f9af61aeb4da4d2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:14:11 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:14:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 03:14:14 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 03:14:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 03:14:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 03:14:20 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 03:14:21 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 03:14:21 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 03:14:22 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 03:14:22 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 03:14:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 03:14:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 03:14:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 03:14:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 03:14:26 GMT
EXPOSE 80
# Tue, 05 Apr 2022 03:14:26 GMT
EXPOSE 443
# Tue, 05 Apr 2022 03:14:27 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 03:14:27 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 03:14:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d650105deec735ac6dce2611f274a6cf2d9f60fc811167dd6d644e281a38f5`  
		Last Modified: Tue, 05 Apr 2022 03:17:39 GMT  
		Size: 291.7 KB (291653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f3d66a6432942b556bf7a077c220319708b7fc75279695b4b05fa25166fbaf`  
		Last Modified: Tue, 05 Apr 2022 03:17:38 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5d8162ee509e3528dd82e497c4057d40064d43d532acc589b4408c08d2b144`  
		Last Modified: Tue, 05 Apr 2022 03:17:46 GMT  
		Size: 11.1 MB (11125784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0ebc13031265ef07e50f9c7658d00ce8d28c00affdf202b6dd849558f06ad6`  
		Last Modified: Tue, 05 Apr 2022 03:17:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; arm variant v7

```console
$ docker pull caddy@sha256:80bf5252e7e8c04e9ff83dd861f7ee4e81bad7b2b52b5c78a43abf0c95818cf7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dddbbfbbc47ddc2ad3b96622c35ee55ec3eecd5e37cde28c3dfe807ac0827ba`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:52 GMT
ADD file:97f7b59ed0e40e7771daab294820763a7bb86c843317be55725baf1cab39aa12 in / 
# Mon, 04 Apr 2022 23:57:52 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:32:17 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:32:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 06:32:20 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 06:32:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 06:32:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:32:26 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 06:32:26 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 06:32:27 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 06:32:27 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 06:32:28 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 06:32:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 06:32:30 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 06:32:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 06:32:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 06:32:31 GMT
EXPOSE 80
# Tue, 05 Apr 2022 06:32:32 GMT
EXPOSE 443
# Tue, 05 Apr 2022 06:32:32 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 06:32:33 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 06:32:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:380010979fdd8a9a4b0bf397034a27ec6cabe61d36e9e6d460ea986f0ddaef38`  
		Last Modified: Mon, 04 Apr 2022 23:59:45 GMT  
		Size: 2.4 MB (2427969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0decd23e3d353b46346bc943e7c39f406496ebc5b14731e4575f770563ddef21`  
		Last Modified: Tue, 05 Apr 2022 06:34:41 GMT  
		Size: 290.6 KB (290637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf30d07056a9a35092dc8a190963a5d19c14fce0543c6f6cfed98fc9a687dc5f`  
		Last Modified: Tue, 05 Apr 2022 06:34:40 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbde61fe85af3ebca0218d5ca1f9b5b6d095a57aedc0d7a827ba511e2143629`  
		Last Modified: Tue, 05 Apr 2022 06:34:48 GMT  
		Size: 11.1 MB (11106715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9e55ef38253194b94160973edf2d58fbb2df74561e28d5e7894a3865f9daf8`  
		Last Modified: Tue, 05 Apr 2022 06:34:40 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:e526f540c45973c7a3a4585918890beceac9f0916e124daea3bf4e8b7a1e09b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13753199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2982d1a58becf38a1cf55541dcd74c1b096e8a02bb2060c30540fd3246e46e4f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:11:38 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:11:40 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 03:11:41 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 03:11:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 03:11:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 03:11:45 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 03:11:46 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 03:11:47 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 03:11:48 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 03:11:49 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 03:11:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 03:11:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 03:11:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 03:11:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 03:11:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 03:11:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 03:11:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 03:11:57 GMT
EXPOSE 80
# Tue, 05 Apr 2022 03:11:58 GMT
EXPOSE 443
# Tue, 05 Apr 2022 03:11:59 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 03:12:00 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 03:12:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b907f83114020e794129b34363890abf552785b8d964dbd3546272cc805702ce`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 291.3 KB (291281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988559859d9a4661992cbcefddba5b3d7a16de6c22547a962024f04767e6debf`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 5.7 KB (5748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7769260cde91250d6c68897788b078fea0a63b1254082d2923affeb859224a92`  
		Last Modified: Tue, 05 Apr 2022 03:13:22 GMT  
		Size: 10.7 MB (10738627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0143e63583cae9b0bc2b0048073b6c52476761cbeffa8e6aeca59d227ae0ee2`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; ppc64le

```console
$ docker pull caddy@sha256:0f4502864c2fae9298130a48ec4ca4351af0787bee15fd4cb5307b7b83e87dd8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13416150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b308dba8382e868224f828f88958151f9c1af01332da44ca296967f8bf09d40b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:44 GMT
ADD file:0b9367758b91930d9d69fd3901262e3a696f7a9f6d9e209e35da83ea6e785837 in / 
# Tue, 05 Apr 2022 00:23:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:07:02 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 07:07:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 07:07:12 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 07:07:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 07:07:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:07:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 07:07:31 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 07:07:33 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 07:07:36 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 07:07:40 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 07:07:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 07:07:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 07:07:47 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 07:07:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 07:07:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 07:07:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 07:07:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 07:08:03 GMT
EXPOSE 80
# Tue, 05 Apr 2022 07:08:06 GMT
EXPOSE 443
# Tue, 05 Apr 2022 07:08:08 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 07:08:10 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 07:08:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ee5f6345565e7aeda814a5c097612cacb0a74186b1f01bf5199e1b812b5d3065`  
		Last Modified: Tue, 05 Apr 2022 00:25:06 GMT  
		Size: 2.8 MB (2814167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8affbe739a71e3875810f257750034ec7a6ee3f2f2c0094f3bcb3ed8a45520b`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 293.7 KB (293710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc927cb41936aaa5bfefa5dc4d654b7193fd568f619707120a5491c620906fc1`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8646c35213c358f518a4d76b75742b5930acec5d12cbd6c75d0a7e217698cee`  
		Last Modified: Tue, 05 Apr 2022 07:11:06 GMT  
		Size: 10.3 MB (10302288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346269e52424a62ec14d10c3e1db1aeb9cefe58f0bf6021855044138396bc074`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; s390x

```console
$ docker pull caddy@sha256:4bdb0834a42c22fa543fe4497215113db9aa55197d55597fb16c6cfd2a7ec22a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14225578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0631ff02e5e01fcee0ebd5387c53f8dca8198463556fd98f569e3454b0bab`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:47 GMT
ADD file:0f70e0f0075bee67acb44e5ef01bf6b9df1f69a25b7aa6fd15bd5bb6ec5bcc9f in / 
# Mon, 04 Apr 2022 23:41:48 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:19:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:19:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 06:19:20 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 06:19:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 06:19:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:19:22 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 06:19:23 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 06:19:23 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 06:19:23 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 80
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 443
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 06:19:25 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 06:19:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6f6a6c77b1bd5dfb3e759efaa292f964f197ae4b96be74d80ef059f87317997a`  
		Last Modified: Mon, 04 Apr 2022 23:42:47 GMT  
		Size: 2.6 MB (2604075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46276fc79092fffc5c0d503ca8733315c8e4002c4e7da79b2383f14c70565746`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 291.8 KB (291788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2e4510a7572a45fad3f051c23678f720057b3bb38d17381f62903aa621c6eb`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf64cfe3d9d0d01f6a1856e4850cd31a634fbb44641472deac6358fdc04352ea`  
		Last Modified: Tue, 05 Apr 2022 06:20:34 GMT  
		Size: 11.3 MB (11323733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363873546085e9612ff25fa067fed8e0038220696a865e645e8046a79035fc99`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-alpine`

```console
$ docker pull caddy@sha256:15e576e7d00b1f41a648c5295a03677c24da5fede09131edcb1e6d809c7dc8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.4.6-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:c8555e2ca66576a4404c2b5f31d843a5378dea6134acb500502901b563efebcf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14842034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ace180df3e668bd7937be4555305fdb7686c68acf2b5514665e2bac99bd266a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:24:48 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 04:24:50 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 04:24:50 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 04:24:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 04:24:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:24:52 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 04:24:52 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 04:24:52 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 04:24:53 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 80
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 443
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 04:24:54 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 04:24:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe024ea85c2d7fb47ce4f044038d4227cee2a982bca3e26a0ea4772b8b652f9a`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 291.2 KB (291230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438e4a77a6e9c40c3bf1fb392618ac596307733f97d294edb86383ce8ff7e51d`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6d2ebbfc8548ecc1dbf4c7568459e52549b81522cb450d42ada1bf82513a8d`  
		Last Modified: Tue, 05 Apr 2022 04:25:34 GMT  
		Size: 11.7 MB (11726452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c5f60dbd2d0286f964c9769a4a3396935a60d0d71ac0e3f8eea5c4c20711fb`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:01ed10f530dfa4af76fa0f13bcdde451a934fbd3a2d77e4cfa72dbc5587ac6f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14049473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c322930340bb73e0796df576638a0214eda5499c8f9b79e4f9af61aeb4da4d2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:14:11 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:14:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 03:14:14 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 03:14:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 03:14:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 03:14:20 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 03:14:21 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 03:14:21 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 03:14:22 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 03:14:22 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 03:14:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 03:14:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 03:14:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 03:14:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 03:14:26 GMT
EXPOSE 80
# Tue, 05 Apr 2022 03:14:26 GMT
EXPOSE 443
# Tue, 05 Apr 2022 03:14:27 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 03:14:27 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 03:14:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d650105deec735ac6dce2611f274a6cf2d9f60fc811167dd6d644e281a38f5`  
		Last Modified: Tue, 05 Apr 2022 03:17:39 GMT  
		Size: 291.7 KB (291653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f3d66a6432942b556bf7a077c220319708b7fc75279695b4b05fa25166fbaf`  
		Last Modified: Tue, 05 Apr 2022 03:17:38 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5d8162ee509e3528dd82e497c4057d40064d43d532acc589b4408c08d2b144`  
		Last Modified: Tue, 05 Apr 2022 03:17:46 GMT  
		Size: 11.1 MB (11125784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0ebc13031265ef07e50f9c7658d00ce8d28c00affdf202b6dd849558f06ad6`  
		Last Modified: Tue, 05 Apr 2022 03:17:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:80bf5252e7e8c04e9ff83dd861f7ee4e81bad7b2b52b5c78a43abf0c95818cf7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dddbbfbbc47ddc2ad3b96622c35ee55ec3eecd5e37cde28c3dfe807ac0827ba`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:52 GMT
ADD file:97f7b59ed0e40e7771daab294820763a7bb86c843317be55725baf1cab39aa12 in / 
# Mon, 04 Apr 2022 23:57:52 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:32:17 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:32:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 06:32:20 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 06:32:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 06:32:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:32:26 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 06:32:26 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 06:32:27 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 06:32:27 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 06:32:28 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 06:32:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 06:32:30 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 06:32:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 06:32:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 06:32:31 GMT
EXPOSE 80
# Tue, 05 Apr 2022 06:32:32 GMT
EXPOSE 443
# Tue, 05 Apr 2022 06:32:32 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 06:32:33 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 06:32:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:380010979fdd8a9a4b0bf397034a27ec6cabe61d36e9e6d460ea986f0ddaef38`  
		Last Modified: Mon, 04 Apr 2022 23:59:45 GMT  
		Size: 2.4 MB (2427969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0decd23e3d353b46346bc943e7c39f406496ebc5b14731e4575f770563ddef21`  
		Last Modified: Tue, 05 Apr 2022 06:34:41 GMT  
		Size: 290.6 KB (290637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf30d07056a9a35092dc8a190963a5d19c14fce0543c6f6cfed98fc9a687dc5f`  
		Last Modified: Tue, 05 Apr 2022 06:34:40 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbde61fe85af3ebca0218d5ca1f9b5b6d095a57aedc0d7a827ba511e2143629`  
		Last Modified: Tue, 05 Apr 2022 06:34:48 GMT  
		Size: 11.1 MB (11106715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9e55ef38253194b94160973edf2d58fbb2df74561e28d5e7894a3865f9daf8`  
		Last Modified: Tue, 05 Apr 2022 06:34:40 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:e526f540c45973c7a3a4585918890beceac9f0916e124daea3bf4e8b7a1e09b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13753199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2982d1a58becf38a1cf55541dcd74c1b096e8a02bb2060c30540fd3246e46e4f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:11:38 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:11:40 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 03:11:41 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 03:11:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 03:11:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 03:11:45 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 03:11:46 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 03:11:47 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 03:11:48 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 03:11:49 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 03:11:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 03:11:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 03:11:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 03:11:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 03:11:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 03:11:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 03:11:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 03:11:57 GMT
EXPOSE 80
# Tue, 05 Apr 2022 03:11:58 GMT
EXPOSE 443
# Tue, 05 Apr 2022 03:11:59 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 03:12:00 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 03:12:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b907f83114020e794129b34363890abf552785b8d964dbd3546272cc805702ce`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 291.3 KB (291281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988559859d9a4661992cbcefddba5b3d7a16de6c22547a962024f04767e6debf`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 5.7 KB (5748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7769260cde91250d6c68897788b078fea0a63b1254082d2923affeb859224a92`  
		Last Modified: Tue, 05 Apr 2022 03:13:22 GMT  
		Size: 10.7 MB (10738627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0143e63583cae9b0bc2b0048073b6c52476761cbeffa8e6aeca59d227ae0ee2`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:0f4502864c2fae9298130a48ec4ca4351af0787bee15fd4cb5307b7b83e87dd8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13416150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b308dba8382e868224f828f88958151f9c1af01332da44ca296967f8bf09d40b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:44 GMT
ADD file:0b9367758b91930d9d69fd3901262e3a696f7a9f6d9e209e35da83ea6e785837 in / 
# Tue, 05 Apr 2022 00:23:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:07:02 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 07:07:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 07:07:12 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 07:07:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 07:07:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:07:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 07:07:31 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 07:07:33 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 07:07:36 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 07:07:40 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 07:07:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 07:07:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 07:07:47 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 07:07:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 07:07:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 07:07:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 07:07:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 07:08:03 GMT
EXPOSE 80
# Tue, 05 Apr 2022 07:08:06 GMT
EXPOSE 443
# Tue, 05 Apr 2022 07:08:08 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 07:08:10 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 07:08:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ee5f6345565e7aeda814a5c097612cacb0a74186b1f01bf5199e1b812b5d3065`  
		Last Modified: Tue, 05 Apr 2022 00:25:06 GMT  
		Size: 2.8 MB (2814167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8affbe739a71e3875810f257750034ec7a6ee3f2f2c0094f3bcb3ed8a45520b`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 293.7 KB (293710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc927cb41936aaa5bfefa5dc4d654b7193fd568f619707120a5491c620906fc1`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8646c35213c358f518a4d76b75742b5930acec5d12cbd6c75d0a7e217698cee`  
		Last Modified: Tue, 05 Apr 2022 07:11:06 GMT  
		Size: 10.3 MB (10302288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346269e52424a62ec14d10c3e1db1aeb9cefe58f0bf6021855044138396bc074`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:4bdb0834a42c22fa543fe4497215113db9aa55197d55597fb16c6cfd2a7ec22a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14225578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0631ff02e5e01fcee0ebd5387c53f8dca8198463556fd98f569e3454b0bab`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:47 GMT
ADD file:0f70e0f0075bee67acb44e5ef01bf6b9df1f69a25b7aa6fd15bd5bb6ec5bcc9f in / 
# Mon, 04 Apr 2022 23:41:48 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:19:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:19:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 06:19:20 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 06:19:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 06:19:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:19:22 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 06:19:23 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 06:19:23 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 06:19:23 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 80
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 443
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 06:19:25 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 06:19:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6f6a6c77b1bd5dfb3e759efaa292f964f197ae4b96be74d80ef059f87317997a`  
		Last Modified: Mon, 04 Apr 2022 23:42:47 GMT  
		Size: 2.6 MB (2604075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46276fc79092fffc5c0d503ca8733315c8e4002c4e7da79b2383f14c70565746`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 291.8 KB (291788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2e4510a7572a45fad3f051c23678f720057b3bb38d17381f62903aa621c6eb`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf64cfe3d9d0d01f6a1856e4850cd31a634fbb44641472deac6358fdc04352ea`  
		Last Modified: Tue, 05 Apr 2022 06:20:34 GMT  
		Size: 11.3 MB (11323733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363873546085e9612ff25fa067fed8e0038220696a865e645e8046a79035fc99`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-builder`

```console
$ docker pull caddy@sha256:7330e2d325fa6b9d0f64526b31373722f60520a8e29131ef0c48537273d15a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2686; amd64

### `caddy:2.4.6-builder` - linux; amd64

```console
$ docker pull caddy@sha256:80234a9cd66af5a747785958e8dc683a43dfe946b9b98c9ffe2806fa4ac5422e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121342541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa54d86d06fba28c500cfe838c151623b997c5e35b2af29ea8b70b6a92a7fb8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:32:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 05:32:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 05:32:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:37:30 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 05:39:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 05:39:29 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 05:39:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:39:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 05:39:30 GMT
WORKDIR /go
# Tue, 05 Apr 2022 15:45:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 15:45:54 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 15:45:54 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 15:45:54 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 15:45:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 15:45:55 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 15:45:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc419b0ee22d1bb5f3b95a57b2edc733b7b585277f8101db7b2c9b53605c1b`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 272.0 KB (271965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc292e5bacdd8b97a1632a82d0fd0ee6c2692409bd4b35cb9e7e652efbc7c8`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dea7a3ad9148616176ac7fd686181a6e3c4eaac3746166e678a11017e4d32d9`  
		Last Modified: Tue, 05 Apr 2022 05:43:55 GMT  
		Size: 110.2 MB (110188123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35228ee6d672a4ef2501b746851ae8dc63cdc2612057a726a7affcd9d7d9f08`  
		Last Modified: Tue, 05 Apr 2022 05:43:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431098d05c7f64b1b215f6e58d58584efa1b85c22de1e46eabdf9f41c9a31550`  
		Last Modified: Tue, 05 Apr 2022 15:46:24 GMT  
		Size: 6.8 MB (6821467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16611ed52579f2526e4c8ef7d32963cc52bdf84706c195aaea01082575369d8d`  
		Last Modified: Tue, 05 Apr 2022 15:46:23 GMT  
		Size: 1.2 MB (1245713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56bc9474ab53335737725ec3c82362fd8d085309b54710629fec01fac471c3d`  
		Last Modified: Tue, 05 Apr 2022 15:46:22 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:dcf5e840b541953183c28551fb8ad10bcb3a75ad0eb6010cf518751eb246cdb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115819309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b820bb6f118cf0da95b1daa66e903131e906c6f7937eeb823bea92880a827ed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:39:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 11:59:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 11:59:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 12:07:43 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 12:10:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 12:10:56 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 12:10:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 12:10:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 12:10:58 GMT
WORKDIR /go
# Tue, 05 Apr 2022 18:47:17 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 18:47:18 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 18:47:18 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 18:47:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 18:47:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 18:47:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 18:47:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560305eea4784da98378676b22f9871093d6a4d7eb88292accc17f0cfd6b12ea`  
		Last Modified: Tue, 05 Apr 2022 11:40:22 GMT  
		Size: 272.1 KB (272138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145a805e932abbcca6b77ad458c7ac26275ff4f23af9912d2c4d3dac9eef4cf8`  
		Last Modified: Tue, 05 Apr 2022 12:15:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc18cdc5d172f77e8e9ab98b63b490a7ee5597737555f86ab3df9580d7603038`  
		Last Modified: Tue, 05 Apr 2022 12:20:29 GMT  
		Size: 105.1 MB (105068577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a00aaf29b7cc08e00fa3ad26938794099e739101e45a4efbd80da84b4b59e8`  
		Last Modified: Tue, 05 Apr 2022 12:19:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce9447fafc122cfcae03e938e9b3bf3750eda3436a83625bc1229d67e6f3526`  
		Last Modified: Tue, 05 Apr 2022 18:49:07 GMT  
		Size: 6.7 MB (6677398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb4981b5917a068228e1b12e5afe118826c4ebb0880a39e0de01773e1a9b6b`  
		Last Modified: Tue, 05 Apr 2022 18:49:04 GMT  
		Size: 1.2 MB (1178510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50ceda04f269611e045f72b6f59cd9458e489675973c2a26d9ba4c92417c110`  
		Last Modified: Tue, 05 Apr 2022 18:49:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:f067c336bf9a0f6755735e5dbd07fdbce24f00d4ded39ae414599dd0707f5909
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114678400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e18d0d8561f2864f5ae2184d369b7ed78f855c8098e12b18e3e66e9ed1d702`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:19:56 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:19:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:19:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:28:26 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 09:31:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 09:31:38 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 09:31:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:31:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 09:31:40 GMT
WORKDIR /go
# Wed, 06 Apr 2022 02:23:29 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 06 Apr 2022 02:23:29 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 06 Apr 2022 02:23:30 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 06 Apr 2022 02:23:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Apr 2022 02:23:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 06 Apr 2022 02:23:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 06 Apr 2022 02:23:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f68dacdb1dfe1ed299ab3e43e478a27f0977380bbefc4c7ca5723758dbac6`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 271.1 KB (271116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431ad618c287090e481554b57afdc0383f065b5bbfc0ccdcefc6518e1a8331e`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1c19e6ea71a7140e1f92aaf1ca20998b7875298f5f0aecdad1849acea539e9`  
		Last Modified: Tue, 05 Apr 2022 09:43:01 GMT  
		Size: 104.9 MB (104853355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d18ca61f70738e42fc01d4076606b8ef68be3c58058c1922e2b44987e87a15`  
		Last Modified: Tue, 05 Apr 2022 09:41:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d951a4c4c0e205bd2d3656382822e0ad97c4ee98c7cc185614d9363d5b7b18df`  
		Last Modified: Wed, 06 Apr 2022 02:25:20 GMT  
		Size: 6.0 MB (5952176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b38ba848bdb94dd4baa0c3e1ed84c6c0f039346dbd2904d5e257b874558a07`  
		Last Modified: Wed, 06 Apr 2022 02:25:18 GMT  
		Size: 1.2 MB (1176713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426c201900d8690c727d61a628a8540811cafc07c1ed656aeb066b7745707c7b`  
		Last Modified: Wed, 06 Apr 2022 02:25:18 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:7b6beab6198241afad1f6660a5083478efd4f1e92ff2edccc566bca27905c310
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115488051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ee73e0e2ed794915b2af927e5458f4bad17835e41f615dab40db89f343bdf0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:38:07 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 07:38:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:38:08 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:41:43 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 07:43:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 07:43:02 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 07:43:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 07:43:05 GMT
WORKDIR /go
# Tue, 05 Apr 2022 17:39:06 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 17:39:07 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 17:39:08 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 17:39:09 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 17:39:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 17:39:13 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 17:39:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7637d0a7b497b253b73e807a5e676ba3f0750afafa9e1a4c61260513feb321f`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 271.8 KB (271764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda57b85efde0ed435315f4f74625e7a055107aa29e8c91a313ca6d525fb709c`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d20097de21a08b3879d9d8acda7ea55af524f6cb8cf3d8526c7ad583992e7f`  
		Last Modified: Tue, 05 Apr 2022 07:47:32 GMT  
		Size: 104.4 MB (104424495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662c5a329cf0f527093cef90725754463b5ab87a23be5a91edff92a844e76c37`  
		Last Modified: Tue, 05 Apr 2022 07:47:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f1e21bd0bbbfa99416af4431f653df5121e14b29364c870d86362268419104`  
		Last Modified: Tue, 05 Apr 2022 17:40:06 GMT  
		Size: 6.9 MB (6925952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e5c2ce8d4fcaae75fbb7497ef4b24c4b192aafbb3384f7a8221b0c1213401`  
		Last Modified: Tue, 05 Apr 2022 17:40:05 GMT  
		Size: 1.1 MB (1148677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4162b5640fb2e218682c6e2bfb93a2f2ad6c9ffbe57ecec50ca91554eefefa`  
		Last Modified: Tue, 05 Apr 2022 17:40:05 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:f0523e893e89caa4a62fb934156846b72fa1e93191eb22fe3e2648b4416da80e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114312516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066aed791277682729d033b831d7ce9039dba3849abd6e0cf881b8992fd75b70`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:50:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:50:19 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:50:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:57:52 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 10:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 10:00:43 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 10:00:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 10:00:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 10:00:55 GMT
WORKDIR /go
# Wed, 06 Apr 2022 02:52:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 06 Apr 2022 02:53:02 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 06 Apr 2022 02:53:05 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 06 Apr 2022 02:53:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Apr 2022 02:53:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 06 Apr 2022 02:53:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 06 Apr 2022 02:53:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcdc2e904e95f788aa4c66c5ce746890d6a02abca4c94711443f5c688b61ebf`  
		Last Modified: Tue, 05 Apr 2022 10:06:11 GMT  
		Size: 274.2 KB (274171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04802687d9aa11413122df45eb15c7d7f85937270997b441d1c6a09001730453`  
		Last Modified: Tue, 05 Apr 2022 10:06:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce62b250e0aee7f0aec0715e9113355ac5a4781c1eaf0d4bea6fcdf4073068f8`  
		Last Modified: Tue, 05 Apr 2022 10:08:01 GMT  
		Size: 102.8 MB (102784652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c7dcfaac085766cdaa5fce90fb5c664130f22fa3f6005b3cebddf45a4e2b9b`  
		Last Modified: Tue, 05 Apr 2022 10:07:43 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7a86ae8bfd11a7525de064d7143eed347098156c965551db06b0da1fab2f67`  
		Last Modified: Wed, 06 Apr 2022 02:54:45 GMT  
		Size: 7.3 MB (7320952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33cc607466c85109d67b2a8aefc6a137b9aebe631f8e33435b2618033bb3737`  
		Last Modified: Wed, 06 Apr 2022 02:54:45 GMT  
		Size: 1.1 MB (1120840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3107bf51b5f81e988fc6b01377bdab7efc085a95bfa0b866d40cd7c18bb23a6d`  
		Last Modified: Wed, 06 Apr 2022 02:54:44 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; s390x

```console
$ docker pull caddy@sha256:7862e378800416206aa5844ed260f8cb64c1537299e481e5004521024727c011
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118747451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d95993f92df472d91942633064b5db1e229654fbf9e15e574f235f732d2171`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:08:51 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 06:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:44:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:48:26 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 06:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 06:49:56 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 06:49:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:49:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 06:49:57 GMT
WORKDIR /go
# Tue, 05 Apr 2022 14:02:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 14:02:02 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 14:02:02 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 14:02:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 14:02:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 14:02:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 14:02:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72593bb761a2ce336603e9e84973d1e284f39e0188e758ad8bc22c45cd9b6395`  
		Last Modified: Tue, 05 Apr 2022 06:09:13 GMT  
		Size: 272.3 KB (272267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf480933488ffcb2c9c9269292e2e3d643bea6eeb04cf948790ca50666a61c8`  
		Last Modified: Tue, 05 Apr 2022 06:53:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b3e51e0eff0c3e6118a6448425ada0b8e1725d738559d5b5e29ef58c570e8d`  
		Last Modified: Tue, 05 Apr 2022 06:54:30 GMT  
		Size: 107.7 MB (107739421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86765c73189fadce4ca276af5f7d9440213d5986a9687b648a51d45978e3a8c4`  
		Last Modified: Tue, 05 Apr 2022 06:54:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f50aeaf488b81d4c5d54c453b47637b6fbdfae9ca014728018463ce30aa78b`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 6.9 MB (6930892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca74c757745c5b39f811e1b5ed2a0fe0b8f2de2ab52b23dd01d8aaa71540d27b`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 1.2 MB (1203782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e4f898506aece97cc68bfd9e1a347bd072242e4672eee262eae303b3e0b6e9`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:568847e6f37af8e2f55d5d780b100e1dbfcbb9178896eb9d8f2b57ecf966d39c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888394051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20261b1174a82d98f801248da692dc2862f133c7cea9e52758b2c17b3567abc3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 13:17:25 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Mar 2022 13:17:26 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Mar 2022 13:17:27 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Mar 2022 13:17:28 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Mar 2022 13:19:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:19:56 GMT
ENV GOPATH=C:\go
# Wed, 09 Mar 2022 13:20:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Mar 2022 13:35:10 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 09 Mar 2022 13:38:26 GMT
RUN $url = 'https://dl.google.com/go/go1.17.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '85ccf2608dca6ea9a46b6538c9e75e7cf2aebdf502379843b248e26b8bb110be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:38:28 GMT
WORKDIR C:\go
# Wed, 09 Mar 2022 18:27:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Mar 2022 23:14:28 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 23:14:29 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 23:14:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 23:15:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('fc6f2a7feb8f0936a0e04d3c9ea26d0404c2f4907eb436eb60e33152c22c1211f851c46606573fcb5c3334f8cc4f7f810b28b917a9f313f6454d1c5cd0f50f8a')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 10 Mar 2022 23:15:41 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7705bbffd7dc00934e935de0e00e09a7b0da55d66c596622f094495478dd71`  
		Last Modified: Wed, 09 Mar 2022 14:04:13 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be7ff0bb187d149a5cf3c76e1ec444d0e07c6606f67b2c921c67ec91829ea03`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876223f25b257577440a80fdee021b43c33ce3c56be9a20b2ddeaede95240522`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991eea244b9c3a1849c84748425dd9e9fbf9ec359ad9329796131b929239ffa4`  
		Last Modified: Wed, 09 Mar 2022 14:04:11 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b4c7c9740eb99bf626b312aa69396db3d186c5bd0e092b01c078ca7248e386`  
		Last Modified: Wed, 09 Mar 2022 14:04:40 GMT  
		Size: 25.5 MB (25454695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6c8a4d4848c21636a48a69a569a5372ec4890ea029f1f620dda76078bdcef`  
		Last Modified: Wed, 09 Mar 2022 14:04:09 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac6d527939082add6d21652ba4888acc5a6e7607365168d8e61fb1485339cb`  
		Last Modified: Wed, 09 Mar 2022 14:04:10 GMT  
		Size: 313.6 KB (313592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37aeceb8c2e5bb3c500129bcf20c3f8aea8c68c353e6714a63a225ed1546e8a1`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d88cd595dc7580d72420b7288c52d4b32201045a13dda1a7b943d9a3468adef`  
		Last Modified: Wed, 09 Mar 2022 14:13:05 GMT  
		Size: 145.5 MB (145488847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be492983ee2b2c9128ce0c732c441ae5fbd203cdb71c94faa253c24b01750c90`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa7b09ca61eb1fbafacee427b430b0879ad4da23e62e430a3fe6a66f181f642`  
		Last Modified: Wed, 09 Mar 2022 18:30:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74014ffde8e1a1677cd81e965bcd2b1f5287bcbf682bbce3bdd125052cd04f29`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43e7b3a6c47e8c9bba8e4ba91d722cd9e491f2df12d5e277356e2b8fc070ba8`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceffc29f93380b6942a245303d5af87875d60351e4c897405f358f018b61b863`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae9e05c08471d9a54c2b46c4f892226ab1eab63b6efd326c44b50bceffb11f2`  
		Last Modified: Thu, 10 Mar 2022 23:22:56 GMT  
		Size: 1.7 MB (1665933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd386d40eef8a252639d03e1486ff30ff8f77cef626bf0592cc7853eb633c7d`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-builder-alpine`

```console
$ docker pull caddy@sha256:54e2deab0aa5245b222cba916d21cb85acb53793dbb1651e3c7a6e7eb6240089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.4.6-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:80234a9cd66af5a747785958e8dc683a43dfe946b9b98c9ffe2806fa4ac5422e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121342541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa54d86d06fba28c500cfe838c151623b997c5e35b2af29ea8b70b6a92a7fb8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:32:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 05:32:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 05:32:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:37:30 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 05:39:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 05:39:29 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 05:39:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:39:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 05:39:30 GMT
WORKDIR /go
# Tue, 05 Apr 2022 15:45:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 15:45:54 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 15:45:54 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 15:45:54 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 15:45:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 15:45:55 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 15:45:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc419b0ee22d1bb5f3b95a57b2edc733b7b585277f8101db7b2c9b53605c1b`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 272.0 KB (271965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc292e5bacdd8b97a1632a82d0fd0ee6c2692409bd4b35cb9e7e652efbc7c8`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dea7a3ad9148616176ac7fd686181a6e3c4eaac3746166e678a11017e4d32d9`  
		Last Modified: Tue, 05 Apr 2022 05:43:55 GMT  
		Size: 110.2 MB (110188123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35228ee6d672a4ef2501b746851ae8dc63cdc2612057a726a7affcd9d7d9f08`  
		Last Modified: Tue, 05 Apr 2022 05:43:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431098d05c7f64b1b215f6e58d58584efa1b85c22de1e46eabdf9f41c9a31550`  
		Last Modified: Tue, 05 Apr 2022 15:46:24 GMT  
		Size: 6.8 MB (6821467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16611ed52579f2526e4c8ef7d32963cc52bdf84706c195aaea01082575369d8d`  
		Last Modified: Tue, 05 Apr 2022 15:46:23 GMT  
		Size: 1.2 MB (1245713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56bc9474ab53335737725ec3c82362fd8d085309b54710629fec01fac471c3d`  
		Last Modified: Tue, 05 Apr 2022 15:46:22 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:dcf5e840b541953183c28551fb8ad10bcb3a75ad0eb6010cf518751eb246cdb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115819309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b820bb6f118cf0da95b1daa66e903131e906c6f7937eeb823bea92880a827ed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:39:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 11:59:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 11:59:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 12:07:43 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 12:10:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 12:10:56 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 12:10:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 12:10:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 12:10:58 GMT
WORKDIR /go
# Tue, 05 Apr 2022 18:47:17 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 18:47:18 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 18:47:18 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 18:47:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 18:47:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 18:47:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 18:47:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560305eea4784da98378676b22f9871093d6a4d7eb88292accc17f0cfd6b12ea`  
		Last Modified: Tue, 05 Apr 2022 11:40:22 GMT  
		Size: 272.1 KB (272138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145a805e932abbcca6b77ad458c7ac26275ff4f23af9912d2c4d3dac9eef4cf8`  
		Last Modified: Tue, 05 Apr 2022 12:15:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc18cdc5d172f77e8e9ab98b63b490a7ee5597737555f86ab3df9580d7603038`  
		Last Modified: Tue, 05 Apr 2022 12:20:29 GMT  
		Size: 105.1 MB (105068577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a00aaf29b7cc08e00fa3ad26938794099e739101e45a4efbd80da84b4b59e8`  
		Last Modified: Tue, 05 Apr 2022 12:19:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce9447fafc122cfcae03e938e9b3bf3750eda3436a83625bc1229d67e6f3526`  
		Last Modified: Tue, 05 Apr 2022 18:49:07 GMT  
		Size: 6.7 MB (6677398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb4981b5917a068228e1b12e5afe118826c4ebb0880a39e0de01773e1a9b6b`  
		Last Modified: Tue, 05 Apr 2022 18:49:04 GMT  
		Size: 1.2 MB (1178510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50ceda04f269611e045f72b6f59cd9458e489675973c2a26d9ba4c92417c110`  
		Last Modified: Tue, 05 Apr 2022 18:49:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:f067c336bf9a0f6755735e5dbd07fdbce24f00d4ded39ae414599dd0707f5909
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114678400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e18d0d8561f2864f5ae2184d369b7ed78f855c8098e12b18e3e66e9ed1d702`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:19:56 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:19:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:19:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:28:26 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 09:31:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 09:31:38 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 09:31:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:31:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 09:31:40 GMT
WORKDIR /go
# Wed, 06 Apr 2022 02:23:29 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 06 Apr 2022 02:23:29 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 06 Apr 2022 02:23:30 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 06 Apr 2022 02:23:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Apr 2022 02:23:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 06 Apr 2022 02:23:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 06 Apr 2022 02:23:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f68dacdb1dfe1ed299ab3e43e478a27f0977380bbefc4c7ca5723758dbac6`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 271.1 KB (271116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431ad618c287090e481554b57afdc0383f065b5bbfc0ccdcefc6518e1a8331e`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1c19e6ea71a7140e1f92aaf1ca20998b7875298f5f0aecdad1849acea539e9`  
		Last Modified: Tue, 05 Apr 2022 09:43:01 GMT  
		Size: 104.9 MB (104853355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d18ca61f70738e42fc01d4076606b8ef68be3c58058c1922e2b44987e87a15`  
		Last Modified: Tue, 05 Apr 2022 09:41:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d951a4c4c0e205bd2d3656382822e0ad97c4ee98c7cc185614d9363d5b7b18df`  
		Last Modified: Wed, 06 Apr 2022 02:25:20 GMT  
		Size: 6.0 MB (5952176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b38ba848bdb94dd4baa0c3e1ed84c6c0f039346dbd2904d5e257b874558a07`  
		Last Modified: Wed, 06 Apr 2022 02:25:18 GMT  
		Size: 1.2 MB (1176713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426c201900d8690c727d61a628a8540811cafc07c1ed656aeb066b7745707c7b`  
		Last Modified: Wed, 06 Apr 2022 02:25:18 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:7b6beab6198241afad1f6660a5083478efd4f1e92ff2edccc566bca27905c310
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115488051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ee73e0e2ed794915b2af927e5458f4bad17835e41f615dab40db89f343bdf0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:38:07 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 07:38:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:38:08 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:41:43 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 07:43:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 07:43:02 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 07:43:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 07:43:05 GMT
WORKDIR /go
# Tue, 05 Apr 2022 17:39:06 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 17:39:07 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 17:39:08 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 17:39:09 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 17:39:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 17:39:13 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 17:39:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7637d0a7b497b253b73e807a5e676ba3f0750afafa9e1a4c61260513feb321f`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 271.8 KB (271764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda57b85efde0ed435315f4f74625e7a055107aa29e8c91a313ca6d525fb709c`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d20097de21a08b3879d9d8acda7ea55af524f6cb8cf3d8526c7ad583992e7f`  
		Last Modified: Tue, 05 Apr 2022 07:47:32 GMT  
		Size: 104.4 MB (104424495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662c5a329cf0f527093cef90725754463b5ab87a23be5a91edff92a844e76c37`  
		Last Modified: Tue, 05 Apr 2022 07:47:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f1e21bd0bbbfa99416af4431f653df5121e14b29364c870d86362268419104`  
		Last Modified: Tue, 05 Apr 2022 17:40:06 GMT  
		Size: 6.9 MB (6925952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e5c2ce8d4fcaae75fbb7497ef4b24c4b192aafbb3384f7a8221b0c1213401`  
		Last Modified: Tue, 05 Apr 2022 17:40:05 GMT  
		Size: 1.1 MB (1148677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4162b5640fb2e218682c6e2bfb93a2f2ad6c9ffbe57ecec50ca91554eefefa`  
		Last Modified: Tue, 05 Apr 2022 17:40:05 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:f0523e893e89caa4a62fb934156846b72fa1e93191eb22fe3e2648b4416da80e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114312516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066aed791277682729d033b831d7ce9039dba3849abd6e0cf881b8992fd75b70`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:50:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:50:19 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:50:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:57:52 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 10:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 10:00:43 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 10:00:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 10:00:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 10:00:55 GMT
WORKDIR /go
# Wed, 06 Apr 2022 02:52:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 06 Apr 2022 02:53:02 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 06 Apr 2022 02:53:05 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 06 Apr 2022 02:53:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Apr 2022 02:53:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 06 Apr 2022 02:53:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 06 Apr 2022 02:53:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcdc2e904e95f788aa4c66c5ce746890d6a02abca4c94711443f5c688b61ebf`  
		Last Modified: Tue, 05 Apr 2022 10:06:11 GMT  
		Size: 274.2 KB (274171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04802687d9aa11413122df45eb15c7d7f85937270997b441d1c6a09001730453`  
		Last Modified: Tue, 05 Apr 2022 10:06:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce62b250e0aee7f0aec0715e9113355ac5a4781c1eaf0d4bea6fcdf4073068f8`  
		Last Modified: Tue, 05 Apr 2022 10:08:01 GMT  
		Size: 102.8 MB (102784652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c7dcfaac085766cdaa5fce90fb5c664130f22fa3f6005b3cebddf45a4e2b9b`  
		Last Modified: Tue, 05 Apr 2022 10:07:43 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7a86ae8bfd11a7525de064d7143eed347098156c965551db06b0da1fab2f67`  
		Last Modified: Wed, 06 Apr 2022 02:54:45 GMT  
		Size: 7.3 MB (7320952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33cc607466c85109d67b2a8aefc6a137b9aebe631f8e33435b2618033bb3737`  
		Last Modified: Wed, 06 Apr 2022 02:54:45 GMT  
		Size: 1.1 MB (1120840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3107bf51b5f81e988fc6b01377bdab7efc085a95bfa0b866d40cd7c18bb23a6d`  
		Last Modified: Wed, 06 Apr 2022 02:54:44 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:7862e378800416206aa5844ed260f8cb64c1537299e481e5004521024727c011
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118747451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d95993f92df472d91942633064b5db1e229654fbf9e15e574f235f732d2171`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:08:51 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 06:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:44:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:48:26 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 06:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 06:49:56 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 06:49:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:49:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 06:49:57 GMT
WORKDIR /go
# Tue, 05 Apr 2022 14:02:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 14:02:02 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 14:02:02 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 14:02:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 14:02:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 14:02:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 14:02:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72593bb761a2ce336603e9e84973d1e284f39e0188e758ad8bc22c45cd9b6395`  
		Last Modified: Tue, 05 Apr 2022 06:09:13 GMT  
		Size: 272.3 KB (272267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf480933488ffcb2c9c9269292e2e3d643bea6eeb04cf948790ca50666a61c8`  
		Last Modified: Tue, 05 Apr 2022 06:53:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b3e51e0eff0c3e6118a6448425ada0b8e1725d738559d5b5e29ef58c570e8d`  
		Last Modified: Tue, 05 Apr 2022 06:54:30 GMT  
		Size: 107.7 MB (107739421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86765c73189fadce4ca276af5f7d9440213d5986a9687b648a51d45978e3a8c4`  
		Last Modified: Tue, 05 Apr 2022 06:54:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f50aeaf488b81d4c5d54c453b47637b6fbdfae9ca014728018463ce30aa78b`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 6.9 MB (6930892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca74c757745c5b39f811e1b5ed2a0fe0b8f2de2ab52b23dd01d8aaa71540d27b`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 1.2 MB (1203782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e4f898506aece97cc68bfd9e1a347bd072242e4672eee262eae303b3e0b6e9`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:276530503290de9ae8be7471e975d5db1e0d286e99d48317b675cec03c7c2fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `caddy:2.4.6-builder-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:568847e6f37af8e2f55d5d780b100e1dbfcbb9178896eb9d8f2b57ecf966d39c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888394051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20261b1174a82d98f801248da692dc2862f133c7cea9e52758b2c17b3567abc3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 13:17:25 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Mar 2022 13:17:26 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Mar 2022 13:17:27 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Mar 2022 13:17:28 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Mar 2022 13:19:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:19:56 GMT
ENV GOPATH=C:\go
# Wed, 09 Mar 2022 13:20:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Mar 2022 13:35:10 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 09 Mar 2022 13:38:26 GMT
RUN $url = 'https://dl.google.com/go/go1.17.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '85ccf2608dca6ea9a46b6538c9e75e7cf2aebdf502379843b248e26b8bb110be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:38:28 GMT
WORKDIR C:\go
# Wed, 09 Mar 2022 18:27:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Mar 2022 23:14:28 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 23:14:29 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 23:14:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 23:15:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('fc6f2a7feb8f0936a0e04d3c9ea26d0404c2f4907eb436eb60e33152c22c1211f851c46606573fcb5c3334f8cc4f7f810b28b917a9f313f6454d1c5cd0f50f8a')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 10 Mar 2022 23:15:41 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7705bbffd7dc00934e935de0e00e09a7b0da55d66c596622f094495478dd71`  
		Last Modified: Wed, 09 Mar 2022 14:04:13 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be7ff0bb187d149a5cf3c76e1ec444d0e07c6606f67b2c921c67ec91829ea03`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876223f25b257577440a80fdee021b43c33ce3c56be9a20b2ddeaede95240522`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991eea244b9c3a1849c84748425dd9e9fbf9ec359ad9329796131b929239ffa4`  
		Last Modified: Wed, 09 Mar 2022 14:04:11 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b4c7c9740eb99bf626b312aa69396db3d186c5bd0e092b01c078ca7248e386`  
		Last Modified: Wed, 09 Mar 2022 14:04:40 GMT  
		Size: 25.5 MB (25454695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6c8a4d4848c21636a48a69a569a5372ec4890ea029f1f620dda76078bdcef`  
		Last Modified: Wed, 09 Mar 2022 14:04:09 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac6d527939082add6d21652ba4888acc5a6e7607365168d8e61fb1485339cb`  
		Last Modified: Wed, 09 Mar 2022 14:04:10 GMT  
		Size: 313.6 KB (313592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37aeceb8c2e5bb3c500129bcf20c3f8aea8c68c353e6714a63a225ed1546e8a1`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d88cd595dc7580d72420b7288c52d4b32201045a13dda1a7b943d9a3468adef`  
		Last Modified: Wed, 09 Mar 2022 14:13:05 GMT  
		Size: 145.5 MB (145488847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be492983ee2b2c9128ce0c732c441ae5fbd203cdb71c94faa253c24b01750c90`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa7b09ca61eb1fbafacee427b430b0879ad4da23e62e430a3fe6a66f181f642`  
		Last Modified: Wed, 09 Mar 2022 18:30:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74014ffde8e1a1677cd81e965bcd2b1f5287bcbf682bbce3bdd125052cd04f29`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43e7b3a6c47e8c9bba8e4ba91d722cd9e491f2df12d5e277356e2b8fc070ba8`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceffc29f93380b6942a245303d5af87875d60351e4c897405f358f018b61b863`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae9e05c08471d9a54c2b46c4f892226ab1eab63b6efd326c44b50bceffb11f2`  
		Last Modified: Thu, 10 Mar 2022 23:22:56 GMT  
		Size: 1.7 MB (1665933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd386d40eef8a252639d03e1486ff30ff8f77cef626bf0592cc7853eb633c7d`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-windowsservercore`

```console
$ docker pull caddy@sha256:a3ba1d80239cc342421e0b3a6a6adba859191852e94c30047402f2ac1cc24407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `caddy:2.4.6-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-windowsservercore-1809`

```console
$ docker pull caddy@sha256:a3ba1d80239cc342421e0b3a6a6adba859191852e94c30047402f2ac1cc24407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `caddy:2.4.6-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-beta.1`

```console
$ docker pull caddy@sha256:67a53eebc3a0089cfeb2f1fb457d339dd41a20de5347bea4dd09e5082718c95c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2686; amd64
	-	windows version 10.0.20348.587; amd64

### `caddy:2.5.0-beta.1` - linux; amd64

```console
$ docker pull caddy@sha256:bac7580bfb78e7d7aedf9044ff33ba0a461e236bbe724253240722a2c2833b37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15281277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4004608d8af3d2fb6ce0c5961777a4106636aa68d2ed9809df92c5b85acff4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:25:00 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 04:25:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 04:25:01 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 04:25:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 04:25:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:25:07 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 04:25:07 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 04:25:07 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 04:25:07 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 04:25:07 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Tue, 05 Apr 2022 04:25:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 04:25:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 04:25:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 04:25:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 04:25:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 04:25:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 04:25:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 04:25:08 GMT
EXPOSE 80
# Tue, 05 Apr 2022 04:25:08 GMT
EXPOSE 443
# Tue, 05 Apr 2022 04:25:08 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 04:25:08 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 04:25:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87ed6b8c4412bcd2bb1f40611012b40444b12071baf4884d0e75044fc1f32c1`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 291.5 KB (291522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840ff7bd6e2c9d7717705a52c1d27654581f987e1a43d2c9f3220ce850a5cdad`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05594f38e13e9c731a8ab55b382f8af8c26f09320e016462a84c4f7ea29b09a`  
		Last Modified: Tue, 05 Apr 2022 04:25:50 GMT  
		Size: 12.2 MB (12169217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3c7da94e5fbe8d331bb4363cff609ee7a5af046d180358dfdb9745ba19a2c1`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1` - linux; arm variant v6

```console
$ docker pull caddy@sha256:995e1ee69c4e941859c8fe08ee8c7ae5d7e449f4e5243d0618391c04353271f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14451284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f8e1c5a4506d1ba5fe3ba7e360fe1bdd8a8668ceb8306da0e02fae7ba993e2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:15:01 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:15:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 03:15:04 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 03:15:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 03:15:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 03:15:10 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 03:15:10 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 03:15:11 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 03:15:11 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 03:15:12 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Tue, 05 Apr 2022 03:15:12 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 03:15:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 03:15:13 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 03:15:13 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 03:15:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 03:15:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 03:15:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 03:15:15 GMT
EXPOSE 80
# Tue, 05 Apr 2022 03:15:16 GMT
EXPOSE 443
# Tue, 05 Apr 2022 03:15:16 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 03:15:17 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 03:15:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b230dd773e10769a2eb3e507260d2470a646efd48a639739ba8852b2915302`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 291.7 KB (291685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac48280871fa0cc6e20550e9909af62acb5b3793a4ada967e49e60367ec386e`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150950fa1b63c40e7ca5764cdeb7988d8a15f550762999723e6e9659c38282c5`  
		Last Modified: Tue, 05 Apr 2022 03:18:18 GMT  
		Size: 11.5 MB (11531644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b85c24743ba55b919e1a0b33c9589948cbef4830c588108e9698ce11235633`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1` - linux; arm variant v7

```console
$ docker pull caddy@sha256:64dcd6e2cc4aad2c2c89bb7cded9819935056ee5c8aaa4f9ef182bc356435ff1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14232949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946580d1e058d0c7451feaf278c204e5bc0da968acf3f2807928c02b8fbcdbd9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:33:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:33:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 06:33:08 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 06:33:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 06:33:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:33:14 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 06:33:14 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 06:33:15 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 06:33:15 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 06:33:15 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Tue, 05 Apr 2022 06:33:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 06:33:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 06:33:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 06:33:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 06:33:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 06:33:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 06:33:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 06:33:19 GMT
EXPOSE 80
# Tue, 05 Apr 2022 06:33:19 GMT
EXPOSE 443
# Tue, 05 Apr 2022 06:33:20 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 06:33:20 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 06:33:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03203881a2568530a735b6e0e7a40ebb79adedc5193a675807b04eeb92cc6ed1`  
		Last Modified: Tue, 05 Apr 2022 06:35:07 GMT  
		Size: 290.7 KB (290668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2de87d2e387fcc410ddd706bbe177b2a04b5137087a6ffca70b45c80dc976e0`  
		Last Modified: Tue, 05 Apr 2022 06:35:08 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfc5deee1bf6f6600fe8402d08138fbf5fb1e9132ae3e820cb274ff78de74c0`  
		Last Modified: Tue, 05 Apr 2022 06:35:15 GMT  
		Size: 11.5 MB (11511975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c950586adcccfcf1ec15e40da0fb338ab975c2f6d63a3f49fbd43ab5a6b9b6`  
		Last Modified: Tue, 05 Apr 2022 06:35:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:99a7c0298ba26e39221504632853f0c12b3cc6d51ebf1d957a8614c2ac62298f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14151675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181d197c22004b9c4242984dee400be86b249372bad74740eb818cc9febf0be6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:12:15 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:12:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 03:12:17 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 03:12:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 03:12:21 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 03:12:22 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 03:12:23 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 03:12:24 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 03:12:25 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 03:12:26 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Tue, 05 Apr 2022 03:12:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 03:12:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 03:12:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 03:12:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 03:12:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 03:12:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 03:12:33 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 03:12:34 GMT
EXPOSE 80
# Tue, 05 Apr 2022 03:12:35 GMT
EXPOSE 443
# Tue, 05 Apr 2022 03:12:36 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 03:12:37 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 03:12:38 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aa37f2341b1e6d98420668c9bc849a47f2c471d159b2303885040bd8d0a92f`  
		Last Modified: Tue, 05 Apr 2022 03:13:38 GMT  
		Size: 291.3 KB (291301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e87f72d84fd403dc0ea7d95672e5865925fca64a932f046b39035e8d3b43aae`  
		Last Modified: Tue, 05 Apr 2022 03:13:37 GMT  
		Size: 5.7 KB (5747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e0ff4c04fc65e4d2e778c739fe0dff0ca9b8006b0ea5e71af2210c38c1ef87`  
		Last Modified: Tue, 05 Apr 2022 03:13:41 GMT  
		Size: 11.1 MB (11137996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cf9a10ab3f4c966798e5ce44cc9569cc31658785767c0d438f7a435666f055`  
		Last Modified: Tue, 05 Apr 2022 03:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1` - linux; ppc64le

```console
$ docker pull caddy@sha256:98a632b2c106991170be442d14b4ed3db078616bd2c5787604c1688ea46b5af0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13786562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3e24a28142e386eb1c4b37b83e291e4256a3f481e3a354f3b4bd160d8156c5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:08:34 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 07:08:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 07:08:45 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 07:08:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 07:09:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:09:06 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 07:09:08 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 07:09:11 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 07:09:13 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 07:09:17 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Tue, 05 Apr 2022 07:09:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 07:09:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 07:09:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 07:09:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 07:09:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 07:09:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 07:09:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 07:09:55 GMT
EXPOSE 80
# Tue, 05 Apr 2022 07:09:58 GMT
EXPOSE 443
# Tue, 05 Apr 2022 07:10:00 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 07:10:04 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 07:10:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743509d6ced044a369685ebb068417e8757981a39d1b397c7b0182ab89f83528`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 293.7 KB (293721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029325992e21f613a5b486751627c7d5e5c7622ec29d4d170549f4dac13ad291`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79976b8a08e399f4d6fd3eb19500adbb418be5088bda898ef58f47c6791c2aa`  
		Last Modified: Tue, 05 Apr 2022 07:11:26 GMT  
		Size: 10.7 MB (10675672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6866f1a9b35b79bf3c4b8bf13c2c2d5b1ffd33351937a641fc88f72ed011a0a7`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1` - linux; s390x

```console
$ docker pull caddy@sha256:5dc3ae5b9a9ec370660f1a192517138ca1f1822436e05f51f2cfd7d8969c901a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14627648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e041975d62fa3de352fb55c2d7349d1f7a023f98d76da64f25a9ef635bf442a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:19:41 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:19:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 06:19:42 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 06:19:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 06:19:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:19:45 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 06:19:45 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 06:19:45 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 06:19:45 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 06:19:45 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Tue, 05 Apr 2022 06:19:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 06:19:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 06:19:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 06:19:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 06:19:46 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 06:19:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 06:19:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 06:19:46 GMT
EXPOSE 80
# Tue, 05 Apr 2022 06:19:46 GMT
EXPOSE 443
# Tue, 05 Apr 2022 06:19:47 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 06:19:47 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 06:19:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8cc7c7c7ffd67f5740add448d341753330a2abdc6ed06e995cb7d28de381ab`  
		Last Modified: Tue, 05 Apr 2022 06:20:44 GMT  
		Size: 291.8 KB (291821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36f8e9524a50422cbb86b1c5e3af26710e4b65591ecc118a5079f1aa7fe5a67`  
		Last Modified: Tue, 05 Apr 2022 06:20:45 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d9efb35d6033b2097e2b43f03270f6509c549e025a79566426a0c5e9450cf6`  
		Last Modified: Tue, 05 Apr 2022 06:20:46 GMT  
		Size: 11.7 MB (11729468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f7e89e0dae073ed741dd140b8085f3e69a24baa02f5c4e762e24aece4e7d5e`  
		Last Modified: Tue, 05 Apr 2022 06:20:44 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:7773fd461ee6f12339ba1673bc5df75781a929c178c69f2b76f6dbb331c4b8a9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728732764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1eacf7022523cf02e6baa380b984f1849385cfe6d35462401e39349c8fae5c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 10 Mar 2022 23:15:55 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 23:17:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d3823cb9ec107805c996e0de561c460a8d865698362c6ba842a69503af693d8f7db8ac418abffc4b7110a273d0b8be50168f8a5bcc0dc4da1e81fd1a4271f9d2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 10 Mar 2022 23:17:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 10 Mar 2022 23:17:02 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 10 Mar 2022 23:17:03 GMT
VOLUME [c:/config]
# Thu, 10 Mar 2022 23:17:05 GMT
VOLUME [c:/data]
# Thu, 10 Mar 2022 23:17:06 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Thu, 10 Mar 2022 23:17:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 10 Mar 2022 23:17:11 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 10 Mar 2022 23:17:13 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 10 Mar 2022 23:17:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 10 Mar 2022 23:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 10 Mar 2022 23:17:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 10 Mar 2022 23:17:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 10 Mar 2022 23:17:24 GMT
EXPOSE 80
# Thu, 10 Mar 2022 23:17:26 GMT
EXPOSE 443
# Thu, 10 Mar 2022 23:17:28 GMT
EXPOSE 2019
# Thu, 10 Mar 2022 23:18:46 GMT
RUN caddy version
# Thu, 10 Mar 2022 23:18:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9d7e8231020fca55f52d14b8a7ce3656ea1a0f7add52d65e90f62121fe48b8`  
		Last Modified: Thu, 10 Mar 2022 23:23:16 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af80d92ff4032a4af7c432751719331889e3987e12e65d34d5ebb282a20c93e9`  
		Last Modified: Thu, 10 Mar 2022 23:23:20 GMT  
		Size: 12.6 MB (12581604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d3ae26f04e000ad3d59599134e362ac56f63587121dfd8c289ad4d7198b2c6`  
		Last Modified: Thu, 10 Mar 2022 23:23:16 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe189798f275d20c78e39c5899fde1e4eb39b5215c94602a02494919622fbd1`  
		Last Modified: Thu, 10 Mar 2022 23:23:15 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bb6704511f5e25c596bb4da2e3876a4ff94d636a5a864cdc2081fa0c8c90e8`  
		Last Modified: Thu, 10 Mar 2022 23:23:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60f4b9d1b8e2632e8c4b5a2ba5cef7b9d320a84cdc2f9b1602bf958c0eae59`  
		Last Modified: Thu, 10 Mar 2022 23:23:14 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad4d74ac905f41961ea9c19da27a83ecf1f9e61f9f11698d8f6640f1ee42463`  
		Last Modified: Thu, 10 Mar 2022 23:23:13 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c1b1b3adc2fba2aafe3fabc3589db5fee1a3e8804da41d5c86c57b9f715e34`  
		Last Modified: Thu, 10 Mar 2022 23:23:14 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920aeb6981196ccd526b2c147b65406c9e7ad753928b540d38b06ce826a10989`  
		Last Modified: Thu, 10 Mar 2022 23:23:13 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3c1945a551d9fd87cdad01e126234fc6c19447c16283c1b7f3a9aaeaa85b`  
		Last Modified: Thu, 10 Mar 2022 23:23:12 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20fc2235c71cef450cb31287142ec7b1653b8aa10e4df09251c2fee9e45e9bfb`  
		Last Modified: Thu, 10 Mar 2022 23:23:12 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1f868d3e6e3b7aeba72b31e537c64540b5cd47876b29dbc6b99449b042c77b`  
		Last Modified: Thu, 10 Mar 2022 23:23:11 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1709c223988941e572100de0e0416fd946212338a4b82d0bf6157a0a9cffb`  
		Last Modified: Thu, 10 Mar 2022 23:23:11 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31826e49182a6b827ba6af55bc08c92b46dcbd38b71dcfb68a76fa4b184624d`  
		Last Modified: Thu, 10 Mar 2022 23:23:11 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10bff2600becf937738dbbeabc119db87dc7bbf300de826c6f356cdf07824b4`  
		Last Modified: Thu, 10 Mar 2022 23:23:09 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39bd343b434eec8e57160a0b4c89e93ef67e08138859c36a8c46c14cbda37ca7`  
		Last Modified: Thu, 10 Mar 2022 23:23:09 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14b1140f1d1c8b21f9bcd3ceb8f5dea64077c8d7cc78b9b4d9ed5b2f490cecd`  
		Last Modified: Thu, 10 Mar 2022 23:23:09 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d5743206ba889ce28c20481d33002512a479d915ae0c5dfc5a8d01bbd943ed`  
		Last Modified: Thu, 10 Mar 2022 23:23:09 GMT  
		Size: 307.8 KB (307825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f83df86e60e5b4e53108b5e0b1bf84a1c3bba826dd3ac59b4f7a1ac79a59908`  
		Last Modified: Thu, 10 Mar 2022 23:23:09 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1` - windows version 10.0.20348.587; amd64

```console
$ docker pull caddy@sha256:190644b756f6e29fdd566242137d83a8ab8cb5da79c6eeb5a686acb280d0c87d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2234975577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec73698bb10b0a408086c4dd1fba649195a728ddf076a02f1e7367f9941183d0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Mar 2022 23:19:22 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 10 Mar 2022 23:19:23 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 23:19:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d3823cb9ec107805c996e0de561c460a8d865698362c6ba842a69503af693d8f7db8ac418abffc4b7110a273d0b8be50168f8a5bcc0dc4da1e81fd1a4271f9d2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 10 Mar 2022 23:19:49 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 10 Mar 2022 23:19:50 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 10 Mar 2022 23:19:51 GMT
VOLUME [c:/config]
# Thu, 10 Mar 2022 23:19:52 GMT
VOLUME [c:/data]
# Thu, 10 Mar 2022 23:19:52 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Thu, 10 Mar 2022 23:19:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 10 Mar 2022 23:19:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 10 Mar 2022 23:19:55 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 10 Mar 2022 23:19:56 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 10 Mar 2022 23:19:57 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 10 Mar 2022 23:19:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 10 Mar 2022 23:19:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 10 Mar 2022 23:20:00 GMT
EXPOSE 80
# Thu, 10 Mar 2022 23:20:01 GMT
EXPOSE 443
# Thu, 10 Mar 2022 23:20:02 GMT
EXPOSE 2019
# Thu, 10 Mar 2022 23:20:16 GMT
RUN caddy version
# Thu, 10 Mar 2022 23:20:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501204225ae4faaf2054af787801c79f59cd7e6764ba27480f88314d662fe8db`  
		Last Modified: Thu, 10 Mar 2022 23:23:35 GMT  
		Size: 618.1 KB (618083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1b161fdd7e1eff73e0b69b5a534a91cdc416dbc212d1d41e86ed77f1bbbb4b`  
		Last Modified: Thu, 10 Mar 2022 23:23:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec81d9b42cee80d858fed2642eb9fceb14a85637d3107bdd77360697068f968`  
		Last Modified: Thu, 10 Mar 2022 23:23:37 GMT  
		Size: 12.8 MB (12770708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf78f158dbd631347c47fa0b4b35ed7c16f4c617befa9f52fbae491a4a2085b`  
		Last Modified: Thu, 10 Mar 2022 23:23:32 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddd79c99dbc6f4dbaf32b5704dc85064b5abb0d388adf5d061eaab0e37b5afa`  
		Last Modified: Thu, 10 Mar 2022 23:23:33 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fdbdbcc0a58e8c38006e9b158adc19da95d85b019433828016eac93f2c03ba`  
		Last Modified: Thu, 10 Mar 2022 23:23:31 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba8cfc63470c708385e8d8796cfeea6c650b82d68526bd52d26418ba8ef3a33`  
		Last Modified: Thu, 10 Mar 2022 23:23:31 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc704f14d84f4cd4b9a956f79720b1fa2fed3455d75920ae21828dba48e0a15c`  
		Last Modified: Thu, 10 Mar 2022 23:23:31 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7390fcba4513a938ed30807fc0a4f3dc62ec98c0c3a81070185b3332cba558d`  
		Last Modified: Thu, 10 Mar 2022 23:23:30 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4a1b650b0b42f48eb9be5a49262e9d61983a217fa6b9cef5c1c4e8ea6037a1`  
		Last Modified: Thu, 10 Mar 2022 23:23:30 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9efc512998552b2c0eb4fd62b04c41138f65d14796d706304028d70fbc6b30`  
		Last Modified: Thu, 10 Mar 2022 23:23:29 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05756c324de05267a5034909e0c59ce72d9f72b09fab332779f98cd3801f0232`  
		Last Modified: Thu, 10 Mar 2022 23:23:28 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43f983684908d82bbab9bbc2f115c19a1f78b5048872a5e54f8d3d208e89fb6`  
		Last Modified: Thu, 10 Mar 2022 23:23:28 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3b450029ff204db60d8023c9e526c38205aec114ab62d67351b1f19004b330`  
		Last Modified: Thu, 10 Mar 2022 23:23:28 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18554b6031813cc80f8ba7e5e1df6f947821e1d1d0a6cab8e410f650209d86ae`  
		Last Modified: Thu, 10 Mar 2022 23:23:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bfbc8f27994a32c626bcad31c573c825f23474b2d2167338ee0d35de1e6099`  
		Last Modified: Thu, 10 Mar 2022 23:23:26 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9e9fb9ea227f0f6e8f513e977a1965a7de7aa0d22c26685a156828a8ebf06c`  
		Last Modified: Thu, 10 Mar 2022 23:23:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35636b68f6f3e0d03a7ba26fb4b136786e49e7a155fecbfd189ba95f4e6f42c`  
		Last Modified: Thu, 10 Mar 2022 23:23:26 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98050fbe661913690cee263b64e5c1defd894c209a4ac627acd69b806ba17e7a`  
		Last Modified: Thu, 10 Mar 2022 23:23:26 GMT  
		Size: 314.3 KB (314344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2dc85353d3e550445d387372cf10180870b8aa3bdf523148585e354588bfb4`  
		Last Modified: Thu, 10 Mar 2022 23:23:26 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-beta.1-alpine`

```console
$ docker pull caddy@sha256:bd9bf209e694c63dbfb34f04547c62c8fb4c5afca702f2674d551b3163e63864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.5.0-beta.1-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:bac7580bfb78e7d7aedf9044ff33ba0a461e236bbe724253240722a2c2833b37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15281277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4004608d8af3d2fb6ce0c5961777a4106636aa68d2ed9809df92c5b85acff4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:25:00 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 04:25:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 04:25:01 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 04:25:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 04:25:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:25:07 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 04:25:07 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 04:25:07 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 04:25:07 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 04:25:07 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Tue, 05 Apr 2022 04:25:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 04:25:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 04:25:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 04:25:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 04:25:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 04:25:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 04:25:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 04:25:08 GMT
EXPOSE 80
# Tue, 05 Apr 2022 04:25:08 GMT
EXPOSE 443
# Tue, 05 Apr 2022 04:25:08 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 04:25:08 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 04:25:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87ed6b8c4412bcd2bb1f40611012b40444b12071baf4884d0e75044fc1f32c1`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 291.5 KB (291522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840ff7bd6e2c9d7717705a52c1d27654581f987e1a43d2c9f3220ce850a5cdad`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05594f38e13e9c731a8ab55b382f8af8c26f09320e016462a84c4f7ea29b09a`  
		Last Modified: Tue, 05 Apr 2022 04:25:50 GMT  
		Size: 12.2 MB (12169217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3c7da94e5fbe8d331bb4363cff609ee7a5af046d180358dfdb9745ba19a2c1`  
		Last Modified: Tue, 05 Apr 2022 04:25:48 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:995e1ee69c4e941859c8fe08ee8c7ae5d7e449f4e5243d0618391c04353271f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14451284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f8e1c5a4506d1ba5fe3ba7e360fe1bdd8a8668ceb8306da0e02fae7ba993e2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:15:01 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:15:03 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 03:15:04 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 03:15:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 03:15:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 03:15:10 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 03:15:10 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 03:15:11 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 03:15:11 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 03:15:12 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Tue, 05 Apr 2022 03:15:12 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 03:15:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 03:15:13 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 03:15:13 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 03:15:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 03:15:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 03:15:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 03:15:15 GMT
EXPOSE 80
# Tue, 05 Apr 2022 03:15:16 GMT
EXPOSE 443
# Tue, 05 Apr 2022 03:15:16 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 03:15:17 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 03:15:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b230dd773e10769a2eb3e507260d2470a646efd48a639739ba8852b2915302`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 291.7 KB (291685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac48280871fa0cc6e20550e9909af62acb5b3793a4ada967e49e60367ec386e`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150950fa1b63c40e7ca5764cdeb7988d8a15f550762999723e6e9659c38282c5`  
		Last Modified: Tue, 05 Apr 2022 03:18:18 GMT  
		Size: 11.5 MB (11531644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b85c24743ba55b919e1a0b33c9589948cbef4830c588108e9698ce11235633`  
		Last Modified: Tue, 05 Apr 2022 03:18:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:64dcd6e2cc4aad2c2c89bb7cded9819935056ee5c8aaa4f9ef182bc356435ff1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14232949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946580d1e058d0c7451feaf278c204e5bc0da968acf3f2807928c02b8fbcdbd9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:33:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:33:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 06:33:08 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 06:33:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 06:33:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:33:14 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 06:33:14 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 06:33:15 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 06:33:15 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 06:33:15 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Tue, 05 Apr 2022 06:33:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 06:33:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 06:33:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 06:33:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 06:33:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 06:33:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 06:33:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 06:33:19 GMT
EXPOSE 80
# Tue, 05 Apr 2022 06:33:19 GMT
EXPOSE 443
# Tue, 05 Apr 2022 06:33:20 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 06:33:20 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 06:33:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03203881a2568530a735b6e0e7a40ebb79adedc5193a675807b04eeb92cc6ed1`  
		Last Modified: Tue, 05 Apr 2022 06:35:07 GMT  
		Size: 290.7 KB (290668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2de87d2e387fcc410ddd706bbe177b2a04b5137087a6ffca70b45c80dc976e0`  
		Last Modified: Tue, 05 Apr 2022 06:35:08 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfc5deee1bf6f6600fe8402d08138fbf5fb1e9132ae3e820cb274ff78de74c0`  
		Last Modified: Tue, 05 Apr 2022 06:35:15 GMT  
		Size: 11.5 MB (11511975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c950586adcccfcf1ec15e40da0fb338ab975c2f6d63a3f49fbd43ab5a6b9b6`  
		Last Modified: Tue, 05 Apr 2022 06:35:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:99a7c0298ba26e39221504632853f0c12b3cc6d51ebf1d957a8614c2ac62298f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14151675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181d197c22004b9c4242984dee400be86b249372bad74740eb818cc9febf0be6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:12:15 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:12:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 03:12:17 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 03:12:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 03:12:21 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 03:12:22 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 03:12:23 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 03:12:24 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 03:12:25 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 03:12:26 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Tue, 05 Apr 2022 03:12:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 03:12:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 03:12:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 03:12:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 03:12:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 03:12:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 03:12:33 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 03:12:34 GMT
EXPOSE 80
# Tue, 05 Apr 2022 03:12:35 GMT
EXPOSE 443
# Tue, 05 Apr 2022 03:12:36 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 03:12:37 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 03:12:38 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aa37f2341b1e6d98420668c9bc849a47f2c471d159b2303885040bd8d0a92f`  
		Last Modified: Tue, 05 Apr 2022 03:13:38 GMT  
		Size: 291.3 KB (291301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e87f72d84fd403dc0ea7d95672e5865925fca64a932f046b39035e8d3b43aae`  
		Last Modified: Tue, 05 Apr 2022 03:13:37 GMT  
		Size: 5.7 KB (5747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e0ff4c04fc65e4d2e778c739fe0dff0ca9b8006b0ea5e71af2210c38c1ef87`  
		Last Modified: Tue, 05 Apr 2022 03:13:41 GMT  
		Size: 11.1 MB (11137996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cf9a10ab3f4c966798e5ce44cc9569cc31658785767c0d438f7a435666f055`  
		Last Modified: Tue, 05 Apr 2022 03:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:98a632b2c106991170be442d14b4ed3db078616bd2c5787604c1688ea46b5af0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13786562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3e24a28142e386eb1c4b37b83e291e4256a3f481e3a354f3b4bd160d8156c5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:08:34 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 07:08:43 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 07:08:45 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 07:08:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 07:09:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:09:06 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 07:09:08 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 07:09:11 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 07:09:13 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 07:09:17 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Tue, 05 Apr 2022 07:09:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 07:09:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 07:09:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 07:09:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 07:09:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 07:09:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 07:09:48 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 07:09:55 GMT
EXPOSE 80
# Tue, 05 Apr 2022 07:09:58 GMT
EXPOSE 443
# Tue, 05 Apr 2022 07:10:00 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 07:10:04 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 07:10:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743509d6ced044a369685ebb068417e8757981a39d1b397c7b0182ab89f83528`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 293.7 KB (293721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029325992e21f613a5b486751627c7d5e5c7622ec29d4d170549f4dac13ad291`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79976b8a08e399f4d6fd3eb19500adbb418be5088bda898ef58f47c6791c2aa`  
		Last Modified: Tue, 05 Apr 2022 07:11:26 GMT  
		Size: 10.7 MB (10675672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6866f1a9b35b79bf3c4b8bf13c2c2d5b1ffd33351937a641fc88f72ed011a0a7`  
		Last Modified: Tue, 05 Apr 2022 07:11:24 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:5dc3ae5b9a9ec370660f1a192517138ca1f1822436e05f51f2cfd7d8969c901a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14627648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e041975d62fa3de352fb55c2d7349d1f7a023f98d76da64f25a9ef635bf442a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:19:41 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:19:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 06:19:42 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 06:19:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 06:19:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:19:45 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 06:19:45 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 06:19:45 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 06:19:45 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 06:19:45 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Tue, 05 Apr 2022 06:19:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 06:19:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 06:19:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 06:19:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 06:19:46 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 06:19:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 06:19:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 06:19:46 GMT
EXPOSE 80
# Tue, 05 Apr 2022 06:19:46 GMT
EXPOSE 443
# Tue, 05 Apr 2022 06:19:47 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 06:19:47 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 06:19:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8cc7c7c7ffd67f5740add448d341753330a2abdc6ed06e995cb7d28de381ab`  
		Last Modified: Tue, 05 Apr 2022 06:20:44 GMT  
		Size: 291.8 KB (291821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36f8e9524a50422cbb86b1c5e3af26710e4b65591ecc118a5079f1aa7fe5a67`  
		Last Modified: Tue, 05 Apr 2022 06:20:45 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d9efb35d6033b2097e2b43f03270f6509c549e025a79566426a0c5e9450cf6`  
		Last Modified: Tue, 05 Apr 2022 06:20:46 GMT  
		Size: 11.7 MB (11729468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f7e89e0dae073ed741dd140b8085f3e69a24baa02f5c4e762e24aece4e7d5e`  
		Last Modified: Tue, 05 Apr 2022 06:20:44 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-beta.1-builder`

```console
$ docker pull caddy@sha256:147b9bdf419565bd0059656014d3659a7b995af067d8e3c3ef47b7feb6a56e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2686; amd64
	-	windows version 10.0.20348.587; amd64

### `caddy:2.5.0-beta.1-builder` - linux; amd64

```console
$ docker pull caddy@sha256:2f7a6246c68a0addf07beb9ae5be81ec7ddf97aaedf8deadcee5f22ca3a9d3e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121342541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4361676d01ba55c18c856a5b6a27803ef4f1a3d7ffc343a6e38abc822b2dac72`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:32:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 05:32:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 05:32:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:37:30 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 05:39:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 05:39:29 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 05:39:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:39:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 05:39:30 GMT
WORKDIR /go
# Tue, 05 Apr 2022 15:45:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 15:45:54 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 15:46:00 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 15:46:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 15:46:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 15:46:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 15:46:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc419b0ee22d1bb5f3b95a57b2edc733b7b585277f8101db7b2c9b53605c1b`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 272.0 KB (271965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc292e5bacdd8b97a1632a82d0fd0ee6c2692409bd4b35cb9e7e652efbc7c8`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dea7a3ad9148616176ac7fd686181a6e3c4eaac3746166e678a11017e4d32d9`  
		Last Modified: Tue, 05 Apr 2022 05:43:55 GMT  
		Size: 110.2 MB (110188123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35228ee6d672a4ef2501b746851ae8dc63cdc2612057a726a7affcd9d7d9f08`  
		Last Modified: Tue, 05 Apr 2022 05:43:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431098d05c7f64b1b215f6e58d58584efa1b85c22de1e46eabdf9f41c9a31550`  
		Last Modified: Tue, 05 Apr 2022 15:46:24 GMT  
		Size: 6.8 MB (6821467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8354d237445c3d0112c622a86ac98178a887b68f8cf8757a5182f35138b79561`  
		Last Modified: Tue, 05 Apr 2022 15:46:36 GMT  
		Size: 1.2 MB (1245713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944857a899b517d43dbd8b8d0d831689c3d69c2bd34248f6fcfb18d125ee0185`  
		Last Modified: Tue, 05 Apr 2022 15:46:36 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:c121081ce22a603e198876486cfc15bd66e1ea76230dc153771520db29a31d5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115819311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb77f3679a567287da457ecde12550bf5a222e8e7cc17d4c93c0a41330880503`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:39:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 11:59:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 11:59:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 12:07:43 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 12:10:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 12:10:56 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 12:10:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 12:10:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 12:10:58 GMT
WORKDIR /go
# Tue, 05 Apr 2022 18:47:17 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 18:47:18 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 18:47:46 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 18:47:47 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 18:47:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 18:47:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 18:47:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560305eea4784da98378676b22f9871093d6a4d7eb88292accc17f0cfd6b12ea`  
		Last Modified: Tue, 05 Apr 2022 11:40:22 GMT  
		Size: 272.1 KB (272138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145a805e932abbcca6b77ad458c7ac26275ff4f23af9912d2c4d3dac9eef4cf8`  
		Last Modified: Tue, 05 Apr 2022 12:15:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc18cdc5d172f77e8e9ab98b63b490a7ee5597737555f86ab3df9580d7603038`  
		Last Modified: Tue, 05 Apr 2022 12:20:29 GMT  
		Size: 105.1 MB (105068577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a00aaf29b7cc08e00fa3ad26938794099e739101e45a4efbd80da84b4b59e8`  
		Last Modified: Tue, 05 Apr 2022 12:19:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce9447fafc122cfcae03e938e9b3bf3750eda3436a83625bc1229d67e6f3526`  
		Last Modified: Tue, 05 Apr 2022 18:49:07 GMT  
		Size: 6.7 MB (6677398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497c1d3714af0b8e4363bfdca0eb6ed3a90222636053647aa93c4d0b9822ea93`  
		Last Modified: Tue, 05 Apr 2022 18:49:24 GMT  
		Size: 1.2 MB (1178511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17eeb76d48a898c902232cd6015c64c3105b5958eae158822e58143a4b37374b`  
		Last Modified: Tue, 05 Apr 2022 18:49:24 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:46e8de3418b30e4d0c73091f48ca7272af113b2231827d181058c0690299cfbc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114678400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15a48ed4c6ddea63b63907d7e1139163787fc1a4f2dcbd1f02d35a9970f7258`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:19:56 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:19:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:19:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:28:26 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 09:31:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 09:31:38 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 09:31:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:31:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 09:31:40 GMT
WORKDIR /go
# Wed, 06 Apr 2022 02:23:29 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 06 Apr 2022 02:23:29 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 06 Apr 2022 02:23:58 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 06 Apr 2022 02:23:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Apr 2022 02:24:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 06 Apr 2022 02:24:01 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 06 Apr 2022 02:24:01 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f68dacdb1dfe1ed299ab3e43e478a27f0977380bbefc4c7ca5723758dbac6`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 271.1 KB (271116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431ad618c287090e481554b57afdc0383f065b5bbfc0ccdcefc6518e1a8331e`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1c19e6ea71a7140e1f92aaf1ca20998b7875298f5f0aecdad1849acea539e9`  
		Last Modified: Tue, 05 Apr 2022 09:43:01 GMT  
		Size: 104.9 MB (104853355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d18ca61f70738e42fc01d4076606b8ef68be3c58058c1922e2b44987e87a15`  
		Last Modified: Tue, 05 Apr 2022 09:41:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d951a4c4c0e205bd2d3656382822e0ad97c4ee98c7cc185614d9363d5b7b18df`  
		Last Modified: Wed, 06 Apr 2022 02:25:20 GMT  
		Size: 6.0 MB (5952176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc619e37ad9461e5adce59223051ac7835d62f4ff59ec13dd09cc8fe03386bb6`  
		Last Modified: Wed, 06 Apr 2022 02:25:38 GMT  
		Size: 1.2 MB (1176714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4be834d337fe68ed4f43831e9e9969f38dd4283be0aec04d58c2a9f9d54e81`  
		Last Modified: Wed, 06 Apr 2022 02:25:37 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b189449535bb46a177f107828f29eefe226c211c6d526efc30143930c8c72326
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115488050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8577f46e39a34180630e6bc132297c3a7687a1835fafbbcd8c1b504a2bb52514`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:38:07 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 07:38:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:38:08 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:41:43 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 07:43:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 07:43:02 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 07:43:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 07:43:05 GMT
WORKDIR /go
# Tue, 05 Apr 2022 17:39:06 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 17:39:07 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 17:39:25 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 17:39:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 17:39:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 17:39:28 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 17:39:28 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7637d0a7b497b253b73e807a5e676ba3f0750afafa9e1a4c61260513feb321f`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 271.8 KB (271764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda57b85efde0ed435315f4f74625e7a055107aa29e8c91a313ca6d525fb709c`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d20097de21a08b3879d9d8acda7ea55af524f6cb8cf3d8526c7ad583992e7f`  
		Last Modified: Tue, 05 Apr 2022 07:47:32 GMT  
		Size: 104.4 MB (104424495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662c5a329cf0f527093cef90725754463b5ab87a23be5a91edff92a844e76c37`  
		Last Modified: Tue, 05 Apr 2022 07:47:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f1e21bd0bbbfa99416af4431f653df5121e14b29364c870d86362268419104`  
		Last Modified: Tue, 05 Apr 2022 17:40:06 GMT  
		Size: 6.9 MB (6925952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f13338e5fed641e40be45c51bf4064de57d5f38c54302cb3f45f2751254c4c3`  
		Last Modified: Tue, 05 Apr 2022 17:40:23 GMT  
		Size: 1.1 MB (1148676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d365e4381114bed779052a3f925786611612f5f0b7da23c6b1e9d53d1e15f5`  
		Last Modified: Tue, 05 Apr 2022 17:40:22 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:62a7c1d33fc67c9b71132339970055aed58ce3edd96bf8a2caa7db07f1a088e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114312522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eade2a29b9eba1bd13ba87a2c669e34812cc902cc873b50ffacf682f822118f3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:50:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:50:19 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:50:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:57:52 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 10:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 10:00:43 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 10:00:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 10:00:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 10:00:55 GMT
WORKDIR /go
# Wed, 06 Apr 2022 02:52:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 06 Apr 2022 02:53:02 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 06 Apr 2022 02:53:42 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 06 Apr 2022 02:53:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Apr 2022 02:53:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 06 Apr 2022 02:53:55 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 06 Apr 2022 02:53:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcdc2e904e95f788aa4c66c5ce746890d6a02abca4c94711443f5c688b61ebf`  
		Last Modified: Tue, 05 Apr 2022 10:06:11 GMT  
		Size: 274.2 KB (274171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04802687d9aa11413122df45eb15c7d7f85937270997b441d1c6a09001730453`  
		Last Modified: Tue, 05 Apr 2022 10:06:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce62b250e0aee7f0aec0715e9113355ac5a4781c1eaf0d4bea6fcdf4073068f8`  
		Last Modified: Tue, 05 Apr 2022 10:08:01 GMT  
		Size: 102.8 MB (102784652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c7dcfaac085766cdaa5fce90fb5c664130f22fa3f6005b3cebddf45a4e2b9b`  
		Last Modified: Tue, 05 Apr 2022 10:07:43 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7a86ae8bfd11a7525de064d7143eed347098156c965551db06b0da1fab2f67`  
		Last Modified: Wed, 06 Apr 2022 02:54:45 GMT  
		Size: 7.3 MB (7320952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0c1522f46b06b20e754f09fd417e5b522acf7b915a44a6cad6fe90bad02db9`  
		Last Modified: Wed, 06 Apr 2022 02:55:04 GMT  
		Size: 1.1 MB (1120844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaec64dc6b0c2892c44454f4ce84e9687ac350308af8c09e1b3aa2ce2765c42c`  
		Last Modified: Wed, 06 Apr 2022 02:55:03 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder` - linux; s390x

```console
$ docker pull caddy@sha256:9ba130fc612fa21ac7394cde419c78e0fcfd0f666ab9505f7192d1524dd6c078
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118747452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bf60c3b8fb5c4231333c71e7f050d096e0b3de1f42003220a65f901d96b242`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:08:51 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 06:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:44:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:48:26 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 06:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 06:49:56 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 06:49:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:49:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 06:49:57 GMT
WORKDIR /go
# Tue, 05 Apr 2022 14:02:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 14:02:02 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 14:02:18 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 14:02:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 14:02:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 14:02:19 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 14:02:19 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72593bb761a2ce336603e9e84973d1e284f39e0188e758ad8bc22c45cd9b6395`  
		Last Modified: Tue, 05 Apr 2022 06:09:13 GMT  
		Size: 272.3 KB (272267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf480933488ffcb2c9c9269292e2e3d643bea6eeb04cf948790ca50666a61c8`  
		Last Modified: Tue, 05 Apr 2022 06:53:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b3e51e0eff0c3e6118a6448425ada0b8e1725d738559d5b5e29ef58c570e8d`  
		Last Modified: Tue, 05 Apr 2022 06:54:30 GMT  
		Size: 107.7 MB (107739421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86765c73189fadce4ca276af5f7d9440213d5986a9687b648a51d45978e3a8c4`  
		Last Modified: Tue, 05 Apr 2022 06:54:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f50aeaf488b81d4c5d54c453b47637b6fbdfae9ca014728018463ce30aa78b`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 6.9 MB (6930892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ae06532c5b47a5e13d45f16dbda523abcb5fb38ed2ecacc6ac918a97c5df5f`  
		Last Modified: Tue, 05 Apr 2022 14:03:12 GMT  
		Size: 1.2 MB (1203783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ec0665f41221821b85ebd8d877934c36d3e93aed6228fcde2e3727228d99c2`  
		Last Modified: Tue, 05 Apr 2022 14:03:12 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:0e7f812fa3e2ecc803dd4fb7b20a72dd1c75759ce49778f51ea9a5bd1719b22d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888394649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1badd557216606e841971ecc4296c63549a10a87cecd522cd7b7c2fa6c353d93`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 13:17:25 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Mar 2022 13:17:26 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Mar 2022 13:17:27 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Mar 2022 13:17:28 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Mar 2022 13:19:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:19:56 GMT
ENV GOPATH=C:\go
# Wed, 09 Mar 2022 13:20:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Mar 2022 13:35:10 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 09 Mar 2022 13:38:26 GMT
RUN $url = 'https://dl.google.com/go/go1.17.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '85ccf2608dca6ea9a46b6538c9e75e7cf2aebdf502379843b248e26b8bb110be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:38:28 GMT
WORKDIR C:\go
# Wed, 09 Mar 2022 18:27:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Mar 2022 23:14:28 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 23:20:35 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 23:20:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 23:21:34 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('fc6f2a7feb8f0936a0e04d3c9ea26d0404c2f4907eb436eb60e33152c22c1211f851c46606573fcb5c3334f8cc4f7f810b28b917a9f313f6454d1c5cd0f50f8a')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 10 Mar 2022 23:21:35 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7705bbffd7dc00934e935de0e00e09a7b0da55d66c596622f094495478dd71`  
		Last Modified: Wed, 09 Mar 2022 14:04:13 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be7ff0bb187d149a5cf3c76e1ec444d0e07c6606f67b2c921c67ec91829ea03`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876223f25b257577440a80fdee021b43c33ce3c56be9a20b2ddeaede95240522`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991eea244b9c3a1849c84748425dd9e9fbf9ec359ad9329796131b929239ffa4`  
		Last Modified: Wed, 09 Mar 2022 14:04:11 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b4c7c9740eb99bf626b312aa69396db3d186c5bd0e092b01c078ca7248e386`  
		Last Modified: Wed, 09 Mar 2022 14:04:40 GMT  
		Size: 25.5 MB (25454695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6c8a4d4848c21636a48a69a569a5372ec4890ea029f1f620dda76078bdcef`  
		Last Modified: Wed, 09 Mar 2022 14:04:09 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac6d527939082add6d21652ba4888acc5a6e7607365168d8e61fb1485339cb`  
		Last Modified: Wed, 09 Mar 2022 14:04:10 GMT  
		Size: 313.6 KB (313592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37aeceb8c2e5bb3c500129bcf20c3f8aea8c68c353e6714a63a225ed1546e8a1`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d88cd595dc7580d72420b7288c52d4b32201045a13dda1a7b943d9a3468adef`  
		Last Modified: Wed, 09 Mar 2022 14:13:05 GMT  
		Size: 145.5 MB (145488847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be492983ee2b2c9128ce0c732c441ae5fbd203cdb71c94faa253c24b01750c90`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa7b09ca61eb1fbafacee427b430b0879ad4da23e62e430a3fe6a66f181f642`  
		Last Modified: Wed, 09 Mar 2022 18:30:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74014ffde8e1a1677cd81e965bcd2b1f5287bcbf682bbce3bdd125052cd04f29`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281142ca6a15b21cfc34926357f799ac7c38783ca3875011b160c096c3229d65`  
		Last Modified: Thu, 10 Mar 2022 23:23:43 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc359b64dd95e97e38c7d61691e76c179b77cc013db0f1076e98fe6bb7be82bc`  
		Last Modified: Thu, 10 Mar 2022 23:23:43 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde3c36ea4dbe6709a5c743097ec10680741b0e35b0e9d41b2b703ed388f6cb4`  
		Last Modified: Thu, 10 Mar 2022 23:23:44 GMT  
		Size: 1.7 MB (1666531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389f0b289a5870da81d3b2ef7f3c7d5b1fb87e5f103073f2f7698ecafbef39a`  
		Last Modified: Thu, 10 Mar 2022 23:23:43 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder` - windows version 10.0.20348.587; amd64

```console
$ docker pull caddy@sha256:8a2e818f9a28bbd1dd99edd69a77b39ff9b5447b52226a98ab1aac9992f6ee29
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2395021082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a46232eca5f0ad5b7c29ac6bba9315f92b55caaf663cdf7404af3383e1549c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 13:12:32 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Mar 2022 13:12:34 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Mar 2022 13:12:35 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Mar 2022 13:12:36 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Mar 2022 13:13:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:13:33 GMT
ENV GOPATH=C:\go
# Wed, 09 Mar 2022 13:14:00 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Mar 2022 13:32:11 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 09 Mar 2022 13:34:51 GMT
RUN $url = 'https://dl.google.com/go/go1.17.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '85ccf2608dca6ea9a46b6538c9e75e7cf2aebdf502379843b248e26b8bb110be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:34:53 GMT
WORKDIR C:\go
# Thu, 10 Mar 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Mar 2022 23:21:49 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 23:21:50 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 23:21:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 23:22:16 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('fc6f2a7feb8f0936a0e04d3c9ea26d0404c2f4907eb436eb60e33152c22c1211f851c46606573fcb5c3334f8cc4f7f810b28b917a9f313f6454d1c5cd0f50f8a')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 10 Mar 2022 23:22:17 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f0159fc3ccac7854a42bd259b35d4a6482bc698865860892cf564a444b3c63`  
		Last Modified: Wed, 09 Mar 2022 14:03:12 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45aae60408220ac14736ec0b59de947d214ff276f074c4d716f9f2107b81671`  
		Last Modified: Wed, 09 Mar 2022 14:03:09 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eec0ac452237f9eaa33ce02c78ae43641960a5cd004be40f1e99f8eda401f78`  
		Last Modified: Wed, 09 Mar 2022 14:03:09 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b14ad7e0d74c6938398565f29103030d14231a39603cb3fef811fa8a55be4a`  
		Last Modified: Wed, 09 Mar 2022 14:03:09 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8065b93123915e69465b4ba5e604b150fa39c4157166451453950874ce4dedf`  
		Last Modified: Wed, 09 Mar 2022 14:03:16 GMT  
		Size: 25.7 MB (25684294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce2ababcffd2ebaadd4d6756c1408d978cbb56bfb5fac29069bf777e6eee0fd`  
		Last Modified: Wed, 09 Mar 2022 14:03:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cd0da17ace6307cacfc21df261451fc8967bbefa8bea2f39da28a647dc391d`  
		Last Modified: Wed, 09 Mar 2022 14:03:04 GMT  
		Size: 512.4 KB (512354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42222c033855a8bddbeb67a0b4cff5b2999afd4119720ee7e4fe9f6c59756404`  
		Last Modified: Wed, 09 Mar 2022 14:11:16 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73cbf8abb1840e446af856b56aac5dd2a832cfe370e17f2ee7b4cbea84ee32d`  
		Last Modified: Wed, 09 Mar 2022 14:12:03 GMT  
		Size: 145.7 MB (145695821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d3ebd62db6d310f5584c9e38da9d33e106ef41c0fbfc4fe4f99031b01cf183`  
		Last Modified: Wed, 09 Mar 2022 14:11:16 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af42907e59cd53434417a3cee16107b6fd3c9e583a7e92f403da1edc9c8881d5`  
		Last Modified: Thu, 10 Mar 2022 23:23:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2dba9ee51310a6df87f204c28a7052ce8cfe8fe4054efe85de312fd9ebd0d2a`  
		Last Modified: Thu, 10 Mar 2022 23:23:50 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90ed7f357bfb619820be785ff8397518d8b81f789fe33d1a458aa78a0b2c293`  
		Last Modified: Thu, 10 Mar 2022 23:23:50 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcaade4b90a730c916671b2dce519d031c74921051d042a36460fb347c4f0f43`  
		Last Modified: Thu, 10 Mar 2022 23:23:50 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fb19e6205c8bf8fb08f0d0c098c493b74d6a86d71667408aa1fe3f689c0d1f`  
		Last Modified: Thu, 10 Mar 2022 23:23:52 GMT  
		Size: 1.9 MB (1863109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cafb79352f1994a6c222b27e70e550375956842aa86e55ba656bcc19c61031`  
		Last Modified: Thu, 10 Mar 2022 23:23:50 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-beta.1-builder-alpine`

```console
$ docker pull caddy@sha256:d9560610fb22a98648bc10f275f1d7aeb2eadb047c6385fc5b07d9a229c57cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.5.0-beta.1-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:2f7a6246c68a0addf07beb9ae5be81ec7ddf97aaedf8deadcee5f22ca3a9d3e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121342541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4361676d01ba55c18c856a5b6a27803ef4f1a3d7ffc343a6e38abc822b2dac72`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:32:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 05:32:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 05:32:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:37:30 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 05:39:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 05:39:29 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 05:39:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:39:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 05:39:30 GMT
WORKDIR /go
# Tue, 05 Apr 2022 15:45:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 15:45:54 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 15:46:00 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 15:46:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 15:46:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 15:46:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 15:46:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc419b0ee22d1bb5f3b95a57b2edc733b7b585277f8101db7b2c9b53605c1b`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 272.0 KB (271965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc292e5bacdd8b97a1632a82d0fd0ee6c2692409bd4b35cb9e7e652efbc7c8`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dea7a3ad9148616176ac7fd686181a6e3c4eaac3746166e678a11017e4d32d9`  
		Last Modified: Tue, 05 Apr 2022 05:43:55 GMT  
		Size: 110.2 MB (110188123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35228ee6d672a4ef2501b746851ae8dc63cdc2612057a726a7affcd9d7d9f08`  
		Last Modified: Tue, 05 Apr 2022 05:43:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431098d05c7f64b1b215f6e58d58584efa1b85c22de1e46eabdf9f41c9a31550`  
		Last Modified: Tue, 05 Apr 2022 15:46:24 GMT  
		Size: 6.8 MB (6821467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8354d237445c3d0112c622a86ac98178a887b68f8cf8757a5182f35138b79561`  
		Last Modified: Tue, 05 Apr 2022 15:46:36 GMT  
		Size: 1.2 MB (1245713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944857a899b517d43dbd8b8d0d831689c3d69c2bd34248f6fcfb18d125ee0185`  
		Last Modified: Tue, 05 Apr 2022 15:46:36 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:c121081ce22a603e198876486cfc15bd66e1ea76230dc153771520db29a31d5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115819311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb77f3679a567287da457ecde12550bf5a222e8e7cc17d4c93c0a41330880503`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:39:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 11:59:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 11:59:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 12:07:43 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 12:10:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 12:10:56 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 12:10:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 12:10:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 12:10:58 GMT
WORKDIR /go
# Tue, 05 Apr 2022 18:47:17 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 18:47:18 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 18:47:46 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 18:47:47 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 18:47:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 18:47:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 18:47:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560305eea4784da98378676b22f9871093d6a4d7eb88292accc17f0cfd6b12ea`  
		Last Modified: Tue, 05 Apr 2022 11:40:22 GMT  
		Size: 272.1 KB (272138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145a805e932abbcca6b77ad458c7ac26275ff4f23af9912d2c4d3dac9eef4cf8`  
		Last Modified: Tue, 05 Apr 2022 12:15:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc18cdc5d172f77e8e9ab98b63b490a7ee5597737555f86ab3df9580d7603038`  
		Last Modified: Tue, 05 Apr 2022 12:20:29 GMT  
		Size: 105.1 MB (105068577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a00aaf29b7cc08e00fa3ad26938794099e739101e45a4efbd80da84b4b59e8`  
		Last Modified: Tue, 05 Apr 2022 12:19:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce9447fafc122cfcae03e938e9b3bf3750eda3436a83625bc1229d67e6f3526`  
		Last Modified: Tue, 05 Apr 2022 18:49:07 GMT  
		Size: 6.7 MB (6677398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497c1d3714af0b8e4363bfdca0eb6ed3a90222636053647aa93c4d0b9822ea93`  
		Last Modified: Tue, 05 Apr 2022 18:49:24 GMT  
		Size: 1.2 MB (1178511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17eeb76d48a898c902232cd6015c64c3105b5958eae158822e58143a4b37374b`  
		Last Modified: Tue, 05 Apr 2022 18:49:24 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:46e8de3418b30e4d0c73091f48ca7272af113b2231827d181058c0690299cfbc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114678400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15a48ed4c6ddea63b63907d7e1139163787fc1a4f2dcbd1f02d35a9970f7258`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:19:56 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:19:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:19:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:28:26 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 09:31:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 09:31:38 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 09:31:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:31:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 09:31:40 GMT
WORKDIR /go
# Wed, 06 Apr 2022 02:23:29 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 06 Apr 2022 02:23:29 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 06 Apr 2022 02:23:58 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 06 Apr 2022 02:23:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Apr 2022 02:24:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 06 Apr 2022 02:24:01 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 06 Apr 2022 02:24:01 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f68dacdb1dfe1ed299ab3e43e478a27f0977380bbefc4c7ca5723758dbac6`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 271.1 KB (271116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431ad618c287090e481554b57afdc0383f065b5bbfc0ccdcefc6518e1a8331e`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1c19e6ea71a7140e1f92aaf1ca20998b7875298f5f0aecdad1849acea539e9`  
		Last Modified: Tue, 05 Apr 2022 09:43:01 GMT  
		Size: 104.9 MB (104853355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d18ca61f70738e42fc01d4076606b8ef68be3c58058c1922e2b44987e87a15`  
		Last Modified: Tue, 05 Apr 2022 09:41:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d951a4c4c0e205bd2d3656382822e0ad97c4ee98c7cc185614d9363d5b7b18df`  
		Last Modified: Wed, 06 Apr 2022 02:25:20 GMT  
		Size: 6.0 MB (5952176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc619e37ad9461e5adce59223051ac7835d62f4ff59ec13dd09cc8fe03386bb6`  
		Last Modified: Wed, 06 Apr 2022 02:25:38 GMT  
		Size: 1.2 MB (1176714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4be834d337fe68ed4f43831e9e9969f38dd4283be0aec04d58c2a9f9d54e81`  
		Last Modified: Wed, 06 Apr 2022 02:25:37 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b189449535bb46a177f107828f29eefe226c211c6d526efc30143930c8c72326
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115488050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8577f46e39a34180630e6bc132297c3a7687a1835fafbbcd8c1b504a2bb52514`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:38:07 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 07:38:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:38:08 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:41:43 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 07:43:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 07:43:02 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 07:43:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 07:43:05 GMT
WORKDIR /go
# Tue, 05 Apr 2022 17:39:06 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 17:39:07 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 17:39:25 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 17:39:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 17:39:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 17:39:28 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 17:39:28 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7637d0a7b497b253b73e807a5e676ba3f0750afafa9e1a4c61260513feb321f`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 271.8 KB (271764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda57b85efde0ed435315f4f74625e7a055107aa29e8c91a313ca6d525fb709c`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d20097de21a08b3879d9d8acda7ea55af524f6cb8cf3d8526c7ad583992e7f`  
		Last Modified: Tue, 05 Apr 2022 07:47:32 GMT  
		Size: 104.4 MB (104424495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662c5a329cf0f527093cef90725754463b5ab87a23be5a91edff92a844e76c37`  
		Last Modified: Tue, 05 Apr 2022 07:47:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f1e21bd0bbbfa99416af4431f653df5121e14b29364c870d86362268419104`  
		Last Modified: Tue, 05 Apr 2022 17:40:06 GMT  
		Size: 6.9 MB (6925952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f13338e5fed641e40be45c51bf4064de57d5f38c54302cb3f45f2751254c4c3`  
		Last Modified: Tue, 05 Apr 2022 17:40:23 GMT  
		Size: 1.1 MB (1148676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d365e4381114bed779052a3f925786611612f5f0b7da23c6b1e9d53d1e15f5`  
		Last Modified: Tue, 05 Apr 2022 17:40:22 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:62a7c1d33fc67c9b71132339970055aed58ce3edd96bf8a2caa7db07f1a088e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114312522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eade2a29b9eba1bd13ba87a2c669e34812cc902cc873b50ffacf682f822118f3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:50:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:50:19 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:50:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:57:52 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 10:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 10:00:43 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 10:00:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 10:00:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 10:00:55 GMT
WORKDIR /go
# Wed, 06 Apr 2022 02:52:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 06 Apr 2022 02:53:02 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 06 Apr 2022 02:53:42 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 06 Apr 2022 02:53:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Apr 2022 02:53:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 06 Apr 2022 02:53:55 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 06 Apr 2022 02:53:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcdc2e904e95f788aa4c66c5ce746890d6a02abca4c94711443f5c688b61ebf`  
		Last Modified: Tue, 05 Apr 2022 10:06:11 GMT  
		Size: 274.2 KB (274171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04802687d9aa11413122df45eb15c7d7f85937270997b441d1c6a09001730453`  
		Last Modified: Tue, 05 Apr 2022 10:06:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce62b250e0aee7f0aec0715e9113355ac5a4781c1eaf0d4bea6fcdf4073068f8`  
		Last Modified: Tue, 05 Apr 2022 10:08:01 GMT  
		Size: 102.8 MB (102784652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c7dcfaac085766cdaa5fce90fb5c664130f22fa3f6005b3cebddf45a4e2b9b`  
		Last Modified: Tue, 05 Apr 2022 10:07:43 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7a86ae8bfd11a7525de064d7143eed347098156c965551db06b0da1fab2f67`  
		Last Modified: Wed, 06 Apr 2022 02:54:45 GMT  
		Size: 7.3 MB (7320952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0c1522f46b06b20e754f09fd417e5b522acf7b915a44a6cad6fe90bad02db9`  
		Last Modified: Wed, 06 Apr 2022 02:55:04 GMT  
		Size: 1.1 MB (1120844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaec64dc6b0c2892c44454f4ce84e9687ac350308af8c09e1b3aa2ce2765c42c`  
		Last Modified: Wed, 06 Apr 2022 02:55:03 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9ba130fc612fa21ac7394cde419c78e0fcfd0f666ab9505f7192d1524dd6c078
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118747452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bf60c3b8fb5c4231333c71e7f050d096e0b3de1f42003220a65f901d96b242`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:08:51 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 06:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:44:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:48:26 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 06:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 06:49:56 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 06:49:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:49:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 06:49:57 GMT
WORKDIR /go
# Tue, 05 Apr 2022 14:02:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 14:02:02 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 14:02:18 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Tue, 05 Apr 2022 14:02:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 14:02:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 14:02:19 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 14:02:19 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72593bb761a2ce336603e9e84973d1e284f39e0188e758ad8bc22c45cd9b6395`  
		Last Modified: Tue, 05 Apr 2022 06:09:13 GMT  
		Size: 272.3 KB (272267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf480933488ffcb2c9c9269292e2e3d643bea6eeb04cf948790ca50666a61c8`  
		Last Modified: Tue, 05 Apr 2022 06:53:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b3e51e0eff0c3e6118a6448425ada0b8e1725d738559d5b5e29ef58c570e8d`  
		Last Modified: Tue, 05 Apr 2022 06:54:30 GMT  
		Size: 107.7 MB (107739421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86765c73189fadce4ca276af5f7d9440213d5986a9687b648a51d45978e3a8c4`  
		Last Modified: Tue, 05 Apr 2022 06:54:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f50aeaf488b81d4c5d54c453b47637b6fbdfae9ca014728018463ce30aa78b`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 6.9 MB (6930892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ae06532c5b47a5e13d45f16dbda523abcb5fb38ed2ecacc6ac918a97c5df5f`  
		Last Modified: Tue, 05 Apr 2022 14:03:12 GMT  
		Size: 1.2 MB (1203783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ec0665f41221821b85ebd8d877934c36d3e93aed6228fcde2e3727228d99c2`  
		Last Modified: Tue, 05 Apr 2022 14:03:12 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-beta.1-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:1fe485f15ae043ddc06909eb0db4aa8908640744f4115d31550a8db0aaa727d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `caddy:2.5.0-beta.1-builder-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:0e7f812fa3e2ecc803dd4fb7b20a72dd1c75759ce49778f51ea9a5bd1719b22d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888394649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1badd557216606e841971ecc4296c63549a10a87cecd522cd7b7c2fa6c353d93`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 13:17:25 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Mar 2022 13:17:26 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Mar 2022 13:17:27 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Mar 2022 13:17:28 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Mar 2022 13:19:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:19:56 GMT
ENV GOPATH=C:\go
# Wed, 09 Mar 2022 13:20:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Mar 2022 13:35:10 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 09 Mar 2022 13:38:26 GMT
RUN $url = 'https://dl.google.com/go/go1.17.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '85ccf2608dca6ea9a46b6538c9e75e7cf2aebdf502379843b248e26b8bb110be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:38:28 GMT
WORKDIR C:\go
# Wed, 09 Mar 2022 18:27:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Mar 2022 23:14:28 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 23:20:35 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 23:20:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 23:21:34 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('fc6f2a7feb8f0936a0e04d3c9ea26d0404c2f4907eb436eb60e33152c22c1211f851c46606573fcb5c3334f8cc4f7f810b28b917a9f313f6454d1c5cd0f50f8a')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 10 Mar 2022 23:21:35 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7705bbffd7dc00934e935de0e00e09a7b0da55d66c596622f094495478dd71`  
		Last Modified: Wed, 09 Mar 2022 14:04:13 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be7ff0bb187d149a5cf3c76e1ec444d0e07c6606f67b2c921c67ec91829ea03`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876223f25b257577440a80fdee021b43c33ce3c56be9a20b2ddeaede95240522`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991eea244b9c3a1849c84748425dd9e9fbf9ec359ad9329796131b929239ffa4`  
		Last Modified: Wed, 09 Mar 2022 14:04:11 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b4c7c9740eb99bf626b312aa69396db3d186c5bd0e092b01c078ca7248e386`  
		Last Modified: Wed, 09 Mar 2022 14:04:40 GMT  
		Size: 25.5 MB (25454695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6c8a4d4848c21636a48a69a569a5372ec4890ea029f1f620dda76078bdcef`  
		Last Modified: Wed, 09 Mar 2022 14:04:09 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac6d527939082add6d21652ba4888acc5a6e7607365168d8e61fb1485339cb`  
		Last Modified: Wed, 09 Mar 2022 14:04:10 GMT  
		Size: 313.6 KB (313592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37aeceb8c2e5bb3c500129bcf20c3f8aea8c68c353e6714a63a225ed1546e8a1`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d88cd595dc7580d72420b7288c52d4b32201045a13dda1a7b943d9a3468adef`  
		Last Modified: Wed, 09 Mar 2022 14:13:05 GMT  
		Size: 145.5 MB (145488847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be492983ee2b2c9128ce0c732c441ae5fbd203cdb71c94faa253c24b01750c90`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa7b09ca61eb1fbafacee427b430b0879ad4da23e62e430a3fe6a66f181f642`  
		Last Modified: Wed, 09 Mar 2022 18:30:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74014ffde8e1a1677cd81e965bcd2b1f5287bcbf682bbce3bdd125052cd04f29`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281142ca6a15b21cfc34926357f799ac7c38783ca3875011b160c096c3229d65`  
		Last Modified: Thu, 10 Mar 2022 23:23:43 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc359b64dd95e97e38c7d61691e76c179b77cc013db0f1076e98fe6bb7be82bc`  
		Last Modified: Thu, 10 Mar 2022 23:23:43 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde3c36ea4dbe6709a5c743097ec10680741b0e35b0e9d41b2b703ed388f6cb4`  
		Last Modified: Thu, 10 Mar 2022 23:23:44 GMT  
		Size: 1.7 MB (1666531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389f0b289a5870da81d3b2ef7f3c7d5b1fb87e5f103073f2f7698ecafbef39a`  
		Last Modified: Thu, 10 Mar 2022 23:23:43 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-beta.1-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:500919c1c14c459428f3cb78c62243ea182dbd19bbf0f991c7d4074cf432fc3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.587; amd64

### `caddy:2.5.0-beta.1-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.587; amd64

```console
$ docker pull caddy@sha256:8a2e818f9a28bbd1dd99edd69a77b39ff9b5447b52226a98ab1aac9992f6ee29
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2395021082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a46232eca5f0ad5b7c29ac6bba9315f92b55caaf663cdf7404af3383e1549c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 13:12:32 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Mar 2022 13:12:34 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Mar 2022 13:12:35 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Mar 2022 13:12:36 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Mar 2022 13:13:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:13:33 GMT
ENV GOPATH=C:\go
# Wed, 09 Mar 2022 13:14:00 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Mar 2022 13:32:11 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 09 Mar 2022 13:34:51 GMT
RUN $url = 'https://dl.google.com/go/go1.17.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '85ccf2608dca6ea9a46b6538c9e75e7cf2aebdf502379843b248e26b8bb110be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:34:53 GMT
WORKDIR C:\go
# Thu, 10 Mar 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Mar 2022 23:21:49 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 23:21:50 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 23:21:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 23:22:16 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('fc6f2a7feb8f0936a0e04d3c9ea26d0404c2f4907eb436eb60e33152c22c1211f851c46606573fcb5c3334f8cc4f7f810b28b917a9f313f6454d1c5cd0f50f8a')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 10 Mar 2022 23:22:17 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f0159fc3ccac7854a42bd259b35d4a6482bc698865860892cf564a444b3c63`  
		Last Modified: Wed, 09 Mar 2022 14:03:12 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45aae60408220ac14736ec0b59de947d214ff276f074c4d716f9f2107b81671`  
		Last Modified: Wed, 09 Mar 2022 14:03:09 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eec0ac452237f9eaa33ce02c78ae43641960a5cd004be40f1e99f8eda401f78`  
		Last Modified: Wed, 09 Mar 2022 14:03:09 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b14ad7e0d74c6938398565f29103030d14231a39603cb3fef811fa8a55be4a`  
		Last Modified: Wed, 09 Mar 2022 14:03:09 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8065b93123915e69465b4ba5e604b150fa39c4157166451453950874ce4dedf`  
		Last Modified: Wed, 09 Mar 2022 14:03:16 GMT  
		Size: 25.7 MB (25684294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce2ababcffd2ebaadd4d6756c1408d978cbb56bfb5fac29069bf777e6eee0fd`  
		Last Modified: Wed, 09 Mar 2022 14:03:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cd0da17ace6307cacfc21df261451fc8967bbefa8bea2f39da28a647dc391d`  
		Last Modified: Wed, 09 Mar 2022 14:03:04 GMT  
		Size: 512.4 KB (512354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42222c033855a8bddbeb67a0b4cff5b2999afd4119720ee7e4fe9f6c59756404`  
		Last Modified: Wed, 09 Mar 2022 14:11:16 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73cbf8abb1840e446af856b56aac5dd2a832cfe370e17f2ee7b4cbea84ee32d`  
		Last Modified: Wed, 09 Mar 2022 14:12:03 GMT  
		Size: 145.7 MB (145695821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d3ebd62db6d310f5584c9e38da9d33e106ef41c0fbfc4fe4f99031b01cf183`  
		Last Modified: Wed, 09 Mar 2022 14:11:16 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af42907e59cd53434417a3cee16107b6fd3c9e583a7e92f403da1edc9c8881d5`  
		Last Modified: Thu, 10 Mar 2022 23:23:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2dba9ee51310a6df87f204c28a7052ce8cfe8fe4054efe85de312fd9ebd0d2a`  
		Last Modified: Thu, 10 Mar 2022 23:23:50 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90ed7f357bfb619820be785ff8397518d8b81f789fe33d1a458aa78a0b2c293`  
		Last Modified: Thu, 10 Mar 2022 23:23:50 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcaade4b90a730c916671b2dce519d031c74921051d042a36460fb347c4f0f43`  
		Last Modified: Thu, 10 Mar 2022 23:23:50 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fb19e6205c8bf8fb08f0d0c098c493b74d6a86d71667408aa1fe3f689c0d1f`  
		Last Modified: Thu, 10 Mar 2022 23:23:52 GMT  
		Size: 1.9 MB (1863109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cafb79352f1994a6c222b27e70e550375956842aa86e55ba656bcc19c61031`  
		Last Modified: Thu, 10 Mar 2022 23:23:50 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-beta.1-windowsservercore`

```console
$ docker pull caddy@sha256:2af9e1d7b943f0166cba6c938edd39f8dc7d04e21de4f1014ab341733e0be872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2686; amd64
	-	windows version 10.0.20348.587; amd64

### `caddy:2.5.0-beta.1-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:7773fd461ee6f12339ba1673bc5df75781a929c178c69f2b76f6dbb331c4b8a9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728732764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1eacf7022523cf02e6baa380b984f1849385cfe6d35462401e39349c8fae5c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 10 Mar 2022 23:15:55 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 23:17:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d3823cb9ec107805c996e0de561c460a8d865698362c6ba842a69503af693d8f7db8ac418abffc4b7110a273d0b8be50168f8a5bcc0dc4da1e81fd1a4271f9d2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 10 Mar 2022 23:17:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 10 Mar 2022 23:17:02 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 10 Mar 2022 23:17:03 GMT
VOLUME [c:/config]
# Thu, 10 Mar 2022 23:17:05 GMT
VOLUME [c:/data]
# Thu, 10 Mar 2022 23:17:06 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Thu, 10 Mar 2022 23:17:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 10 Mar 2022 23:17:11 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 10 Mar 2022 23:17:13 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 10 Mar 2022 23:17:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 10 Mar 2022 23:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 10 Mar 2022 23:17:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 10 Mar 2022 23:17:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 10 Mar 2022 23:17:24 GMT
EXPOSE 80
# Thu, 10 Mar 2022 23:17:26 GMT
EXPOSE 443
# Thu, 10 Mar 2022 23:17:28 GMT
EXPOSE 2019
# Thu, 10 Mar 2022 23:18:46 GMT
RUN caddy version
# Thu, 10 Mar 2022 23:18:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9d7e8231020fca55f52d14b8a7ce3656ea1a0f7add52d65e90f62121fe48b8`  
		Last Modified: Thu, 10 Mar 2022 23:23:16 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af80d92ff4032a4af7c432751719331889e3987e12e65d34d5ebb282a20c93e9`  
		Last Modified: Thu, 10 Mar 2022 23:23:20 GMT  
		Size: 12.6 MB (12581604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d3ae26f04e000ad3d59599134e362ac56f63587121dfd8c289ad4d7198b2c6`  
		Last Modified: Thu, 10 Mar 2022 23:23:16 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe189798f275d20c78e39c5899fde1e4eb39b5215c94602a02494919622fbd1`  
		Last Modified: Thu, 10 Mar 2022 23:23:15 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bb6704511f5e25c596bb4da2e3876a4ff94d636a5a864cdc2081fa0c8c90e8`  
		Last Modified: Thu, 10 Mar 2022 23:23:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60f4b9d1b8e2632e8c4b5a2ba5cef7b9d320a84cdc2f9b1602bf958c0eae59`  
		Last Modified: Thu, 10 Mar 2022 23:23:14 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad4d74ac905f41961ea9c19da27a83ecf1f9e61f9f11698d8f6640f1ee42463`  
		Last Modified: Thu, 10 Mar 2022 23:23:13 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c1b1b3adc2fba2aafe3fabc3589db5fee1a3e8804da41d5c86c57b9f715e34`  
		Last Modified: Thu, 10 Mar 2022 23:23:14 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920aeb6981196ccd526b2c147b65406c9e7ad753928b540d38b06ce826a10989`  
		Last Modified: Thu, 10 Mar 2022 23:23:13 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3c1945a551d9fd87cdad01e126234fc6c19447c16283c1b7f3a9aaeaa85b`  
		Last Modified: Thu, 10 Mar 2022 23:23:12 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20fc2235c71cef450cb31287142ec7b1653b8aa10e4df09251c2fee9e45e9bfb`  
		Last Modified: Thu, 10 Mar 2022 23:23:12 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1f868d3e6e3b7aeba72b31e537c64540b5cd47876b29dbc6b99449b042c77b`  
		Last Modified: Thu, 10 Mar 2022 23:23:11 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1709c223988941e572100de0e0416fd946212338a4b82d0bf6157a0a9cffb`  
		Last Modified: Thu, 10 Mar 2022 23:23:11 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31826e49182a6b827ba6af55bc08c92b46dcbd38b71dcfb68a76fa4b184624d`  
		Last Modified: Thu, 10 Mar 2022 23:23:11 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10bff2600becf937738dbbeabc119db87dc7bbf300de826c6f356cdf07824b4`  
		Last Modified: Thu, 10 Mar 2022 23:23:09 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39bd343b434eec8e57160a0b4c89e93ef67e08138859c36a8c46c14cbda37ca7`  
		Last Modified: Thu, 10 Mar 2022 23:23:09 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14b1140f1d1c8b21f9bcd3ceb8f5dea64077c8d7cc78b9b4d9ed5b2f490cecd`  
		Last Modified: Thu, 10 Mar 2022 23:23:09 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d5743206ba889ce28c20481d33002512a479d915ae0c5dfc5a8d01bbd943ed`  
		Last Modified: Thu, 10 Mar 2022 23:23:09 GMT  
		Size: 307.8 KB (307825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f83df86e60e5b4e53108b5e0b1bf84a1c3bba826dd3ac59b4f7a1ac79a59908`  
		Last Modified: Thu, 10 Mar 2022 23:23:09 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-windowsservercore` - windows version 10.0.20348.587; amd64

```console
$ docker pull caddy@sha256:190644b756f6e29fdd566242137d83a8ab8cb5da79c6eeb5a686acb280d0c87d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2234975577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec73698bb10b0a408086c4dd1fba649195a728ddf076a02f1e7367f9941183d0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Mar 2022 23:19:22 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 10 Mar 2022 23:19:23 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 23:19:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d3823cb9ec107805c996e0de561c460a8d865698362c6ba842a69503af693d8f7db8ac418abffc4b7110a273d0b8be50168f8a5bcc0dc4da1e81fd1a4271f9d2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 10 Mar 2022 23:19:49 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 10 Mar 2022 23:19:50 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 10 Mar 2022 23:19:51 GMT
VOLUME [c:/config]
# Thu, 10 Mar 2022 23:19:52 GMT
VOLUME [c:/data]
# Thu, 10 Mar 2022 23:19:52 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Thu, 10 Mar 2022 23:19:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 10 Mar 2022 23:19:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 10 Mar 2022 23:19:55 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 10 Mar 2022 23:19:56 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 10 Mar 2022 23:19:57 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 10 Mar 2022 23:19:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 10 Mar 2022 23:19:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 10 Mar 2022 23:20:00 GMT
EXPOSE 80
# Thu, 10 Mar 2022 23:20:01 GMT
EXPOSE 443
# Thu, 10 Mar 2022 23:20:02 GMT
EXPOSE 2019
# Thu, 10 Mar 2022 23:20:16 GMT
RUN caddy version
# Thu, 10 Mar 2022 23:20:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501204225ae4faaf2054af787801c79f59cd7e6764ba27480f88314d662fe8db`  
		Last Modified: Thu, 10 Mar 2022 23:23:35 GMT  
		Size: 618.1 KB (618083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1b161fdd7e1eff73e0b69b5a534a91cdc416dbc212d1d41e86ed77f1bbbb4b`  
		Last Modified: Thu, 10 Mar 2022 23:23:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec81d9b42cee80d858fed2642eb9fceb14a85637d3107bdd77360697068f968`  
		Last Modified: Thu, 10 Mar 2022 23:23:37 GMT  
		Size: 12.8 MB (12770708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf78f158dbd631347c47fa0b4b35ed7c16f4c617befa9f52fbae491a4a2085b`  
		Last Modified: Thu, 10 Mar 2022 23:23:32 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddd79c99dbc6f4dbaf32b5704dc85064b5abb0d388adf5d061eaab0e37b5afa`  
		Last Modified: Thu, 10 Mar 2022 23:23:33 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fdbdbcc0a58e8c38006e9b158adc19da95d85b019433828016eac93f2c03ba`  
		Last Modified: Thu, 10 Mar 2022 23:23:31 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba8cfc63470c708385e8d8796cfeea6c650b82d68526bd52d26418ba8ef3a33`  
		Last Modified: Thu, 10 Mar 2022 23:23:31 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc704f14d84f4cd4b9a956f79720b1fa2fed3455d75920ae21828dba48e0a15c`  
		Last Modified: Thu, 10 Mar 2022 23:23:31 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7390fcba4513a938ed30807fc0a4f3dc62ec98c0c3a81070185b3332cba558d`  
		Last Modified: Thu, 10 Mar 2022 23:23:30 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4a1b650b0b42f48eb9be5a49262e9d61983a217fa6b9cef5c1c4e8ea6037a1`  
		Last Modified: Thu, 10 Mar 2022 23:23:30 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9efc512998552b2c0eb4fd62b04c41138f65d14796d706304028d70fbc6b30`  
		Last Modified: Thu, 10 Mar 2022 23:23:29 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05756c324de05267a5034909e0c59ce72d9f72b09fab332779f98cd3801f0232`  
		Last Modified: Thu, 10 Mar 2022 23:23:28 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43f983684908d82bbab9bbc2f115c19a1f78b5048872a5e54f8d3d208e89fb6`  
		Last Modified: Thu, 10 Mar 2022 23:23:28 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3b450029ff204db60d8023c9e526c38205aec114ab62d67351b1f19004b330`  
		Last Modified: Thu, 10 Mar 2022 23:23:28 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18554b6031813cc80f8ba7e5e1df6f947821e1d1d0a6cab8e410f650209d86ae`  
		Last Modified: Thu, 10 Mar 2022 23:23:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bfbc8f27994a32c626bcad31c573c825f23474b2d2167338ee0d35de1e6099`  
		Last Modified: Thu, 10 Mar 2022 23:23:26 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9e9fb9ea227f0f6e8f513e977a1965a7de7aa0d22c26685a156828a8ebf06c`  
		Last Modified: Thu, 10 Mar 2022 23:23:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35636b68f6f3e0d03a7ba26fb4b136786e49e7a155fecbfd189ba95f4e6f42c`  
		Last Modified: Thu, 10 Mar 2022 23:23:26 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98050fbe661913690cee263b64e5c1defd894c209a4ac627acd69b806ba17e7a`  
		Last Modified: Thu, 10 Mar 2022 23:23:26 GMT  
		Size: 314.3 KB (314344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2dc85353d3e550445d387372cf10180870b8aa3bdf523148585e354588bfb4`  
		Last Modified: Thu, 10 Mar 2022 23:23:26 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-beta.1-windowsservercore-1809`

```console
$ docker pull caddy@sha256:cb16b8aea224ac5fcac35beb9514f818332a1b46c4a99005974b2da915619d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `caddy:2.5.0-beta.1-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:7773fd461ee6f12339ba1673bc5df75781a929c178c69f2b76f6dbb331c4b8a9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728732764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1eacf7022523cf02e6baa380b984f1849385cfe6d35462401e39349c8fae5c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 10 Mar 2022 23:15:55 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 23:17:00 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d3823cb9ec107805c996e0de561c460a8d865698362c6ba842a69503af693d8f7db8ac418abffc4b7110a273d0b8be50168f8a5bcc0dc4da1e81fd1a4271f9d2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 10 Mar 2022 23:17:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 10 Mar 2022 23:17:02 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 10 Mar 2022 23:17:03 GMT
VOLUME [c:/config]
# Thu, 10 Mar 2022 23:17:05 GMT
VOLUME [c:/data]
# Thu, 10 Mar 2022 23:17:06 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Thu, 10 Mar 2022 23:17:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 10 Mar 2022 23:17:11 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 10 Mar 2022 23:17:13 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 10 Mar 2022 23:17:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 10 Mar 2022 23:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 10 Mar 2022 23:17:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 10 Mar 2022 23:17:22 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 10 Mar 2022 23:17:24 GMT
EXPOSE 80
# Thu, 10 Mar 2022 23:17:26 GMT
EXPOSE 443
# Thu, 10 Mar 2022 23:17:28 GMT
EXPOSE 2019
# Thu, 10 Mar 2022 23:18:46 GMT
RUN caddy version
# Thu, 10 Mar 2022 23:18:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9d7e8231020fca55f52d14b8a7ce3656ea1a0f7add52d65e90f62121fe48b8`  
		Last Modified: Thu, 10 Mar 2022 23:23:16 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af80d92ff4032a4af7c432751719331889e3987e12e65d34d5ebb282a20c93e9`  
		Last Modified: Thu, 10 Mar 2022 23:23:20 GMT  
		Size: 12.6 MB (12581604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d3ae26f04e000ad3d59599134e362ac56f63587121dfd8c289ad4d7198b2c6`  
		Last Modified: Thu, 10 Mar 2022 23:23:16 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe189798f275d20c78e39c5899fde1e4eb39b5215c94602a02494919622fbd1`  
		Last Modified: Thu, 10 Mar 2022 23:23:15 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bb6704511f5e25c596bb4da2e3876a4ff94d636a5a864cdc2081fa0c8c90e8`  
		Last Modified: Thu, 10 Mar 2022 23:23:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60f4b9d1b8e2632e8c4b5a2ba5cef7b9d320a84cdc2f9b1602bf958c0eae59`  
		Last Modified: Thu, 10 Mar 2022 23:23:14 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad4d74ac905f41961ea9c19da27a83ecf1f9e61f9f11698d8f6640f1ee42463`  
		Last Modified: Thu, 10 Mar 2022 23:23:13 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c1b1b3adc2fba2aafe3fabc3589db5fee1a3e8804da41d5c86c57b9f715e34`  
		Last Modified: Thu, 10 Mar 2022 23:23:14 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920aeb6981196ccd526b2c147b65406c9e7ad753928b540d38b06ce826a10989`  
		Last Modified: Thu, 10 Mar 2022 23:23:13 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9c3c1945a551d9fd87cdad01e126234fc6c19447c16283c1b7f3a9aaeaa85b`  
		Last Modified: Thu, 10 Mar 2022 23:23:12 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20fc2235c71cef450cb31287142ec7b1653b8aa10e4df09251c2fee9e45e9bfb`  
		Last Modified: Thu, 10 Mar 2022 23:23:12 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1f868d3e6e3b7aeba72b31e537c64540b5cd47876b29dbc6b99449b042c77b`  
		Last Modified: Thu, 10 Mar 2022 23:23:11 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1709c223988941e572100de0e0416fd946212338a4b82d0bf6157a0a9cffb`  
		Last Modified: Thu, 10 Mar 2022 23:23:11 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31826e49182a6b827ba6af55bc08c92b46dcbd38b71dcfb68a76fa4b184624d`  
		Last Modified: Thu, 10 Mar 2022 23:23:11 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10bff2600becf937738dbbeabc119db87dc7bbf300de826c6f356cdf07824b4`  
		Last Modified: Thu, 10 Mar 2022 23:23:09 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39bd343b434eec8e57160a0b4c89e93ef67e08138859c36a8c46c14cbda37ca7`  
		Last Modified: Thu, 10 Mar 2022 23:23:09 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14b1140f1d1c8b21f9bcd3ceb8f5dea64077c8d7cc78b9b4d9ed5b2f490cecd`  
		Last Modified: Thu, 10 Mar 2022 23:23:09 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d5743206ba889ce28c20481d33002512a479d915ae0c5dfc5a8d01bbd943ed`  
		Last Modified: Thu, 10 Mar 2022 23:23:09 GMT  
		Size: 307.8 KB (307825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f83df86e60e5b4e53108b5e0b1bf84a1c3bba826dd3ac59b4f7a1ac79a59908`  
		Last Modified: Thu, 10 Mar 2022 23:23:09 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-beta.1-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:fa27c627b6079b5f944febb88fc9ff13eba0477d345ee00bc89682c6cd960c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.587; amd64

### `caddy:2.5.0-beta.1-windowsservercore-ltsc2022` - windows version 10.0.20348.587; amd64

```console
$ docker pull caddy@sha256:190644b756f6e29fdd566242137d83a8ab8cb5da79c6eeb5a686acb280d0c87d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2234975577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec73698bb10b0a408086c4dd1fba649195a728ddf076a02f1e7367f9941183d0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Mar 2022 23:19:22 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 10 Mar 2022 23:19:23 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 23:19:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d3823cb9ec107805c996e0de561c460a8d865698362c6ba842a69503af693d8f7db8ac418abffc4b7110a273d0b8be50168f8a5bcc0dc4da1e81fd1a4271f9d2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 10 Mar 2022 23:19:49 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 10 Mar 2022 23:19:50 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 10 Mar 2022 23:19:51 GMT
VOLUME [c:/config]
# Thu, 10 Mar 2022 23:19:52 GMT
VOLUME [c:/data]
# Thu, 10 Mar 2022 23:19:52 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Thu, 10 Mar 2022 23:19:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 10 Mar 2022 23:19:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 10 Mar 2022 23:19:55 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 10 Mar 2022 23:19:56 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 10 Mar 2022 23:19:57 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 10 Mar 2022 23:19:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 10 Mar 2022 23:19:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 10 Mar 2022 23:20:00 GMT
EXPOSE 80
# Thu, 10 Mar 2022 23:20:01 GMT
EXPOSE 443
# Thu, 10 Mar 2022 23:20:02 GMT
EXPOSE 2019
# Thu, 10 Mar 2022 23:20:16 GMT
RUN caddy version
# Thu, 10 Mar 2022 23:20:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501204225ae4faaf2054af787801c79f59cd7e6764ba27480f88314d662fe8db`  
		Last Modified: Thu, 10 Mar 2022 23:23:35 GMT  
		Size: 618.1 KB (618083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1b161fdd7e1eff73e0b69b5a534a91cdc416dbc212d1d41e86ed77f1bbbb4b`  
		Last Modified: Thu, 10 Mar 2022 23:23:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec81d9b42cee80d858fed2642eb9fceb14a85637d3107bdd77360697068f968`  
		Last Modified: Thu, 10 Mar 2022 23:23:37 GMT  
		Size: 12.8 MB (12770708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf78f158dbd631347c47fa0b4b35ed7c16f4c617befa9f52fbae491a4a2085b`  
		Last Modified: Thu, 10 Mar 2022 23:23:32 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddd79c99dbc6f4dbaf32b5704dc85064b5abb0d388adf5d061eaab0e37b5afa`  
		Last Modified: Thu, 10 Mar 2022 23:23:33 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fdbdbcc0a58e8c38006e9b158adc19da95d85b019433828016eac93f2c03ba`  
		Last Modified: Thu, 10 Mar 2022 23:23:31 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba8cfc63470c708385e8d8796cfeea6c650b82d68526bd52d26418ba8ef3a33`  
		Last Modified: Thu, 10 Mar 2022 23:23:31 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc704f14d84f4cd4b9a956f79720b1fa2fed3455d75920ae21828dba48e0a15c`  
		Last Modified: Thu, 10 Mar 2022 23:23:31 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7390fcba4513a938ed30807fc0a4f3dc62ec98c0c3a81070185b3332cba558d`  
		Last Modified: Thu, 10 Mar 2022 23:23:30 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4a1b650b0b42f48eb9be5a49262e9d61983a217fa6b9cef5c1c4e8ea6037a1`  
		Last Modified: Thu, 10 Mar 2022 23:23:30 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9efc512998552b2c0eb4fd62b04c41138f65d14796d706304028d70fbc6b30`  
		Last Modified: Thu, 10 Mar 2022 23:23:29 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05756c324de05267a5034909e0c59ce72d9f72b09fab332779f98cd3801f0232`  
		Last Modified: Thu, 10 Mar 2022 23:23:28 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43f983684908d82bbab9bbc2f115c19a1f78b5048872a5e54f8d3d208e89fb6`  
		Last Modified: Thu, 10 Mar 2022 23:23:28 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3b450029ff204db60d8023c9e526c38205aec114ab62d67351b1f19004b330`  
		Last Modified: Thu, 10 Mar 2022 23:23:28 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18554b6031813cc80f8ba7e5e1df6f947821e1d1d0a6cab8e410f650209d86ae`  
		Last Modified: Thu, 10 Mar 2022 23:23:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bfbc8f27994a32c626bcad31c573c825f23474b2d2167338ee0d35de1e6099`  
		Last Modified: Thu, 10 Mar 2022 23:23:26 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9e9fb9ea227f0f6e8f513e977a1965a7de7aa0d22c26685a156828a8ebf06c`  
		Last Modified: Thu, 10 Mar 2022 23:23:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35636b68f6f3e0d03a7ba26fb4b136786e49e7a155fecbfd189ba95f4e6f42c`  
		Last Modified: Thu, 10 Mar 2022 23:23:26 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98050fbe661913690cee263b64e5c1defd894c209a4ac627acd69b806ba17e7a`  
		Last Modified: Thu, 10 Mar 2022 23:23:26 GMT  
		Size: 314.3 KB (314344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2dc85353d3e550445d387372cf10180870b8aa3bdf523148585e354588bfb4`  
		Last Modified: Thu, 10 Mar 2022 23:23:26 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:alpine`

```console
$ docker pull caddy@sha256:15e576e7d00b1f41a648c5295a03677c24da5fede09131edcb1e6d809c7dc8aa
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
$ docker pull caddy@sha256:c8555e2ca66576a4404c2b5f31d843a5378dea6134acb500502901b563efebcf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14842034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ace180df3e668bd7937be4555305fdb7686c68acf2b5514665e2bac99bd266a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:24:48 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 04:24:50 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 04:24:50 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 04:24:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 04:24:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:24:52 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 04:24:52 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 04:24:52 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 04:24:53 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 80
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 443
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 04:24:54 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 04:24:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe024ea85c2d7fb47ce4f044038d4227cee2a982bca3e26a0ea4772b8b652f9a`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 291.2 KB (291230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438e4a77a6e9c40c3bf1fb392618ac596307733f97d294edb86383ce8ff7e51d`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6d2ebbfc8548ecc1dbf4c7568459e52549b81522cb450d42ada1bf82513a8d`  
		Last Modified: Tue, 05 Apr 2022 04:25:34 GMT  
		Size: 11.7 MB (11726452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c5f60dbd2d0286f964c9769a4a3396935a60d0d71ac0e3f8eea5c4c20711fb`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:01ed10f530dfa4af76fa0f13bcdde451a934fbd3a2d77e4cfa72dbc5587ac6f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14049473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c322930340bb73e0796df576638a0214eda5499c8f9b79e4f9af61aeb4da4d2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:14:11 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:14:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 03:14:14 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 03:14:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 03:14:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 03:14:20 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 03:14:21 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 03:14:21 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 03:14:22 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 03:14:22 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 03:14:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 03:14:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 03:14:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 03:14:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 03:14:26 GMT
EXPOSE 80
# Tue, 05 Apr 2022 03:14:26 GMT
EXPOSE 443
# Tue, 05 Apr 2022 03:14:27 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 03:14:27 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 03:14:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d650105deec735ac6dce2611f274a6cf2d9f60fc811167dd6d644e281a38f5`  
		Last Modified: Tue, 05 Apr 2022 03:17:39 GMT  
		Size: 291.7 KB (291653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f3d66a6432942b556bf7a077c220319708b7fc75279695b4b05fa25166fbaf`  
		Last Modified: Tue, 05 Apr 2022 03:17:38 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5d8162ee509e3528dd82e497c4057d40064d43d532acc589b4408c08d2b144`  
		Last Modified: Tue, 05 Apr 2022 03:17:46 GMT  
		Size: 11.1 MB (11125784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0ebc13031265ef07e50f9c7658d00ce8d28c00affdf202b6dd849558f06ad6`  
		Last Modified: Tue, 05 Apr 2022 03:17:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:80bf5252e7e8c04e9ff83dd861f7ee4e81bad7b2b52b5c78a43abf0c95818cf7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dddbbfbbc47ddc2ad3b96622c35ee55ec3eecd5e37cde28c3dfe807ac0827ba`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:52 GMT
ADD file:97f7b59ed0e40e7771daab294820763a7bb86c843317be55725baf1cab39aa12 in / 
# Mon, 04 Apr 2022 23:57:52 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:32:17 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:32:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 06:32:20 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 06:32:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 06:32:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:32:26 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 06:32:26 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 06:32:27 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 06:32:27 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 06:32:28 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 06:32:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 06:32:30 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 06:32:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 06:32:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 06:32:31 GMT
EXPOSE 80
# Tue, 05 Apr 2022 06:32:32 GMT
EXPOSE 443
# Tue, 05 Apr 2022 06:32:32 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 06:32:33 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 06:32:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:380010979fdd8a9a4b0bf397034a27ec6cabe61d36e9e6d460ea986f0ddaef38`  
		Last Modified: Mon, 04 Apr 2022 23:59:45 GMT  
		Size: 2.4 MB (2427969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0decd23e3d353b46346bc943e7c39f406496ebc5b14731e4575f770563ddef21`  
		Last Modified: Tue, 05 Apr 2022 06:34:41 GMT  
		Size: 290.6 KB (290637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf30d07056a9a35092dc8a190963a5d19c14fce0543c6f6cfed98fc9a687dc5f`  
		Last Modified: Tue, 05 Apr 2022 06:34:40 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbde61fe85af3ebca0218d5ca1f9b5b6d095a57aedc0d7a827ba511e2143629`  
		Last Modified: Tue, 05 Apr 2022 06:34:48 GMT  
		Size: 11.1 MB (11106715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9e55ef38253194b94160973edf2d58fbb2df74561e28d5e7894a3865f9daf8`  
		Last Modified: Tue, 05 Apr 2022 06:34:40 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:e526f540c45973c7a3a4585918890beceac9f0916e124daea3bf4e8b7a1e09b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13753199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2982d1a58becf38a1cf55541dcd74c1b096e8a02bb2060c30540fd3246e46e4f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:11:38 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:11:40 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 03:11:41 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 03:11:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 03:11:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 03:11:45 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 03:11:46 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 03:11:47 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 03:11:48 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 03:11:49 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 03:11:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 03:11:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 03:11:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 03:11:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 03:11:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 03:11:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 03:11:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 03:11:57 GMT
EXPOSE 80
# Tue, 05 Apr 2022 03:11:58 GMT
EXPOSE 443
# Tue, 05 Apr 2022 03:11:59 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 03:12:00 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 03:12:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b907f83114020e794129b34363890abf552785b8d964dbd3546272cc805702ce`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 291.3 KB (291281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988559859d9a4661992cbcefddba5b3d7a16de6c22547a962024f04767e6debf`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 5.7 KB (5748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7769260cde91250d6c68897788b078fea0a63b1254082d2923affeb859224a92`  
		Last Modified: Tue, 05 Apr 2022 03:13:22 GMT  
		Size: 10.7 MB (10738627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0143e63583cae9b0bc2b0048073b6c52476761cbeffa8e6aeca59d227ae0ee2`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:0f4502864c2fae9298130a48ec4ca4351af0787bee15fd4cb5307b7b83e87dd8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13416150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b308dba8382e868224f828f88958151f9c1af01332da44ca296967f8bf09d40b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:44 GMT
ADD file:0b9367758b91930d9d69fd3901262e3a696f7a9f6d9e209e35da83ea6e785837 in / 
# Tue, 05 Apr 2022 00:23:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:07:02 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 07:07:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 07:07:12 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 07:07:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 07:07:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:07:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 07:07:31 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 07:07:33 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 07:07:36 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 07:07:40 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 07:07:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 07:07:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 07:07:47 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 07:07:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 07:07:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 07:07:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 07:07:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 07:08:03 GMT
EXPOSE 80
# Tue, 05 Apr 2022 07:08:06 GMT
EXPOSE 443
# Tue, 05 Apr 2022 07:08:08 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 07:08:10 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 07:08:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ee5f6345565e7aeda814a5c097612cacb0a74186b1f01bf5199e1b812b5d3065`  
		Last Modified: Tue, 05 Apr 2022 00:25:06 GMT  
		Size: 2.8 MB (2814167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8affbe739a71e3875810f257750034ec7a6ee3f2f2c0094f3bcb3ed8a45520b`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 293.7 KB (293710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc927cb41936aaa5bfefa5dc4d654b7193fd568f619707120a5491c620906fc1`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8646c35213c358f518a4d76b75742b5930acec5d12cbd6c75d0a7e217698cee`  
		Last Modified: Tue, 05 Apr 2022 07:11:06 GMT  
		Size: 10.3 MB (10302288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346269e52424a62ec14d10c3e1db1aeb9cefe58f0bf6021855044138396bc074`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:4bdb0834a42c22fa543fe4497215113db9aa55197d55597fb16c6cfd2a7ec22a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14225578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0631ff02e5e01fcee0ebd5387c53f8dca8198463556fd98f569e3454b0bab`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:47 GMT
ADD file:0f70e0f0075bee67acb44e5ef01bf6b9df1f69a25b7aa6fd15bd5bb6ec5bcc9f in / 
# Mon, 04 Apr 2022 23:41:48 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:19:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:19:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 06:19:20 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 06:19:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 06:19:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:19:22 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 06:19:23 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 06:19:23 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 06:19:23 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 80
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 443
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 06:19:25 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 06:19:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6f6a6c77b1bd5dfb3e759efaa292f964f197ae4b96be74d80ef059f87317997a`  
		Last Modified: Mon, 04 Apr 2022 23:42:47 GMT  
		Size: 2.6 MB (2604075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46276fc79092fffc5c0d503ca8733315c8e4002c4e7da79b2383f14c70565746`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 291.8 KB (291788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2e4510a7572a45fad3f051c23678f720057b3bb38d17381f62903aa621c6eb`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf64cfe3d9d0d01f6a1856e4850cd31a634fbb44641472deac6358fdc04352ea`  
		Last Modified: Tue, 05 Apr 2022 06:20:34 GMT  
		Size: 11.3 MB (11323733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363873546085e9612ff25fa067fed8e0038220696a865e645e8046a79035fc99`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:7330e2d325fa6b9d0f64526b31373722f60520a8e29131ef0c48537273d15a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2686; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:80234a9cd66af5a747785958e8dc683a43dfe946b9b98c9ffe2806fa4ac5422e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121342541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa54d86d06fba28c500cfe838c151623b997c5e35b2af29ea8b70b6a92a7fb8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:32:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 05:32:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 05:32:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:37:30 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 05:39:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 05:39:29 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 05:39:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:39:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 05:39:30 GMT
WORKDIR /go
# Tue, 05 Apr 2022 15:45:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 15:45:54 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 15:45:54 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 15:45:54 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 15:45:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 15:45:55 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 15:45:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc419b0ee22d1bb5f3b95a57b2edc733b7b585277f8101db7b2c9b53605c1b`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 272.0 KB (271965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc292e5bacdd8b97a1632a82d0fd0ee6c2692409bd4b35cb9e7e652efbc7c8`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dea7a3ad9148616176ac7fd686181a6e3c4eaac3746166e678a11017e4d32d9`  
		Last Modified: Tue, 05 Apr 2022 05:43:55 GMT  
		Size: 110.2 MB (110188123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35228ee6d672a4ef2501b746851ae8dc63cdc2612057a726a7affcd9d7d9f08`  
		Last Modified: Tue, 05 Apr 2022 05:43:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431098d05c7f64b1b215f6e58d58584efa1b85c22de1e46eabdf9f41c9a31550`  
		Last Modified: Tue, 05 Apr 2022 15:46:24 GMT  
		Size: 6.8 MB (6821467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16611ed52579f2526e4c8ef7d32963cc52bdf84706c195aaea01082575369d8d`  
		Last Modified: Tue, 05 Apr 2022 15:46:23 GMT  
		Size: 1.2 MB (1245713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56bc9474ab53335737725ec3c82362fd8d085309b54710629fec01fac471c3d`  
		Last Modified: Tue, 05 Apr 2022 15:46:22 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:dcf5e840b541953183c28551fb8ad10bcb3a75ad0eb6010cf518751eb246cdb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115819309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b820bb6f118cf0da95b1daa66e903131e906c6f7937eeb823bea92880a827ed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:39:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 11:59:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 11:59:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 12:07:43 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 12:10:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 12:10:56 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 12:10:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 12:10:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 12:10:58 GMT
WORKDIR /go
# Tue, 05 Apr 2022 18:47:17 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 18:47:18 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 18:47:18 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 18:47:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 18:47:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 18:47:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 18:47:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560305eea4784da98378676b22f9871093d6a4d7eb88292accc17f0cfd6b12ea`  
		Last Modified: Tue, 05 Apr 2022 11:40:22 GMT  
		Size: 272.1 KB (272138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145a805e932abbcca6b77ad458c7ac26275ff4f23af9912d2c4d3dac9eef4cf8`  
		Last Modified: Tue, 05 Apr 2022 12:15:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc18cdc5d172f77e8e9ab98b63b490a7ee5597737555f86ab3df9580d7603038`  
		Last Modified: Tue, 05 Apr 2022 12:20:29 GMT  
		Size: 105.1 MB (105068577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a00aaf29b7cc08e00fa3ad26938794099e739101e45a4efbd80da84b4b59e8`  
		Last Modified: Tue, 05 Apr 2022 12:19:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce9447fafc122cfcae03e938e9b3bf3750eda3436a83625bc1229d67e6f3526`  
		Last Modified: Tue, 05 Apr 2022 18:49:07 GMT  
		Size: 6.7 MB (6677398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb4981b5917a068228e1b12e5afe118826c4ebb0880a39e0de01773e1a9b6b`  
		Last Modified: Tue, 05 Apr 2022 18:49:04 GMT  
		Size: 1.2 MB (1178510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50ceda04f269611e045f72b6f59cd9458e489675973c2a26d9ba4c92417c110`  
		Last Modified: Tue, 05 Apr 2022 18:49:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:f067c336bf9a0f6755735e5dbd07fdbce24f00d4ded39ae414599dd0707f5909
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114678400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e18d0d8561f2864f5ae2184d369b7ed78f855c8098e12b18e3e66e9ed1d702`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:19:56 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:19:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:19:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:28:26 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 09:31:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 09:31:38 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 09:31:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:31:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 09:31:40 GMT
WORKDIR /go
# Wed, 06 Apr 2022 02:23:29 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 06 Apr 2022 02:23:29 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 06 Apr 2022 02:23:30 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 06 Apr 2022 02:23:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Apr 2022 02:23:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 06 Apr 2022 02:23:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 06 Apr 2022 02:23:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f68dacdb1dfe1ed299ab3e43e478a27f0977380bbefc4c7ca5723758dbac6`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 271.1 KB (271116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431ad618c287090e481554b57afdc0383f065b5bbfc0ccdcefc6518e1a8331e`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1c19e6ea71a7140e1f92aaf1ca20998b7875298f5f0aecdad1849acea539e9`  
		Last Modified: Tue, 05 Apr 2022 09:43:01 GMT  
		Size: 104.9 MB (104853355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d18ca61f70738e42fc01d4076606b8ef68be3c58058c1922e2b44987e87a15`  
		Last Modified: Tue, 05 Apr 2022 09:41:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d951a4c4c0e205bd2d3656382822e0ad97c4ee98c7cc185614d9363d5b7b18df`  
		Last Modified: Wed, 06 Apr 2022 02:25:20 GMT  
		Size: 6.0 MB (5952176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b38ba848bdb94dd4baa0c3e1ed84c6c0f039346dbd2904d5e257b874558a07`  
		Last Modified: Wed, 06 Apr 2022 02:25:18 GMT  
		Size: 1.2 MB (1176713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426c201900d8690c727d61a628a8540811cafc07c1ed656aeb066b7745707c7b`  
		Last Modified: Wed, 06 Apr 2022 02:25:18 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:7b6beab6198241afad1f6660a5083478efd4f1e92ff2edccc566bca27905c310
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115488051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ee73e0e2ed794915b2af927e5458f4bad17835e41f615dab40db89f343bdf0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:38:07 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 07:38:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:38:08 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:41:43 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 07:43:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 07:43:02 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 07:43:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 07:43:05 GMT
WORKDIR /go
# Tue, 05 Apr 2022 17:39:06 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 17:39:07 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 17:39:08 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 17:39:09 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 17:39:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 17:39:13 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 17:39:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7637d0a7b497b253b73e807a5e676ba3f0750afafa9e1a4c61260513feb321f`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 271.8 KB (271764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda57b85efde0ed435315f4f74625e7a055107aa29e8c91a313ca6d525fb709c`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d20097de21a08b3879d9d8acda7ea55af524f6cb8cf3d8526c7ad583992e7f`  
		Last Modified: Tue, 05 Apr 2022 07:47:32 GMT  
		Size: 104.4 MB (104424495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662c5a329cf0f527093cef90725754463b5ab87a23be5a91edff92a844e76c37`  
		Last Modified: Tue, 05 Apr 2022 07:47:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f1e21bd0bbbfa99416af4431f653df5121e14b29364c870d86362268419104`  
		Last Modified: Tue, 05 Apr 2022 17:40:06 GMT  
		Size: 6.9 MB (6925952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e5c2ce8d4fcaae75fbb7497ef4b24c4b192aafbb3384f7a8221b0c1213401`  
		Last Modified: Tue, 05 Apr 2022 17:40:05 GMT  
		Size: 1.1 MB (1148677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4162b5640fb2e218682c6e2bfb93a2f2ad6c9ffbe57ecec50ca91554eefefa`  
		Last Modified: Tue, 05 Apr 2022 17:40:05 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:f0523e893e89caa4a62fb934156846b72fa1e93191eb22fe3e2648b4416da80e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114312516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066aed791277682729d033b831d7ce9039dba3849abd6e0cf881b8992fd75b70`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:50:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:50:19 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:50:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:57:52 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 10:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 10:00:43 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 10:00:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 10:00:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 10:00:55 GMT
WORKDIR /go
# Wed, 06 Apr 2022 02:52:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 06 Apr 2022 02:53:02 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 06 Apr 2022 02:53:05 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 06 Apr 2022 02:53:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Apr 2022 02:53:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 06 Apr 2022 02:53:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 06 Apr 2022 02:53:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcdc2e904e95f788aa4c66c5ce746890d6a02abca4c94711443f5c688b61ebf`  
		Last Modified: Tue, 05 Apr 2022 10:06:11 GMT  
		Size: 274.2 KB (274171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04802687d9aa11413122df45eb15c7d7f85937270997b441d1c6a09001730453`  
		Last Modified: Tue, 05 Apr 2022 10:06:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce62b250e0aee7f0aec0715e9113355ac5a4781c1eaf0d4bea6fcdf4073068f8`  
		Last Modified: Tue, 05 Apr 2022 10:08:01 GMT  
		Size: 102.8 MB (102784652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c7dcfaac085766cdaa5fce90fb5c664130f22fa3f6005b3cebddf45a4e2b9b`  
		Last Modified: Tue, 05 Apr 2022 10:07:43 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7a86ae8bfd11a7525de064d7143eed347098156c965551db06b0da1fab2f67`  
		Last Modified: Wed, 06 Apr 2022 02:54:45 GMT  
		Size: 7.3 MB (7320952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33cc607466c85109d67b2a8aefc6a137b9aebe631f8e33435b2618033bb3737`  
		Last Modified: Wed, 06 Apr 2022 02:54:45 GMT  
		Size: 1.1 MB (1120840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3107bf51b5f81e988fc6b01377bdab7efc085a95bfa0b866d40cd7c18bb23a6d`  
		Last Modified: Wed, 06 Apr 2022 02:54:44 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:7862e378800416206aa5844ed260f8cb64c1537299e481e5004521024727c011
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118747451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d95993f92df472d91942633064b5db1e229654fbf9e15e574f235f732d2171`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:08:51 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 06:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:44:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:48:26 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 06:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 06:49:56 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 06:49:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:49:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 06:49:57 GMT
WORKDIR /go
# Tue, 05 Apr 2022 14:02:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 14:02:02 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 14:02:02 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 14:02:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 14:02:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 14:02:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 14:02:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72593bb761a2ce336603e9e84973d1e284f39e0188e758ad8bc22c45cd9b6395`  
		Last Modified: Tue, 05 Apr 2022 06:09:13 GMT  
		Size: 272.3 KB (272267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf480933488ffcb2c9c9269292e2e3d643bea6eeb04cf948790ca50666a61c8`  
		Last Modified: Tue, 05 Apr 2022 06:53:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b3e51e0eff0c3e6118a6448425ada0b8e1725d738559d5b5e29ef58c570e8d`  
		Last Modified: Tue, 05 Apr 2022 06:54:30 GMT  
		Size: 107.7 MB (107739421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86765c73189fadce4ca276af5f7d9440213d5986a9687b648a51d45978e3a8c4`  
		Last Modified: Tue, 05 Apr 2022 06:54:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f50aeaf488b81d4c5d54c453b47637b6fbdfae9ca014728018463ce30aa78b`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 6.9 MB (6930892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca74c757745c5b39f811e1b5ed2a0fe0b8f2de2ab52b23dd01d8aaa71540d27b`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 1.2 MB (1203782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e4f898506aece97cc68bfd9e1a347bd072242e4672eee262eae303b3e0b6e9`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:568847e6f37af8e2f55d5d780b100e1dbfcbb9178896eb9d8f2b57ecf966d39c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888394051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20261b1174a82d98f801248da692dc2862f133c7cea9e52758b2c17b3567abc3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 13:17:25 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Mar 2022 13:17:26 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Mar 2022 13:17:27 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Mar 2022 13:17:28 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Mar 2022 13:19:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:19:56 GMT
ENV GOPATH=C:\go
# Wed, 09 Mar 2022 13:20:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Mar 2022 13:35:10 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 09 Mar 2022 13:38:26 GMT
RUN $url = 'https://dl.google.com/go/go1.17.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '85ccf2608dca6ea9a46b6538c9e75e7cf2aebdf502379843b248e26b8bb110be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:38:28 GMT
WORKDIR C:\go
# Wed, 09 Mar 2022 18:27:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Mar 2022 23:14:28 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 23:14:29 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 23:14:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 23:15:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('fc6f2a7feb8f0936a0e04d3c9ea26d0404c2f4907eb436eb60e33152c22c1211f851c46606573fcb5c3334f8cc4f7f810b28b917a9f313f6454d1c5cd0f50f8a')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 10 Mar 2022 23:15:41 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7705bbffd7dc00934e935de0e00e09a7b0da55d66c596622f094495478dd71`  
		Last Modified: Wed, 09 Mar 2022 14:04:13 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be7ff0bb187d149a5cf3c76e1ec444d0e07c6606f67b2c921c67ec91829ea03`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876223f25b257577440a80fdee021b43c33ce3c56be9a20b2ddeaede95240522`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991eea244b9c3a1849c84748425dd9e9fbf9ec359ad9329796131b929239ffa4`  
		Last Modified: Wed, 09 Mar 2022 14:04:11 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b4c7c9740eb99bf626b312aa69396db3d186c5bd0e092b01c078ca7248e386`  
		Last Modified: Wed, 09 Mar 2022 14:04:40 GMT  
		Size: 25.5 MB (25454695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6c8a4d4848c21636a48a69a569a5372ec4890ea029f1f620dda76078bdcef`  
		Last Modified: Wed, 09 Mar 2022 14:04:09 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac6d527939082add6d21652ba4888acc5a6e7607365168d8e61fb1485339cb`  
		Last Modified: Wed, 09 Mar 2022 14:04:10 GMT  
		Size: 313.6 KB (313592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37aeceb8c2e5bb3c500129bcf20c3f8aea8c68c353e6714a63a225ed1546e8a1`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d88cd595dc7580d72420b7288c52d4b32201045a13dda1a7b943d9a3468adef`  
		Last Modified: Wed, 09 Mar 2022 14:13:05 GMT  
		Size: 145.5 MB (145488847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be492983ee2b2c9128ce0c732c441ae5fbd203cdb71c94faa253c24b01750c90`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa7b09ca61eb1fbafacee427b430b0879ad4da23e62e430a3fe6a66f181f642`  
		Last Modified: Wed, 09 Mar 2022 18:30:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74014ffde8e1a1677cd81e965bcd2b1f5287bcbf682bbce3bdd125052cd04f29`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43e7b3a6c47e8c9bba8e4ba91d722cd9e491f2df12d5e277356e2b8fc070ba8`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceffc29f93380b6942a245303d5af87875d60351e4c897405f358f018b61b863`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae9e05c08471d9a54c2b46c4f892226ab1eab63b6efd326c44b50bceffb11f2`  
		Last Modified: Thu, 10 Mar 2022 23:22:56 GMT  
		Size: 1.7 MB (1665933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd386d40eef8a252639d03e1486ff30ff8f77cef626bf0592cc7853eb633c7d`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:54e2deab0aa5245b222cba916d21cb85acb53793dbb1651e3c7a6e7eb6240089
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
$ docker pull caddy@sha256:80234a9cd66af5a747785958e8dc683a43dfe946b9b98c9ffe2806fa4ac5422e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121342541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa54d86d06fba28c500cfe838c151623b997c5e35b2af29ea8b70b6a92a7fb8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:32:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 05:32:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 05:32:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:37:30 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 05:39:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 05:39:29 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 05:39:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:39:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 05:39:30 GMT
WORKDIR /go
# Tue, 05 Apr 2022 15:45:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 15:45:54 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 15:45:54 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 15:45:54 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 15:45:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 15:45:55 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 15:45:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc419b0ee22d1bb5f3b95a57b2edc733b7b585277f8101db7b2c9b53605c1b`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 272.0 KB (271965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc292e5bacdd8b97a1632a82d0fd0ee6c2692409bd4b35cb9e7e652efbc7c8`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dea7a3ad9148616176ac7fd686181a6e3c4eaac3746166e678a11017e4d32d9`  
		Last Modified: Tue, 05 Apr 2022 05:43:55 GMT  
		Size: 110.2 MB (110188123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35228ee6d672a4ef2501b746851ae8dc63cdc2612057a726a7affcd9d7d9f08`  
		Last Modified: Tue, 05 Apr 2022 05:43:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431098d05c7f64b1b215f6e58d58584efa1b85c22de1e46eabdf9f41c9a31550`  
		Last Modified: Tue, 05 Apr 2022 15:46:24 GMT  
		Size: 6.8 MB (6821467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16611ed52579f2526e4c8ef7d32963cc52bdf84706c195aaea01082575369d8d`  
		Last Modified: Tue, 05 Apr 2022 15:46:23 GMT  
		Size: 1.2 MB (1245713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56bc9474ab53335737725ec3c82362fd8d085309b54710629fec01fac471c3d`  
		Last Modified: Tue, 05 Apr 2022 15:46:22 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:dcf5e840b541953183c28551fb8ad10bcb3a75ad0eb6010cf518751eb246cdb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115819309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b820bb6f118cf0da95b1daa66e903131e906c6f7937eeb823bea92880a827ed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:39:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 11:59:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 11:59:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 12:07:43 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 12:10:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 12:10:56 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 12:10:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 12:10:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 12:10:58 GMT
WORKDIR /go
# Tue, 05 Apr 2022 18:47:17 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 18:47:18 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 18:47:18 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 18:47:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 18:47:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 18:47:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 18:47:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560305eea4784da98378676b22f9871093d6a4d7eb88292accc17f0cfd6b12ea`  
		Last Modified: Tue, 05 Apr 2022 11:40:22 GMT  
		Size: 272.1 KB (272138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145a805e932abbcca6b77ad458c7ac26275ff4f23af9912d2c4d3dac9eef4cf8`  
		Last Modified: Tue, 05 Apr 2022 12:15:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc18cdc5d172f77e8e9ab98b63b490a7ee5597737555f86ab3df9580d7603038`  
		Last Modified: Tue, 05 Apr 2022 12:20:29 GMT  
		Size: 105.1 MB (105068577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a00aaf29b7cc08e00fa3ad26938794099e739101e45a4efbd80da84b4b59e8`  
		Last Modified: Tue, 05 Apr 2022 12:19:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce9447fafc122cfcae03e938e9b3bf3750eda3436a83625bc1229d67e6f3526`  
		Last Modified: Tue, 05 Apr 2022 18:49:07 GMT  
		Size: 6.7 MB (6677398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cb4981b5917a068228e1b12e5afe118826c4ebb0880a39e0de01773e1a9b6b`  
		Last Modified: Tue, 05 Apr 2022 18:49:04 GMT  
		Size: 1.2 MB (1178510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50ceda04f269611e045f72b6f59cd9458e489675973c2a26d9ba4c92417c110`  
		Last Modified: Tue, 05 Apr 2022 18:49:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:f067c336bf9a0f6755735e5dbd07fdbce24f00d4ded39ae414599dd0707f5909
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114678400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e18d0d8561f2864f5ae2184d369b7ed78f855c8098e12b18e3e66e9ed1d702`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:19:56 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:19:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:19:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:28:26 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 09:31:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 09:31:38 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 09:31:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:31:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 09:31:40 GMT
WORKDIR /go
# Wed, 06 Apr 2022 02:23:29 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 06 Apr 2022 02:23:29 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 06 Apr 2022 02:23:30 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 06 Apr 2022 02:23:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Apr 2022 02:23:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 06 Apr 2022 02:23:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 06 Apr 2022 02:23:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f68dacdb1dfe1ed299ab3e43e478a27f0977380bbefc4c7ca5723758dbac6`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 271.1 KB (271116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5431ad618c287090e481554b57afdc0383f065b5bbfc0ccdcefc6518e1a8331e`  
		Last Modified: Tue, 05 Apr 2022 09:38:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1c19e6ea71a7140e1f92aaf1ca20998b7875298f5f0aecdad1849acea539e9`  
		Last Modified: Tue, 05 Apr 2022 09:43:01 GMT  
		Size: 104.9 MB (104853355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d18ca61f70738e42fc01d4076606b8ef68be3c58058c1922e2b44987e87a15`  
		Last Modified: Tue, 05 Apr 2022 09:41:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d951a4c4c0e205bd2d3656382822e0ad97c4ee98c7cc185614d9363d5b7b18df`  
		Last Modified: Wed, 06 Apr 2022 02:25:20 GMT  
		Size: 6.0 MB (5952176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b38ba848bdb94dd4baa0c3e1ed84c6c0f039346dbd2904d5e257b874558a07`  
		Last Modified: Wed, 06 Apr 2022 02:25:18 GMT  
		Size: 1.2 MB (1176713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426c201900d8690c727d61a628a8540811cafc07c1ed656aeb066b7745707c7b`  
		Last Modified: Wed, 06 Apr 2022 02:25:18 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:7b6beab6198241afad1f6660a5083478efd4f1e92ff2edccc566bca27905c310
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115488051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ee73e0e2ed794915b2af927e5458f4bad17835e41f615dab40db89f343bdf0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:38:07 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 07:38:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:38:08 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:41:43 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 07:43:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 07:43:02 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 07:43:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 07:43:05 GMT
WORKDIR /go
# Tue, 05 Apr 2022 17:39:06 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 17:39:07 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 17:39:08 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 17:39:09 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 17:39:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 17:39:13 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 17:39:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7637d0a7b497b253b73e807a5e676ba3f0750afafa9e1a4c61260513feb321f`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 271.8 KB (271764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda57b85efde0ed435315f4f74625e7a055107aa29e8c91a313ca6d525fb709c`  
		Last Modified: Tue, 05 Apr 2022 07:45:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d20097de21a08b3879d9d8acda7ea55af524f6cb8cf3d8526c7ad583992e7f`  
		Last Modified: Tue, 05 Apr 2022 07:47:32 GMT  
		Size: 104.4 MB (104424495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662c5a329cf0f527093cef90725754463b5ab87a23be5a91edff92a844e76c37`  
		Last Modified: Tue, 05 Apr 2022 07:47:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f1e21bd0bbbfa99416af4431f653df5121e14b29364c870d86362268419104`  
		Last Modified: Tue, 05 Apr 2022 17:40:06 GMT  
		Size: 6.9 MB (6925952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e5c2ce8d4fcaae75fbb7497ef4b24c4b192aafbb3384f7a8221b0c1213401`  
		Last Modified: Tue, 05 Apr 2022 17:40:05 GMT  
		Size: 1.1 MB (1148677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4162b5640fb2e218682c6e2bfb93a2f2ad6c9ffbe57ecec50ca91554eefefa`  
		Last Modified: Tue, 05 Apr 2022 17:40:05 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:f0523e893e89caa4a62fb934156846b72fa1e93191eb22fe3e2648b4416da80e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114312516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066aed791277682729d033b831d7ce9039dba3849abd6e0cf881b8992fd75b70`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:50:13 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 09:50:19 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 09:50:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 09:57:52 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 10:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 10:00:43 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 10:00:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 10:00:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 10:00:55 GMT
WORKDIR /go
# Wed, 06 Apr 2022 02:52:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 06 Apr 2022 02:53:02 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 06 Apr 2022 02:53:05 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 06 Apr 2022 02:53:08 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 06 Apr 2022 02:53:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 06 Apr 2022 02:53:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 06 Apr 2022 02:53:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcdc2e904e95f788aa4c66c5ce746890d6a02abca4c94711443f5c688b61ebf`  
		Last Modified: Tue, 05 Apr 2022 10:06:11 GMT  
		Size: 274.2 KB (274171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04802687d9aa11413122df45eb15c7d7f85937270997b441d1c6a09001730453`  
		Last Modified: Tue, 05 Apr 2022 10:06:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce62b250e0aee7f0aec0715e9113355ac5a4781c1eaf0d4bea6fcdf4073068f8`  
		Last Modified: Tue, 05 Apr 2022 10:08:01 GMT  
		Size: 102.8 MB (102784652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c7dcfaac085766cdaa5fce90fb5c664130f22fa3f6005b3cebddf45a4e2b9b`  
		Last Modified: Tue, 05 Apr 2022 10:07:43 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7a86ae8bfd11a7525de064d7143eed347098156c965551db06b0da1fab2f67`  
		Last Modified: Wed, 06 Apr 2022 02:54:45 GMT  
		Size: 7.3 MB (7320952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33cc607466c85109d67b2a8aefc6a137b9aebe631f8e33435b2618033bb3737`  
		Last Modified: Wed, 06 Apr 2022 02:54:45 GMT  
		Size: 1.1 MB (1120840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3107bf51b5f81e988fc6b01377bdab7efc085a95bfa0b866d40cd7c18bb23a6d`  
		Last Modified: Wed, 06 Apr 2022 02:54:44 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:7862e378800416206aa5844ed260f8cb64c1537299e481e5004521024727c011
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118747451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d95993f92df472d91942633064b5db1e229654fbf9e15e574f235f732d2171`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:08:51 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 06:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:44:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:48:26 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 06:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 06:49:56 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 06:49:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:49:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 06:49:57 GMT
WORKDIR /go
# Tue, 05 Apr 2022 14:02:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 14:02:02 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 14:02:02 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 14:02:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 14:02:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 14:02:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 14:02:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72593bb761a2ce336603e9e84973d1e284f39e0188e758ad8bc22c45cd9b6395`  
		Last Modified: Tue, 05 Apr 2022 06:09:13 GMT  
		Size: 272.3 KB (272267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf480933488ffcb2c9c9269292e2e3d643bea6eeb04cf948790ca50666a61c8`  
		Last Modified: Tue, 05 Apr 2022 06:53:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b3e51e0eff0c3e6118a6448425ada0b8e1725d738559d5b5e29ef58c570e8d`  
		Last Modified: Tue, 05 Apr 2022 06:54:30 GMT  
		Size: 107.7 MB (107739421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86765c73189fadce4ca276af5f7d9440213d5986a9687b648a51d45978e3a8c4`  
		Last Modified: Tue, 05 Apr 2022 06:54:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f50aeaf488b81d4c5d54c453b47637b6fbdfae9ca014728018463ce30aa78b`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 6.9 MB (6930892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca74c757745c5b39f811e1b5ed2a0fe0b8f2de2ab52b23dd01d8aaa71540d27b`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 1.2 MB (1203782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e4f898506aece97cc68bfd9e1a347bd072242e4672eee262eae303b3e0b6e9`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:276530503290de9ae8be7471e975d5db1e0d286e99d48317b675cec03c7c2fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:568847e6f37af8e2f55d5d780b100e1dbfcbb9178896eb9d8f2b57ecf966d39c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888394051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20261b1174a82d98f801248da692dc2862f133c7cea9e52758b2c17b3567abc3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 13:17:25 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Mar 2022 13:17:26 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Mar 2022 13:17:27 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Mar 2022 13:17:28 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Mar 2022 13:19:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:19:56 GMT
ENV GOPATH=C:\go
# Wed, 09 Mar 2022 13:20:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Mar 2022 13:35:10 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 09 Mar 2022 13:38:26 GMT
RUN $url = 'https://dl.google.com/go/go1.17.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '85ccf2608dca6ea9a46b6538c9e75e7cf2aebdf502379843b248e26b8bb110be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:38:28 GMT
WORKDIR C:\go
# Wed, 09 Mar 2022 18:27:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Mar 2022 23:14:28 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 23:14:29 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 23:14:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 23:15:39 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('fc6f2a7feb8f0936a0e04d3c9ea26d0404c2f4907eb436eb60e33152c22c1211f851c46606573fcb5c3334f8cc4f7f810b28b917a9f313f6454d1c5cd0f50f8a')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 10 Mar 2022 23:15:41 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7705bbffd7dc00934e935de0e00e09a7b0da55d66c596622f094495478dd71`  
		Last Modified: Wed, 09 Mar 2022 14:04:13 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be7ff0bb187d149a5cf3c76e1ec444d0e07c6606f67b2c921c67ec91829ea03`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876223f25b257577440a80fdee021b43c33ce3c56be9a20b2ddeaede95240522`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991eea244b9c3a1849c84748425dd9e9fbf9ec359ad9329796131b929239ffa4`  
		Last Modified: Wed, 09 Mar 2022 14:04:11 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b4c7c9740eb99bf626b312aa69396db3d186c5bd0e092b01c078ca7248e386`  
		Last Modified: Wed, 09 Mar 2022 14:04:40 GMT  
		Size: 25.5 MB (25454695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6c8a4d4848c21636a48a69a569a5372ec4890ea029f1f620dda76078bdcef`  
		Last Modified: Wed, 09 Mar 2022 14:04:09 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac6d527939082add6d21652ba4888acc5a6e7607365168d8e61fb1485339cb`  
		Last Modified: Wed, 09 Mar 2022 14:04:10 GMT  
		Size: 313.6 KB (313592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37aeceb8c2e5bb3c500129bcf20c3f8aea8c68c353e6714a63a225ed1546e8a1`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d88cd595dc7580d72420b7288c52d4b32201045a13dda1a7b943d9a3468adef`  
		Last Modified: Wed, 09 Mar 2022 14:13:05 GMT  
		Size: 145.5 MB (145488847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be492983ee2b2c9128ce0c732c441ae5fbd203cdb71c94faa253c24b01750c90`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa7b09ca61eb1fbafacee427b430b0879ad4da23e62e430a3fe6a66f181f642`  
		Last Modified: Wed, 09 Mar 2022 18:30:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74014ffde8e1a1677cd81e965bcd2b1f5287bcbf682bbce3bdd125052cd04f29`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43e7b3a6c47e8c9bba8e4ba91d722cd9e491f2df12d5e277356e2b8fc070ba8`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceffc29f93380b6942a245303d5af87875d60351e4c897405f358f018b61b863`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae9e05c08471d9a54c2b46c4f892226ab1eab63b6efd326c44b50bceffb11f2`  
		Last Modified: Thu, 10 Mar 2022 23:22:56 GMT  
		Size: 1.7 MB (1665933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd386d40eef8a252639d03e1486ff30ff8f77cef626bf0592cc7853eb633c7d`  
		Last Modified: Thu, 10 Mar 2022 23:22:54 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:50a38e32a96b709de9e5112eb1909b7f03fab16959929da71f342c5bdb114641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2686; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:c8555e2ca66576a4404c2b5f31d843a5378dea6134acb500502901b563efebcf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14842034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ace180df3e668bd7937be4555305fdb7686c68acf2b5514665e2bac99bd266a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:24:48 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 04:24:50 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 04:24:50 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 04:24:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 04:24:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 04:24:52 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 04:24:52 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 04:24:52 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 04:24:53 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 04:24:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 80
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 443
# Tue, 05 Apr 2022 04:24:54 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 04:24:54 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 04:24:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe024ea85c2d7fb47ce4f044038d4227cee2a982bca3e26a0ea4772b8b652f9a`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 291.2 KB (291230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438e4a77a6e9c40c3bf1fb392618ac596307733f97d294edb86383ce8ff7e51d`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6d2ebbfc8548ecc1dbf4c7568459e52549b81522cb450d42ada1bf82513a8d`  
		Last Modified: Tue, 05 Apr 2022 04:25:34 GMT  
		Size: 11.7 MB (11726452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c5f60dbd2d0286f964c9769a4a3396935a60d0d71ac0e3f8eea5c4c20711fb`  
		Last Modified: Tue, 05 Apr 2022 04:25:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:01ed10f530dfa4af76fa0f13bcdde451a934fbd3a2d77e4cfa72dbc5587ac6f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14049473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c322930340bb73e0796df576638a0214eda5499c8f9b79e4f9af61aeb4da4d2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:14:11 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:14:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 03:14:14 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 03:14:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 03:14:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 03:14:20 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 03:14:21 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 03:14:21 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 03:14:22 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 03:14:22 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 03:14:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 03:14:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 03:14:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 03:14:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 03:14:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 03:14:26 GMT
EXPOSE 80
# Tue, 05 Apr 2022 03:14:26 GMT
EXPOSE 443
# Tue, 05 Apr 2022 03:14:27 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 03:14:27 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 03:14:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d650105deec735ac6dce2611f274a6cf2d9f60fc811167dd6d644e281a38f5`  
		Last Modified: Tue, 05 Apr 2022 03:17:39 GMT  
		Size: 291.7 KB (291653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f3d66a6432942b556bf7a077c220319708b7fc75279695b4b05fa25166fbaf`  
		Last Modified: Tue, 05 Apr 2022 03:17:38 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5d8162ee509e3528dd82e497c4057d40064d43d532acc589b4408c08d2b144`  
		Last Modified: Tue, 05 Apr 2022 03:17:46 GMT  
		Size: 11.1 MB (11125784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0ebc13031265ef07e50f9c7658d00ce8d28c00affdf202b6dd849558f06ad6`  
		Last Modified: Tue, 05 Apr 2022 03:17:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:80bf5252e7e8c04e9ff83dd861f7ee4e81bad7b2b52b5c78a43abf0c95818cf7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dddbbfbbc47ddc2ad3b96622c35ee55ec3eecd5e37cde28c3dfe807ac0827ba`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:52 GMT
ADD file:97f7b59ed0e40e7771daab294820763a7bb86c843317be55725baf1cab39aa12 in / 
# Mon, 04 Apr 2022 23:57:52 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:32:17 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:32:19 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 06:32:20 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 06:32:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 06:32:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:32:26 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 06:32:26 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 06:32:27 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 06:32:27 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 06:32:28 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 06:32:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 06:32:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 06:32:30 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 06:32:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 06:32:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 06:32:31 GMT
EXPOSE 80
# Tue, 05 Apr 2022 06:32:32 GMT
EXPOSE 443
# Tue, 05 Apr 2022 06:32:32 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 06:32:33 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 06:32:33 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:380010979fdd8a9a4b0bf397034a27ec6cabe61d36e9e6d460ea986f0ddaef38`  
		Last Modified: Mon, 04 Apr 2022 23:59:45 GMT  
		Size: 2.4 MB (2427969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0decd23e3d353b46346bc943e7c39f406496ebc5b14731e4575f770563ddef21`  
		Last Modified: Tue, 05 Apr 2022 06:34:41 GMT  
		Size: 290.6 KB (290637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf30d07056a9a35092dc8a190963a5d19c14fce0543c6f6cfed98fc9a687dc5f`  
		Last Modified: Tue, 05 Apr 2022 06:34:40 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbde61fe85af3ebca0218d5ca1f9b5b6d095a57aedc0d7a827ba511e2143629`  
		Last Modified: Tue, 05 Apr 2022 06:34:48 GMT  
		Size: 11.1 MB (11106715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9e55ef38253194b94160973edf2d58fbb2df74561e28d5e7894a3865f9daf8`  
		Last Modified: Tue, 05 Apr 2022 06:34:40 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:e526f540c45973c7a3a4585918890beceac9f0916e124daea3bf4e8b7a1e09b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13753199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2982d1a58becf38a1cf55541dcd74c1b096e8a02bb2060c30540fd3246e46e4f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:11:38 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 03:11:40 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 03:11:41 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 03:11:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 03:11:44 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 03:11:45 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 03:11:46 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 03:11:47 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 03:11:48 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 03:11:49 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 03:11:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 03:11:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 03:11:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 03:11:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 03:11:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 03:11:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 03:11:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 03:11:57 GMT
EXPOSE 80
# Tue, 05 Apr 2022 03:11:58 GMT
EXPOSE 443
# Tue, 05 Apr 2022 03:11:59 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 03:12:00 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 03:12:01 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b907f83114020e794129b34363890abf552785b8d964dbd3546272cc805702ce`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 291.3 KB (291281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988559859d9a4661992cbcefddba5b3d7a16de6c22547a962024f04767e6debf`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 5.7 KB (5748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7769260cde91250d6c68897788b078fea0a63b1254082d2923affeb859224a92`  
		Last Modified: Tue, 05 Apr 2022 03:13:22 GMT  
		Size: 10.7 MB (10738627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0143e63583cae9b0bc2b0048073b6c52476761cbeffa8e6aeca59d227ae0ee2`  
		Last Modified: Tue, 05 Apr 2022 03:13:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:0f4502864c2fae9298130a48ec4ca4351af0787bee15fd4cb5307b7b83e87dd8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13416150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b308dba8382e868224f828f88958151f9c1af01332da44ca296967f8bf09d40b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:44 GMT
ADD file:0b9367758b91930d9d69fd3901262e3a696f7a9f6d9e209e35da83ea6e785837 in / 
# Tue, 05 Apr 2022 00:23:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:07:02 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 07:07:10 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 07:07:12 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 07:07:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 07:07:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 07:07:29 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 07:07:31 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 07:07:33 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 07:07:36 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 07:07:40 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 07:07:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 07:07:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 07:07:47 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 07:07:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 07:07:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 07:07:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 07:07:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 07:08:03 GMT
EXPOSE 80
# Tue, 05 Apr 2022 07:08:06 GMT
EXPOSE 443
# Tue, 05 Apr 2022 07:08:08 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 07:08:10 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 07:08:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ee5f6345565e7aeda814a5c097612cacb0a74186b1f01bf5199e1b812b5d3065`  
		Last Modified: Tue, 05 Apr 2022 00:25:06 GMT  
		Size: 2.8 MB (2814167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8affbe739a71e3875810f257750034ec7a6ee3f2f2c0094f3bcb3ed8a45520b`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 293.7 KB (293710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc927cb41936aaa5bfefa5dc4d654b7193fd568f619707120a5491c620906fc1`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8646c35213c358f518a4d76b75742b5930acec5d12cbd6c75d0a7e217698cee`  
		Last Modified: Tue, 05 Apr 2022 07:11:06 GMT  
		Size: 10.3 MB (10302288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346269e52424a62ec14d10c3e1db1aeb9cefe58f0bf6021855044138396bc074`  
		Last Modified: Tue, 05 Apr 2022 07:11:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:4bdb0834a42c22fa543fe4497215113db9aa55197d55597fb16c6cfd2a7ec22a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14225578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0631ff02e5e01fcee0ebd5387c53f8dca8198463556fd98f569e3454b0bab`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:47 GMT
ADD file:0f70e0f0075bee67acb44e5ef01bf6b9df1f69a25b7aa6fd15bd5bb6ec5bcc9f in / 
# Mon, 04 Apr 2022 23:41:48 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:19:18 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 05 Apr 2022 06:19:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 05 Apr 2022 06:19:20 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 06:19:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 05 Apr 2022 06:19:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:19:22 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 05 Apr 2022 06:19:23 GMT
ENV XDG_DATA_HOME=/data
# Tue, 05 Apr 2022 06:19:23 GMT
VOLUME [/config]
# Tue, 05 Apr 2022 06:19:23 GMT
VOLUME [/data]
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 05 Apr 2022 06:19:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 05 Apr 2022 06:19:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 80
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 443
# Tue, 05 Apr 2022 06:19:24 GMT
EXPOSE 2019
# Tue, 05 Apr 2022 06:19:25 GMT
WORKDIR /srv
# Tue, 05 Apr 2022 06:19:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:6f6a6c77b1bd5dfb3e759efaa292f964f197ae4b96be74d80ef059f87317997a`  
		Last Modified: Mon, 04 Apr 2022 23:42:47 GMT  
		Size: 2.6 MB (2604075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46276fc79092fffc5c0d503ca8733315c8e4002c4e7da79b2383f14c70565746`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 291.8 KB (291788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2e4510a7572a45fad3f051c23678f720057b3bb38d17381f62903aa621c6eb`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf64cfe3d9d0d01f6a1856e4850cd31a634fbb44641472deac6358fdc04352ea`  
		Last Modified: Tue, 05 Apr 2022 06:20:34 GMT  
		Size: 11.3 MB (11323733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363873546085e9612ff25fa067fed8e0038220696a865e645e8046a79035fc99`  
		Last Modified: Tue, 05 Apr 2022 06:20:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:a3ba1d80239cc342421e0b3a6a6adba859191852e94c30047402f2ac1cc24407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:a3ba1d80239cc342421e0b3a6a6adba859191852e94c30047402f2ac1cc24407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
