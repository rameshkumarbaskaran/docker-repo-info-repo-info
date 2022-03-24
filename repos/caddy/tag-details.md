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
$ docker pull caddy@sha256:ea838cedcb447323d5f2726e8671290a277311b5419859d3244640e8f276eb93
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
$ docker pull caddy@sha256:e9451e07cc2803c7a90963bf251e0b81abcc9967ca49fb7a87c3301fad5e60dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735d6b37a42653d291d2a89384895976357b1437fb674a07614cbd3fb35f00e0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:02:43 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 19 Mar 2022 00:02:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 19 Mar 2022 00:02:45 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 19 Mar 2022 00:02:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 19 Mar 2022 00:02:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 19 Mar 2022 00:02:49 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Mar 2022 00:02:49 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Mar 2022 00:02:49 GMT
VOLUME [/config]
# Sat, 19 Mar 2022 00:02:50 GMT
VOLUME [/data]
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 80
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 443
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 2019
# Sat, 19 Mar 2022 00:02:52 GMT
WORKDIR /srv
# Sat, 19 Mar 2022 00:02:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c225d4ce3a38a8a3e6febdc9bbb81aa1faff22dfdccfc44d557d61621d8c3b3`  
		Last Modified: Sat, 19 Mar 2022 00:03:30 GMT  
		Size: 291.2 KB (291236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b48903a98ce96620ab34d505f9fd3337e46ef729e6b93f4c31442a01c031958`  
		Last Modified: Sat, 19 Mar 2022 00:03:29 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9a49498837c179e70172feedd8b5b1684fda96fc85932d533d15fb395d2d25`  
		Last Modified: Sat, 19 Mar 2022 00:03:32 GMT  
		Size: 11.7 MB (11726453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f986cb0c37bc3e0802acdfcb21bfebfdfadce1af2753530be51de31642dc8db5`  
		Last Modified: Sat, 19 Mar 2022 00:03:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5f09a9314e7bcb6c997fafb0c72623e4fe1333f5ffacf717901b8d71992a6314
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14052796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23651bcdf82f31f580af8bb2a691742988178ec24273cc7d427790fc899b70d2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 14:58:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 14:58:06 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 14:58:07 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 14:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 14:58:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 14:58:13 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 14:58:14 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 14:58:14 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 14:58:15 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 14:58:15 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 14:58:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 14:58:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 14:58:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 14:58:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 14:58:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 14:58:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 14:58:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 14:58:19 GMT
EXPOSE 80
# Thu, 17 Mar 2022 14:58:19 GMT
EXPOSE 443
# Thu, 17 Mar 2022 14:58:20 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 14:58:20 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 14:58:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe387c61070bfe1fbf52bdf2f034ca39f369605473616ebfc4b89287058a395d`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 291.6 KB (291648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bc40a5454d774d40dfddbe6f85673f34aed00cd8e9a3035963763b18376639`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81988b3231106e730dc6c7d0b24ebc84826809dd090bff899495129990559e78`  
		Last Modified: Thu, 17 Mar 2022 15:00:19 GMT  
		Size: 11.1 MB (11125802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd1a3665abdbac555066d2695c45980beba49a104e3a55b2d2cf31f8da4c2da`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5d40c99ca31d7c7cc087a8c0059966c8b9e43f0bafbf525cf4fb1494a45da5b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13833799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde5bec726177426cb4d320b0f016f0a8e4569182c6de303c9c9d042446b6197`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 17:21:06 GMT
ADD file:c25fcf153ea349f64e08a1bd0756ce550f2a081ad56cc40c89027d85d1bc26da in / 
# Thu, 17 Mar 2022 17:21:06 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 18:17:11 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 18:17:12 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 18:17:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 18:17:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 18:17:19 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 18:17:19 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 18:17:20 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 18:17:20 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 18:17:21 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 18:17:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 18:17:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 18:17:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 18:17:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 18:17:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 18:17:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 18:17:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 18:17:25 GMT
EXPOSE 80
# Thu, 17 Mar 2022 18:17:25 GMT
EXPOSE 443
# Thu, 17 Mar 2022 18:17:26 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 18:17:26 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 18:17:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c3a1157c36d8d156f7664fa098212ab2149a64bcb59767cdf4595a86617c17fd`  
		Last Modified: Thu, 17 Mar 2022 17:22:45 GMT  
		Size: 2.4 MB (2430456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376a93fbfdd661b6ba92aa7097c65e646f83c50d150e4227f42141e158b7928b`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 290.6 KB (290632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3bd6226dffa9763d44b0e5688ab7b844b744846e3cc0fa7d8ab6d3c068e466`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9ffbfdd3e888d3f9a94270e0b47ca758645b21ec38f6a203223475052b2802`  
		Last Modified: Thu, 17 Mar 2022 18:19:42 GMT  
		Size: 11.1 MB (11106727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb6dc1be2f2389fa78d2d0002c63575d8d14197e59e0347dbca9ae951a38d4f`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:a4e7a7a9d505b716122bbfb9b41e25b8189dafc8115284279687c2021de7aca1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13751720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a574b32ce3c98bd1848efe2e07ad86e55789b4da7fe02909566fa06a0fdbe6a1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 07:13:27 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 18 Mar 2022 07:13:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 18 Mar 2022 07:13:30 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 18 Mar 2022 07:13:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 18 Mar 2022 07:13:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 18 Mar 2022 07:13:34 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 18 Mar 2022 07:13:35 GMT
ENV XDG_DATA_HOME=/data
# Fri, 18 Mar 2022 07:13:36 GMT
VOLUME [/config]
# Fri, 18 Mar 2022 07:13:37 GMT
VOLUME [/data]
# Fri, 18 Mar 2022 07:13:38 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 18 Mar 2022 07:13:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 18 Mar 2022 07:13:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 18 Mar 2022 07:13:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 18 Mar 2022 07:13:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 18 Mar 2022 07:13:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 18 Mar 2022 07:13:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 18 Mar 2022 07:13:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 18 Mar 2022 07:13:46 GMT
EXPOSE 80
# Fri, 18 Mar 2022 07:13:47 GMT
EXPOSE 443
# Fri, 18 Mar 2022 07:13:48 GMT
EXPOSE 2019
# Fri, 18 Mar 2022 07:13:49 GMT
WORKDIR /srv
# Fri, 18 Mar 2022 07:13:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649e3e65430e0077032ab20dedb081c00e1be3a1f4660b94275f242d1dcd295d`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 291.3 KB (291292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048be0a2d569af2daf2b6cd4728a72f8fecd26611069441023a70b360d3850a0`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 5.8 KB (5751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e382adfd8256a09e2e4bed4c90c8755fc3ee3c58e0679734cd85e4da6ac486`  
		Last Modified: Fri, 18 Mar 2022 07:14:59 GMT  
		Size: 10.7 MB (10738636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d589a4f582ad58b1be3ac310f968793927b5d1629ae84b5c78100265bd825d`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:b91b55c6bdcfe17f047217339ace7c264f76e9011d077d7f84cb4852667273e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13419279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0272ad9824009f684ca3ecddd7e61583b5994b0c08a6db63295222a0dbf8a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 18:18:43 GMT
ADD file:bf9c99d8209e0bed9fd3b62cbe691ebf3829d5a35e63e2b066f1f842577a6d24 in / 
# Thu, 17 Mar 2022 18:18:48 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:30:55 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 21:31:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 21:31:03 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 21:31:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 21:31:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 21:31:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 21:31:22 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 21:31:24 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 21:31:27 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 21:31:29 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 21:31:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 21:31:34 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 21:31:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 21:31:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 21:31:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 21:31:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 21:31:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 21:31:49 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:31:55 GMT
EXPOSE 443
# Thu, 17 Mar 2022 21:31:58 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 21:32:01 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 21:32:03 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8b7e8363a93630a772b70e3cf72231f43c62addae0ee8e507c61d43e3781c4e7`  
		Last Modified: Thu, 17 Mar 2022 18:20:01 GMT  
		Size: 2.8 MB (2817281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e91dcc90eb989323abf507cb545731e08fdb7ae99452318650960f3b2bc29b8`  
		Last Modified: Thu, 17 Mar 2022 21:34:38 GMT  
		Size: 293.7 KB (293720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8763c1a56f6f74d41630bbb545d52602505e99c0e311f1ccfc50c001aa5c705c`  
		Last Modified: Thu, 17 Mar 2022 21:34:37 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e19db97ec3aacb5588ff43135ffccf7eef8281b28c0f3e95f8fa4a4c6e9f554`  
		Last Modified: Thu, 17 Mar 2022 21:34:40 GMT  
		Size: 10.3 MB (10302291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5f036cbadaf9e63bb1584d58115f79a3f4f9fdbce665e25642178129efa74b`  
		Last Modified: Thu, 17 Mar 2022 21:34:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:f710373b7c95e8c39a1e57b06884bac2548574d182889812998295c8b120c1ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14226716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced9b4438f1c256b9508d7d3dbf5048aed06c31b8a05cfbda638e5292d0dee83`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:00:36 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 21:00:37 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 21:00:37 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 21:00:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 21:00:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 21:00:40 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 21:00:40 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 21:00:40 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 21:00:41 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 21:00:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 443
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 21:00:42 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 21:00:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c5df2f20a519a7f78f07f63378f86b2481339dccb5001000518f146e1ef5c0`  
		Last Modified: Thu, 17 Mar 2022 21:01:48 GMT  
		Size: 291.8 KB (291797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6179022673cadc5a23974fa435eaa88fbe3c46ae7f0e61e3a80fa34f7cb6c846`  
		Last Modified: Thu, 17 Mar 2022 21:01:47 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a36f8de1aad1bf91018c94013e0cf58d27a1e6c141c8c11cb4beae1b0aaa78`  
		Last Modified: Thu, 17 Mar 2022 21:01:49 GMT  
		Size: 11.3 MB (11323729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f17a5362f8b342e5c3ac44e83b09ad5a9c93dabbea07012c1a32399962536e`  
		Last Modified: Thu, 17 Mar 2022 21:01:48 GMT  
		Size: 152.0 B  
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
$ docker pull caddy@sha256:b5a59725783bab0d65803f87028c68dd6611ca6184040bd98b18797cbe26bdd9
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
$ docker pull caddy@sha256:e9451e07cc2803c7a90963bf251e0b81abcc9967ca49fb7a87c3301fad5e60dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735d6b37a42653d291d2a89384895976357b1437fb674a07614cbd3fb35f00e0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:02:43 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 19 Mar 2022 00:02:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 19 Mar 2022 00:02:45 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 19 Mar 2022 00:02:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 19 Mar 2022 00:02:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 19 Mar 2022 00:02:49 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Mar 2022 00:02:49 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Mar 2022 00:02:49 GMT
VOLUME [/config]
# Sat, 19 Mar 2022 00:02:50 GMT
VOLUME [/data]
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 80
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 443
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 2019
# Sat, 19 Mar 2022 00:02:52 GMT
WORKDIR /srv
# Sat, 19 Mar 2022 00:02:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c225d4ce3a38a8a3e6febdc9bbb81aa1faff22dfdccfc44d557d61621d8c3b3`  
		Last Modified: Sat, 19 Mar 2022 00:03:30 GMT  
		Size: 291.2 KB (291236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b48903a98ce96620ab34d505f9fd3337e46ef729e6b93f4c31442a01c031958`  
		Last Modified: Sat, 19 Mar 2022 00:03:29 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9a49498837c179e70172feedd8b5b1684fda96fc85932d533d15fb395d2d25`  
		Last Modified: Sat, 19 Mar 2022 00:03:32 GMT  
		Size: 11.7 MB (11726453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f986cb0c37bc3e0802acdfcb21bfebfdfadce1af2753530be51de31642dc8db5`  
		Last Modified: Sat, 19 Mar 2022 00:03:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5f09a9314e7bcb6c997fafb0c72623e4fe1333f5ffacf717901b8d71992a6314
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14052796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23651bcdf82f31f580af8bb2a691742988178ec24273cc7d427790fc899b70d2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 14:58:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 14:58:06 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 14:58:07 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 14:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 14:58:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 14:58:13 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 14:58:14 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 14:58:14 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 14:58:15 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 14:58:15 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 14:58:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 14:58:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 14:58:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 14:58:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 14:58:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 14:58:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 14:58:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 14:58:19 GMT
EXPOSE 80
# Thu, 17 Mar 2022 14:58:19 GMT
EXPOSE 443
# Thu, 17 Mar 2022 14:58:20 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 14:58:20 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 14:58:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe387c61070bfe1fbf52bdf2f034ca39f369605473616ebfc4b89287058a395d`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 291.6 KB (291648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bc40a5454d774d40dfddbe6f85673f34aed00cd8e9a3035963763b18376639`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81988b3231106e730dc6c7d0b24ebc84826809dd090bff899495129990559e78`  
		Last Modified: Thu, 17 Mar 2022 15:00:19 GMT  
		Size: 11.1 MB (11125802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd1a3665abdbac555066d2695c45980beba49a104e3a55b2d2cf31f8da4c2da`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5d40c99ca31d7c7cc087a8c0059966c8b9e43f0bafbf525cf4fb1494a45da5b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13833799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde5bec726177426cb4d320b0f016f0a8e4569182c6de303c9c9d042446b6197`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 17:21:06 GMT
ADD file:c25fcf153ea349f64e08a1bd0756ce550f2a081ad56cc40c89027d85d1bc26da in / 
# Thu, 17 Mar 2022 17:21:06 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 18:17:11 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 18:17:12 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 18:17:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 18:17:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 18:17:19 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 18:17:19 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 18:17:20 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 18:17:20 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 18:17:21 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 18:17:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 18:17:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 18:17:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 18:17:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 18:17:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 18:17:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 18:17:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 18:17:25 GMT
EXPOSE 80
# Thu, 17 Mar 2022 18:17:25 GMT
EXPOSE 443
# Thu, 17 Mar 2022 18:17:26 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 18:17:26 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 18:17:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c3a1157c36d8d156f7664fa098212ab2149a64bcb59767cdf4595a86617c17fd`  
		Last Modified: Thu, 17 Mar 2022 17:22:45 GMT  
		Size: 2.4 MB (2430456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376a93fbfdd661b6ba92aa7097c65e646f83c50d150e4227f42141e158b7928b`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 290.6 KB (290632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3bd6226dffa9763d44b0e5688ab7b844b744846e3cc0fa7d8ab6d3c068e466`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9ffbfdd3e888d3f9a94270e0b47ca758645b21ec38f6a203223475052b2802`  
		Last Modified: Thu, 17 Mar 2022 18:19:42 GMT  
		Size: 11.1 MB (11106727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb6dc1be2f2389fa78d2d0002c63575d8d14197e59e0347dbca9ae951a38d4f`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:a4e7a7a9d505b716122bbfb9b41e25b8189dafc8115284279687c2021de7aca1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13751720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a574b32ce3c98bd1848efe2e07ad86e55789b4da7fe02909566fa06a0fdbe6a1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 07:13:27 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 18 Mar 2022 07:13:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 18 Mar 2022 07:13:30 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 18 Mar 2022 07:13:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 18 Mar 2022 07:13:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 18 Mar 2022 07:13:34 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 18 Mar 2022 07:13:35 GMT
ENV XDG_DATA_HOME=/data
# Fri, 18 Mar 2022 07:13:36 GMT
VOLUME [/config]
# Fri, 18 Mar 2022 07:13:37 GMT
VOLUME [/data]
# Fri, 18 Mar 2022 07:13:38 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 18 Mar 2022 07:13:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 18 Mar 2022 07:13:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 18 Mar 2022 07:13:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 18 Mar 2022 07:13:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 18 Mar 2022 07:13:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 18 Mar 2022 07:13:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 18 Mar 2022 07:13:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 18 Mar 2022 07:13:46 GMT
EXPOSE 80
# Fri, 18 Mar 2022 07:13:47 GMT
EXPOSE 443
# Fri, 18 Mar 2022 07:13:48 GMT
EXPOSE 2019
# Fri, 18 Mar 2022 07:13:49 GMT
WORKDIR /srv
# Fri, 18 Mar 2022 07:13:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649e3e65430e0077032ab20dedb081c00e1be3a1f4660b94275f242d1dcd295d`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 291.3 KB (291292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048be0a2d569af2daf2b6cd4728a72f8fecd26611069441023a70b360d3850a0`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 5.8 KB (5751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e382adfd8256a09e2e4bed4c90c8755fc3ee3c58e0679734cd85e4da6ac486`  
		Last Modified: Fri, 18 Mar 2022 07:14:59 GMT  
		Size: 10.7 MB (10738636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d589a4f582ad58b1be3ac310f968793927b5d1629ae84b5c78100265bd825d`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b91b55c6bdcfe17f047217339ace7c264f76e9011d077d7f84cb4852667273e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13419279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0272ad9824009f684ca3ecddd7e61583b5994b0c08a6db63295222a0dbf8a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 18:18:43 GMT
ADD file:bf9c99d8209e0bed9fd3b62cbe691ebf3829d5a35e63e2b066f1f842577a6d24 in / 
# Thu, 17 Mar 2022 18:18:48 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:30:55 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 21:31:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 21:31:03 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 21:31:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 21:31:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 21:31:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 21:31:22 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 21:31:24 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 21:31:27 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 21:31:29 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 21:31:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 21:31:34 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 21:31:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 21:31:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 21:31:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 21:31:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 21:31:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 21:31:49 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:31:55 GMT
EXPOSE 443
# Thu, 17 Mar 2022 21:31:58 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 21:32:01 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 21:32:03 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8b7e8363a93630a772b70e3cf72231f43c62addae0ee8e507c61d43e3781c4e7`  
		Last Modified: Thu, 17 Mar 2022 18:20:01 GMT  
		Size: 2.8 MB (2817281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e91dcc90eb989323abf507cb545731e08fdb7ae99452318650960f3b2bc29b8`  
		Last Modified: Thu, 17 Mar 2022 21:34:38 GMT  
		Size: 293.7 KB (293720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8763c1a56f6f74d41630bbb545d52602505e99c0e311f1ccfc50c001aa5c705c`  
		Last Modified: Thu, 17 Mar 2022 21:34:37 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e19db97ec3aacb5588ff43135ffccf7eef8281b28c0f3e95f8fa4a4c6e9f554`  
		Last Modified: Thu, 17 Mar 2022 21:34:40 GMT  
		Size: 10.3 MB (10302291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5f036cbadaf9e63bb1584d58115f79a3f4f9fdbce665e25642178129efa74b`  
		Last Modified: Thu, 17 Mar 2022 21:34:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:f710373b7c95e8c39a1e57b06884bac2548574d182889812998295c8b120c1ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14226716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced9b4438f1c256b9508d7d3dbf5048aed06c31b8a05cfbda638e5292d0dee83`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:00:36 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 21:00:37 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 21:00:37 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 21:00:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 21:00:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 21:00:40 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 21:00:40 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 21:00:40 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 21:00:41 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 21:00:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 443
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 21:00:42 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 21:00:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c5df2f20a519a7f78f07f63378f86b2481339dccb5001000518f146e1ef5c0`  
		Last Modified: Thu, 17 Mar 2022 21:01:48 GMT  
		Size: 291.8 KB (291797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6179022673cadc5a23974fa435eaa88fbe3c46ae7f0e61e3a80fa34f7cb6c846`  
		Last Modified: Thu, 17 Mar 2022 21:01:47 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a36f8de1aad1bf91018c94013e0cf58d27a1e6c141c8c11cb4beae1b0aaa78`  
		Last Modified: Thu, 17 Mar 2022 21:01:49 GMT  
		Size: 11.3 MB (11323729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f17a5362f8b342e5c3ac44e83b09ad5a9c93dabbea07012c1a32399962536e`  
		Last Modified: Thu, 17 Mar 2022 21:01:48 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:d68bc5f41d6aa3c85abcf9601715ad226a9a29f9e33b7d47c6d963804a3777cd
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
$ docker pull caddy@sha256:2cde19d722eecd94ceaa9bab9a6c4347f74ce5a2fd3a0a48a509e971f13591c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121339146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09d14008da07e14004b96c64f6845c57e0e194ca4de036a13fdf51fe4187d75`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 17:33:52 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 17:47:17 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 17:47:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:49:48 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 17:51:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 17:51:49 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 17:51:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:51:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 17:51:50 GMT
WORKDIR /go
# Wed, 23 Mar 2022 20:57:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 23 Mar 2022 20:57:03 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 23 Mar 2022 20:57:03 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 23 Mar 2022 20:57:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 23 Mar 2022 20:57:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 23 Mar 2022 20:57:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 23 Mar 2022 20:57:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ae170c2a8ceb6dfe7dd52edb58d7be5583518415f0e441c5b7d4f0f8bad244`  
		Last Modified: Wed, 23 Mar 2022 17:34:04 GMT  
		Size: 272.0 KB (271973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb35b180f41941e8ec9af85110ff412f204e4afaf593ac8fc601c07b7449304d`  
		Last Modified: Wed, 23 Mar 2022 17:52:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367011ddbc177b50e507d24a640d8fdbdd64a32a4b0e2a3549ad26a1c0581da5`  
		Last Modified: Wed, 23 Mar 2022 17:53:41 GMT  
		Size: 110.2 MB (110186567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318840287a8912b4d3a5caf13e21932dd668cfa441f84c3f7cb89884f12bc498`  
		Last Modified: Wed, 23 Mar 2022 17:53:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c39dbaf7c7b7fee5c862d4a01ade30b6cc7ab1640f4d9768f164f020ebb0df`  
		Last Modified: Wed, 23 Mar 2022 20:57:42 GMT  
		Size: 6.8 MB (6821487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7c788e131725ef62ff805cf02500b08d59ffe6c17a83e2dfa2c19a5999259e`  
		Last Modified: Wed, 23 Mar 2022 20:57:42 GMT  
		Size: 1.2 MB (1245716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66404f523f94bed92b342dc3d6d751110fe89285e41d3428c8961f4ff8c970ae`  
		Last Modified: Wed, 23 Mar 2022 20:57:41 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f1da3f8fa8aed1df028de4dbfa4512d40b857dae6a2a67f37a3359059c6c8252
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115822199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4371bb88d2b11615cd2bbf5613374b41164d11cf83b1ea4ddc7560961210c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:49:35 GMT
ADD file:fd7f6da4a48df653ae6dd18e6d5959008daf5ce429845c974982dc7d213342d9 in / 
# Wed, 23 Mar 2022 15:49:35 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:19:47 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:19:48 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:19:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:24:07 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:27:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:27:24 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:27:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:27:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:27:26 GMT
WORKDIR /go
# Thu, 24 Mar 2022 02:26:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 02:26:42 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 02:26:43 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 02:26:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 02:26:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 02:26:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 02:26:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4e012d7cd81aa4570d9d209a75131b32f34a3533d5d449d23fd875513922588e`  
		Last Modified: Wed, 23 Mar 2022 15:51:07 GMT  
		Size: 2.6 MB (2624816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b4a951e94c8a6946a91154ab5ace93adbd78d1ebd435a602fb836ac671efd7`  
		Last Modified: Wed, 23 Mar 2022 19:29:03 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63d00ec81dafe9f0ca510122a4959c5a6a1f1c1acf4be47bf25c3cff6cd4be9`  
		Last Modified: Wed, 23 Mar 2022 19:29:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71824796f74f5fbac9812755baf9bc693e67715490b2b7bf6b83484476796f9c`  
		Last Modified: Wed, 23 Mar 2022 19:32:09 GMT  
		Size: 105.1 MB (105068610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5b249d15fb3bdb66c75a0883f0d10c153c767bb066d86c428791a5478ccb1a`  
		Last Modified: Wed, 23 Mar 2022 19:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0daf81a4e5a849bf96c5aea4c17ac34d6b76e6f4d6de637fdc6b71a37fb17aba`  
		Last Modified: Thu, 24 Mar 2022 02:28:34 GMT  
		Size: 6.7 MB (6677403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd152783b4ba077867dc853a8a18f0a188c9416b1df4a65852513c0199c6e68`  
		Last Modified: Thu, 24 Mar 2022 02:28:32 GMT  
		Size: 1.2 MB (1178511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e80b5acad3274c86d1c575b8370883cbc92a0bcf8f69787011ab5e9ad0309d`  
		Last Modified: Thu, 24 Mar 2022 02:28:31 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:02f8b98f2d7f610839150ec7c8b2cb28303ae5b928a3c46827dba569edcd4cc2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114681140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3173e35645f6e2df7cbb70ab3f0caa9e2e9d580c868b7323cbd4daa9fdf36a95`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:43:55 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:43:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:43:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:48:35 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:51:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:51:52 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:51:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:51:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:51:54 GMT
WORKDIR /go
# Thu, 24 Mar 2022 04:35:30 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 04:35:31 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 04:35:31 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 04:35:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 04:35:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 04:35:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 04:35:35 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331b3631dc9d8ace1881c2cb1c28eb266b0ec19c778721faa865e7bb38223ff6`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 271.1 KB (271107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac904122a78116e4100e90af49a2891c00345dbccfae86db8d59e7eb485212d1`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba6f0fdfa168bee61b63cce8a65b54fc5a493c16656abe13d65fb568c83352f`  
		Last Modified: Wed, 23 Mar 2022 21:39:45 GMT  
		Size: 104.9 MB (104853378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137658965282de05bacdac1471373fd69acaae9418ca2169e043327d833e27ca`  
		Last Modified: Wed, 23 Mar 2022 21:38:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52955aeb924042d48cdbb607de289b7457f6a5d6a0e9739931f61fdfe427f344`  
		Last Modified: Thu, 24 Mar 2022 04:37:20 GMT  
		Size: 6.0 MB (5952171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4014b68d35871bfdbe2e53206c7c5d4ced7c200ae0fcd28605f203330c4bfe1`  
		Last Modified: Thu, 24 Mar 2022 04:37:18 GMT  
		Size: 1.2 MB (1176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fba897ff3f805fe40858af1887544e7fa2e99543c8410fbfb002a3a21ddaf8`  
		Last Modified: Thu, 24 Mar 2022 04:37:18 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:ea3dfbed453c77f5f75be7cb81c2ccee9dce3c65b654e8ef309dfe32b33652e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115485391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15729f70afc23409c5069a96dd3a3a35df28d19c5becc3bdc6dacc7c156a3777`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 08:40:42 GMT
RUN apk add --no-cache ca-certificates
# Thu, 24 Mar 2022 09:03:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Mar 2022 09:03:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 09:05:34 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 24 Mar 2022 09:06:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 24 Mar 2022 09:06:52 GMT
ENV GOPATH=/go
# Thu, 24 Mar 2022 09:06:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 09:06:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 24 Mar 2022 09:06:55 GMT
WORKDIR /go
# Thu, 24 Mar 2022 12:06:47 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 12:06:48 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 12:06:49 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 12:06:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 12:06:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 12:06:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 12:06:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b0b4c4587fbfa6f0755490bb53175932c8f0348926efd629b5e26b281aaa57`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 271.8 KB (271767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bc71a7e8dd1d9668121710be981aa07a74660d94ff3bc08a49ec70e7654c7f`  
		Last Modified: Thu, 24 Mar 2022 09:08:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f22eeb6ec86e713b0a2cb7da0cc984bba811a2fd1d3aef57ac8a509969f9a2e`  
		Last Modified: Thu, 24 Mar 2022 09:09:26 GMT  
		Size: 104.4 MB (104423565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1374803ba168889172986189f9d0d20f5b1491771af58ebe714cb84f99fa3a15`  
		Last Modified: Thu, 24 Mar 2022 09:09:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a9f8667a88f626fef41f02488af5fd79509d422aa4e00fe721fd704c067f87`  
		Last Modified: Thu, 24 Mar 2022 12:07:47 GMT  
		Size: 6.9 MB (6925978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b55c23fcf50b7be62fd87f864eb47347cc2bffb823221798cbfcf40d994fdd`  
		Last Modified: Thu, 24 Mar 2022 12:07:46 GMT  
		Size: 1.1 MB (1148676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d38bff84bce7d7ee9ea1a3bfe3473790a3681d0ecec05d0bdd077af8a567ab1`  
		Last Modified: Thu, 24 Mar 2022 12:07:46 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:11649bbf1cf06ebea3bcef630c8601cc35feaa553ade9923fa62f53c282db438
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114315662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc5080a9dc71d919e80a3f561c2b9af0560976209f3535b1c327b1f26650fff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:57:35 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:57:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:57:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 20:14:48 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 20:17:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 20:17:23 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 20:17:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 20:17:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 20:17:52 GMT
WORKDIR /go
# Thu, 24 Mar 2022 03:31:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 03:31:15 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 03:31:18 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 03:31:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 03:31:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 03:31:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 03:31:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1638cef9b912d53eb425be9e028b98f20521ef09b221e120180e69b238a14321`  
		Last Modified: Wed, 23 Mar 2022 20:19:18 GMT  
		Size: 274.2 KB (274168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611046ca672b25224535bd7440ddf58c8b3f23db1f3b3a079dd7411ea06aafa1`  
		Last Modified: Wed, 23 Mar 2022 20:19:17 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5277b684f884438c817309578480b4bbaf44dec0767ea8c51ceb76bb9b9b60`  
		Last Modified: Wed, 23 Mar 2022 20:19:35 GMT  
		Size: 102.8 MB (102784907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb475fbb9abdc19e3bb6e3ce9caedb03b0cfb03f91dffdc01117daa32d36dfa`  
		Last Modified: Wed, 23 Mar 2022 20:19:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53cb43e7adeb1ac72bd05420bc8de466a4b23f7ef2834419cbbe6f04415022f1`  
		Last Modified: Thu, 24 Mar 2022 03:33:11 GMT  
		Size: 7.3 MB (7320988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c822ff2754104c9cdf880adb708e4dec3d253566eb6e2287220bab202d462abc`  
		Last Modified: Thu, 24 Mar 2022 03:33:09 GMT  
		Size: 1.1 MB (1120846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016dbe0d502dc8e63e4f16f1f7936c74e076cbf990aaea69795c2a56b4c137df`  
		Last Modified: Thu, 24 Mar 2022 03:33:09 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:dfcf236ef9b39bb046ee1f48ecd09d1c7fc7a1f577993d7f7853f55eae3d648b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118748542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e7df7a28241422c766fb3b02badc9125abfd33f30709757ca435b65bc47adb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:03:22 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:03:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:03:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:05:28 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:06:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:06:54 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:06:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:06:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:06:55 GMT
WORKDIR /go
# Wed, 23 Mar 2022 22:22:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 23 Mar 2022 22:22:04 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 23 Mar 2022 22:22:04 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 23 Mar 2022 22:22:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 23 Mar 2022 22:22:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 23 Mar 2022 22:22:05 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 23 Mar 2022 22:22:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332d95e018732d014fb48555d26ed3b1acdc693fa15e5e47a76df80ae10a5fb1`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 272.3 KB (272259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f72ff5871bf659daab8a8511372fe2c96cedb9bcf381d83295e789a93f4b07`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80339d6bea83256c3717aaab67711c55ac89a9bc146b9c891fe826e0462b6b5`  
		Last Modified: Wed, 23 Mar 2022 19:09:18 GMT  
		Size: 107.7 MB (107739195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20716e4f8fc56be1943b49531d073a7a30112a97e9c1772dd2d67f495afab1`  
		Last Modified: Wed, 23 Mar 2022 19:09:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cb1e266fa8a15e2d1a81bc572482e40c95b2db376d37a0935415cb96404132`  
		Last Modified: Wed, 23 Mar 2022 22:23:01 GMT  
		Size: 6.9 MB (6930889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b96c8a99cb7674ba09bf70886a1b327bd8dc19b439c6e828dd8fa8de98261d`  
		Last Modified: Wed, 23 Mar 2022 22:23:01 GMT  
		Size: 1.2 MB (1203789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1572768c5198e65924f57fb4f9008d0847a676367109b9e0d0aad64521b498`  
		Last Modified: Wed, 23 Mar 2022 22:23:00 GMT  
		Size: 403.0 B  
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
$ docker pull caddy@sha256:a2ce0b7552206ba989201ea58d325b7c3ddab4ac035b017775e800bf42e224cb
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
$ docker pull caddy@sha256:2cde19d722eecd94ceaa9bab9a6c4347f74ce5a2fd3a0a48a509e971f13591c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121339146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09d14008da07e14004b96c64f6845c57e0e194ca4de036a13fdf51fe4187d75`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 17:33:52 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 17:47:17 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 17:47:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:49:48 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 17:51:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 17:51:49 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 17:51:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:51:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 17:51:50 GMT
WORKDIR /go
# Wed, 23 Mar 2022 20:57:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 23 Mar 2022 20:57:03 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 23 Mar 2022 20:57:03 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 23 Mar 2022 20:57:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 23 Mar 2022 20:57:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 23 Mar 2022 20:57:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 23 Mar 2022 20:57:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ae170c2a8ceb6dfe7dd52edb58d7be5583518415f0e441c5b7d4f0f8bad244`  
		Last Modified: Wed, 23 Mar 2022 17:34:04 GMT  
		Size: 272.0 KB (271973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb35b180f41941e8ec9af85110ff412f204e4afaf593ac8fc601c07b7449304d`  
		Last Modified: Wed, 23 Mar 2022 17:52:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367011ddbc177b50e507d24a640d8fdbdd64a32a4b0e2a3549ad26a1c0581da5`  
		Last Modified: Wed, 23 Mar 2022 17:53:41 GMT  
		Size: 110.2 MB (110186567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318840287a8912b4d3a5caf13e21932dd668cfa441f84c3f7cb89884f12bc498`  
		Last Modified: Wed, 23 Mar 2022 17:53:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c39dbaf7c7b7fee5c862d4a01ade30b6cc7ab1640f4d9768f164f020ebb0df`  
		Last Modified: Wed, 23 Mar 2022 20:57:42 GMT  
		Size: 6.8 MB (6821487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7c788e131725ef62ff805cf02500b08d59ffe6c17a83e2dfa2c19a5999259e`  
		Last Modified: Wed, 23 Mar 2022 20:57:42 GMT  
		Size: 1.2 MB (1245716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66404f523f94bed92b342dc3d6d751110fe89285e41d3428c8961f4ff8c970ae`  
		Last Modified: Wed, 23 Mar 2022 20:57:41 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f1da3f8fa8aed1df028de4dbfa4512d40b857dae6a2a67f37a3359059c6c8252
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115822199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4371bb88d2b11615cd2bbf5613374b41164d11cf83b1ea4ddc7560961210c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:49:35 GMT
ADD file:fd7f6da4a48df653ae6dd18e6d5959008daf5ce429845c974982dc7d213342d9 in / 
# Wed, 23 Mar 2022 15:49:35 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:19:47 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:19:48 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:19:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:24:07 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:27:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:27:24 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:27:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:27:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:27:26 GMT
WORKDIR /go
# Thu, 24 Mar 2022 02:26:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 02:26:42 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 02:26:43 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 02:26:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 02:26:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 02:26:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 02:26:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4e012d7cd81aa4570d9d209a75131b32f34a3533d5d449d23fd875513922588e`  
		Last Modified: Wed, 23 Mar 2022 15:51:07 GMT  
		Size: 2.6 MB (2624816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b4a951e94c8a6946a91154ab5ace93adbd78d1ebd435a602fb836ac671efd7`  
		Last Modified: Wed, 23 Mar 2022 19:29:03 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63d00ec81dafe9f0ca510122a4959c5a6a1f1c1acf4be47bf25c3cff6cd4be9`  
		Last Modified: Wed, 23 Mar 2022 19:29:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71824796f74f5fbac9812755baf9bc693e67715490b2b7bf6b83484476796f9c`  
		Last Modified: Wed, 23 Mar 2022 19:32:09 GMT  
		Size: 105.1 MB (105068610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5b249d15fb3bdb66c75a0883f0d10c153c767bb066d86c428791a5478ccb1a`  
		Last Modified: Wed, 23 Mar 2022 19:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0daf81a4e5a849bf96c5aea4c17ac34d6b76e6f4d6de637fdc6b71a37fb17aba`  
		Last Modified: Thu, 24 Mar 2022 02:28:34 GMT  
		Size: 6.7 MB (6677403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd152783b4ba077867dc853a8a18f0a188c9416b1df4a65852513c0199c6e68`  
		Last Modified: Thu, 24 Mar 2022 02:28:32 GMT  
		Size: 1.2 MB (1178511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e80b5acad3274c86d1c575b8370883cbc92a0bcf8f69787011ab5e9ad0309d`  
		Last Modified: Thu, 24 Mar 2022 02:28:31 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:02f8b98f2d7f610839150ec7c8b2cb28303ae5b928a3c46827dba569edcd4cc2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114681140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3173e35645f6e2df7cbb70ab3f0caa9e2e9d580c868b7323cbd4daa9fdf36a95`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:43:55 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:43:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:43:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:48:35 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:51:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:51:52 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:51:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:51:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:51:54 GMT
WORKDIR /go
# Thu, 24 Mar 2022 04:35:30 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 04:35:31 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 04:35:31 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 04:35:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 04:35:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 04:35:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 04:35:35 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331b3631dc9d8ace1881c2cb1c28eb266b0ec19c778721faa865e7bb38223ff6`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 271.1 KB (271107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac904122a78116e4100e90af49a2891c00345dbccfae86db8d59e7eb485212d1`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba6f0fdfa168bee61b63cce8a65b54fc5a493c16656abe13d65fb568c83352f`  
		Last Modified: Wed, 23 Mar 2022 21:39:45 GMT  
		Size: 104.9 MB (104853378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137658965282de05bacdac1471373fd69acaae9418ca2169e043327d833e27ca`  
		Last Modified: Wed, 23 Mar 2022 21:38:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52955aeb924042d48cdbb607de289b7457f6a5d6a0e9739931f61fdfe427f344`  
		Last Modified: Thu, 24 Mar 2022 04:37:20 GMT  
		Size: 6.0 MB (5952171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4014b68d35871bfdbe2e53206c7c5d4ced7c200ae0fcd28605f203330c4bfe1`  
		Last Modified: Thu, 24 Mar 2022 04:37:18 GMT  
		Size: 1.2 MB (1176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fba897ff3f805fe40858af1887544e7fa2e99543c8410fbfb002a3a21ddaf8`  
		Last Modified: Thu, 24 Mar 2022 04:37:18 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:ea3dfbed453c77f5f75be7cb81c2ccee9dce3c65b654e8ef309dfe32b33652e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115485391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15729f70afc23409c5069a96dd3a3a35df28d19c5becc3bdc6dacc7c156a3777`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 08:40:42 GMT
RUN apk add --no-cache ca-certificates
# Thu, 24 Mar 2022 09:03:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Mar 2022 09:03:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 09:05:34 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 24 Mar 2022 09:06:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 24 Mar 2022 09:06:52 GMT
ENV GOPATH=/go
# Thu, 24 Mar 2022 09:06:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 09:06:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 24 Mar 2022 09:06:55 GMT
WORKDIR /go
# Thu, 24 Mar 2022 12:06:47 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 12:06:48 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 12:06:49 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 12:06:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 12:06:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 12:06:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 12:06:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b0b4c4587fbfa6f0755490bb53175932c8f0348926efd629b5e26b281aaa57`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 271.8 KB (271767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bc71a7e8dd1d9668121710be981aa07a74660d94ff3bc08a49ec70e7654c7f`  
		Last Modified: Thu, 24 Mar 2022 09:08:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f22eeb6ec86e713b0a2cb7da0cc984bba811a2fd1d3aef57ac8a509969f9a2e`  
		Last Modified: Thu, 24 Mar 2022 09:09:26 GMT  
		Size: 104.4 MB (104423565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1374803ba168889172986189f9d0d20f5b1491771af58ebe714cb84f99fa3a15`  
		Last Modified: Thu, 24 Mar 2022 09:09:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a9f8667a88f626fef41f02488af5fd79509d422aa4e00fe721fd704c067f87`  
		Last Modified: Thu, 24 Mar 2022 12:07:47 GMT  
		Size: 6.9 MB (6925978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b55c23fcf50b7be62fd87f864eb47347cc2bffb823221798cbfcf40d994fdd`  
		Last Modified: Thu, 24 Mar 2022 12:07:46 GMT  
		Size: 1.1 MB (1148676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d38bff84bce7d7ee9ea1a3bfe3473790a3681d0ecec05d0bdd077af8a567ab1`  
		Last Modified: Thu, 24 Mar 2022 12:07:46 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:11649bbf1cf06ebea3bcef630c8601cc35feaa553ade9923fa62f53c282db438
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114315662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc5080a9dc71d919e80a3f561c2b9af0560976209f3535b1c327b1f26650fff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:57:35 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:57:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:57:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 20:14:48 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 20:17:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 20:17:23 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 20:17:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 20:17:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 20:17:52 GMT
WORKDIR /go
# Thu, 24 Mar 2022 03:31:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 03:31:15 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 03:31:18 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 03:31:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 03:31:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 03:31:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 03:31:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1638cef9b912d53eb425be9e028b98f20521ef09b221e120180e69b238a14321`  
		Last Modified: Wed, 23 Mar 2022 20:19:18 GMT  
		Size: 274.2 KB (274168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611046ca672b25224535bd7440ddf58c8b3f23db1f3b3a079dd7411ea06aafa1`  
		Last Modified: Wed, 23 Mar 2022 20:19:17 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5277b684f884438c817309578480b4bbaf44dec0767ea8c51ceb76bb9b9b60`  
		Last Modified: Wed, 23 Mar 2022 20:19:35 GMT  
		Size: 102.8 MB (102784907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb475fbb9abdc19e3bb6e3ce9caedb03b0cfb03f91dffdc01117daa32d36dfa`  
		Last Modified: Wed, 23 Mar 2022 20:19:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53cb43e7adeb1ac72bd05420bc8de466a4b23f7ef2834419cbbe6f04415022f1`  
		Last Modified: Thu, 24 Mar 2022 03:33:11 GMT  
		Size: 7.3 MB (7320988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c822ff2754104c9cdf880adb708e4dec3d253566eb6e2287220bab202d462abc`  
		Last Modified: Thu, 24 Mar 2022 03:33:09 GMT  
		Size: 1.1 MB (1120846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016dbe0d502dc8e63e4f16f1f7936c74e076cbf990aaea69795c2a56b4c137df`  
		Last Modified: Thu, 24 Mar 2022 03:33:09 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:dfcf236ef9b39bb046ee1f48ecd09d1c7fc7a1f577993d7f7853f55eae3d648b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118748542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e7df7a28241422c766fb3b02badc9125abfd33f30709757ca435b65bc47adb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:03:22 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:03:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:03:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:05:28 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:06:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:06:54 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:06:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:06:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:06:55 GMT
WORKDIR /go
# Wed, 23 Mar 2022 22:22:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 23 Mar 2022 22:22:04 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 23 Mar 2022 22:22:04 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 23 Mar 2022 22:22:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 23 Mar 2022 22:22:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 23 Mar 2022 22:22:05 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 23 Mar 2022 22:22:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332d95e018732d014fb48555d26ed3b1acdc693fa15e5e47a76df80ae10a5fb1`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 272.3 KB (272259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f72ff5871bf659daab8a8511372fe2c96cedb9bcf381d83295e789a93f4b07`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80339d6bea83256c3717aaab67711c55ac89a9bc146b9c891fe826e0462b6b5`  
		Last Modified: Wed, 23 Mar 2022 19:09:18 GMT  
		Size: 107.7 MB (107739195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20716e4f8fc56be1943b49531d073a7a30112a97e9c1772dd2d67f495afab1`  
		Last Modified: Wed, 23 Mar 2022 19:09:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cb1e266fa8a15e2d1a81bc572482e40c95b2db376d37a0935415cb96404132`  
		Last Modified: Wed, 23 Mar 2022 22:23:01 GMT  
		Size: 6.9 MB (6930889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b96c8a99cb7674ba09bf70886a1b327bd8dc19b439c6e828dd8fa8de98261d`  
		Last Modified: Wed, 23 Mar 2022 22:23:01 GMT  
		Size: 1.2 MB (1203789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1572768c5198e65924f57fb4f9008d0847a676367109b9e0d0aad64521b498`  
		Last Modified: Wed, 23 Mar 2022 22:23:00 GMT  
		Size: 403.0 B  
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
$ docker pull caddy@sha256:ea838cedcb447323d5f2726e8671290a277311b5419859d3244640e8f276eb93
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
$ docker pull caddy@sha256:e9451e07cc2803c7a90963bf251e0b81abcc9967ca49fb7a87c3301fad5e60dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735d6b37a42653d291d2a89384895976357b1437fb674a07614cbd3fb35f00e0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:02:43 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 19 Mar 2022 00:02:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 19 Mar 2022 00:02:45 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 19 Mar 2022 00:02:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 19 Mar 2022 00:02:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 19 Mar 2022 00:02:49 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Mar 2022 00:02:49 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Mar 2022 00:02:49 GMT
VOLUME [/config]
# Sat, 19 Mar 2022 00:02:50 GMT
VOLUME [/data]
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 80
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 443
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 2019
# Sat, 19 Mar 2022 00:02:52 GMT
WORKDIR /srv
# Sat, 19 Mar 2022 00:02:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c225d4ce3a38a8a3e6febdc9bbb81aa1faff22dfdccfc44d557d61621d8c3b3`  
		Last Modified: Sat, 19 Mar 2022 00:03:30 GMT  
		Size: 291.2 KB (291236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b48903a98ce96620ab34d505f9fd3337e46ef729e6b93f4c31442a01c031958`  
		Last Modified: Sat, 19 Mar 2022 00:03:29 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9a49498837c179e70172feedd8b5b1684fda96fc85932d533d15fb395d2d25`  
		Last Modified: Sat, 19 Mar 2022 00:03:32 GMT  
		Size: 11.7 MB (11726453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f986cb0c37bc3e0802acdfcb21bfebfdfadce1af2753530be51de31642dc8db5`  
		Last Modified: Sat, 19 Mar 2022 00:03:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5f09a9314e7bcb6c997fafb0c72623e4fe1333f5ffacf717901b8d71992a6314
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14052796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23651bcdf82f31f580af8bb2a691742988178ec24273cc7d427790fc899b70d2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 14:58:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 14:58:06 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 14:58:07 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 14:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 14:58:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 14:58:13 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 14:58:14 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 14:58:14 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 14:58:15 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 14:58:15 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 14:58:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 14:58:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 14:58:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 14:58:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 14:58:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 14:58:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 14:58:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 14:58:19 GMT
EXPOSE 80
# Thu, 17 Mar 2022 14:58:19 GMT
EXPOSE 443
# Thu, 17 Mar 2022 14:58:20 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 14:58:20 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 14:58:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe387c61070bfe1fbf52bdf2f034ca39f369605473616ebfc4b89287058a395d`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 291.6 KB (291648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bc40a5454d774d40dfddbe6f85673f34aed00cd8e9a3035963763b18376639`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81988b3231106e730dc6c7d0b24ebc84826809dd090bff899495129990559e78`  
		Last Modified: Thu, 17 Mar 2022 15:00:19 GMT  
		Size: 11.1 MB (11125802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd1a3665abdbac555066d2695c45980beba49a104e3a55b2d2cf31f8da4c2da`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5d40c99ca31d7c7cc087a8c0059966c8b9e43f0bafbf525cf4fb1494a45da5b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13833799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde5bec726177426cb4d320b0f016f0a8e4569182c6de303c9c9d042446b6197`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 17:21:06 GMT
ADD file:c25fcf153ea349f64e08a1bd0756ce550f2a081ad56cc40c89027d85d1bc26da in / 
# Thu, 17 Mar 2022 17:21:06 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 18:17:11 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 18:17:12 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 18:17:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 18:17:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 18:17:19 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 18:17:19 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 18:17:20 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 18:17:20 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 18:17:21 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 18:17:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 18:17:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 18:17:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 18:17:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 18:17:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 18:17:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 18:17:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 18:17:25 GMT
EXPOSE 80
# Thu, 17 Mar 2022 18:17:25 GMT
EXPOSE 443
# Thu, 17 Mar 2022 18:17:26 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 18:17:26 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 18:17:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c3a1157c36d8d156f7664fa098212ab2149a64bcb59767cdf4595a86617c17fd`  
		Last Modified: Thu, 17 Mar 2022 17:22:45 GMT  
		Size: 2.4 MB (2430456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376a93fbfdd661b6ba92aa7097c65e646f83c50d150e4227f42141e158b7928b`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 290.6 KB (290632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3bd6226dffa9763d44b0e5688ab7b844b744846e3cc0fa7d8ab6d3c068e466`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9ffbfdd3e888d3f9a94270e0b47ca758645b21ec38f6a203223475052b2802`  
		Last Modified: Thu, 17 Mar 2022 18:19:42 GMT  
		Size: 11.1 MB (11106727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb6dc1be2f2389fa78d2d0002c63575d8d14197e59e0347dbca9ae951a38d4f`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:a4e7a7a9d505b716122bbfb9b41e25b8189dafc8115284279687c2021de7aca1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13751720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a574b32ce3c98bd1848efe2e07ad86e55789b4da7fe02909566fa06a0fdbe6a1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 07:13:27 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 18 Mar 2022 07:13:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 18 Mar 2022 07:13:30 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 18 Mar 2022 07:13:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 18 Mar 2022 07:13:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 18 Mar 2022 07:13:34 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 18 Mar 2022 07:13:35 GMT
ENV XDG_DATA_HOME=/data
# Fri, 18 Mar 2022 07:13:36 GMT
VOLUME [/config]
# Fri, 18 Mar 2022 07:13:37 GMT
VOLUME [/data]
# Fri, 18 Mar 2022 07:13:38 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 18 Mar 2022 07:13:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 18 Mar 2022 07:13:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 18 Mar 2022 07:13:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 18 Mar 2022 07:13:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 18 Mar 2022 07:13:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 18 Mar 2022 07:13:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 18 Mar 2022 07:13:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 18 Mar 2022 07:13:46 GMT
EXPOSE 80
# Fri, 18 Mar 2022 07:13:47 GMT
EXPOSE 443
# Fri, 18 Mar 2022 07:13:48 GMT
EXPOSE 2019
# Fri, 18 Mar 2022 07:13:49 GMT
WORKDIR /srv
# Fri, 18 Mar 2022 07:13:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649e3e65430e0077032ab20dedb081c00e1be3a1f4660b94275f242d1dcd295d`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 291.3 KB (291292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048be0a2d569af2daf2b6cd4728a72f8fecd26611069441023a70b360d3850a0`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 5.8 KB (5751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e382adfd8256a09e2e4bed4c90c8755fc3ee3c58e0679734cd85e4da6ac486`  
		Last Modified: Fri, 18 Mar 2022 07:14:59 GMT  
		Size: 10.7 MB (10738636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d589a4f582ad58b1be3ac310f968793927b5d1629ae84b5c78100265bd825d`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; ppc64le

```console
$ docker pull caddy@sha256:b91b55c6bdcfe17f047217339ace7c264f76e9011d077d7f84cb4852667273e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13419279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0272ad9824009f684ca3ecddd7e61583b5994b0c08a6db63295222a0dbf8a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 18:18:43 GMT
ADD file:bf9c99d8209e0bed9fd3b62cbe691ebf3829d5a35e63e2b066f1f842577a6d24 in / 
# Thu, 17 Mar 2022 18:18:48 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:30:55 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 21:31:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 21:31:03 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 21:31:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 21:31:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 21:31:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 21:31:22 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 21:31:24 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 21:31:27 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 21:31:29 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 21:31:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 21:31:34 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 21:31:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 21:31:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 21:31:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 21:31:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 21:31:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 21:31:49 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:31:55 GMT
EXPOSE 443
# Thu, 17 Mar 2022 21:31:58 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 21:32:01 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 21:32:03 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8b7e8363a93630a772b70e3cf72231f43c62addae0ee8e507c61d43e3781c4e7`  
		Last Modified: Thu, 17 Mar 2022 18:20:01 GMT  
		Size: 2.8 MB (2817281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e91dcc90eb989323abf507cb545731e08fdb7ae99452318650960f3b2bc29b8`  
		Last Modified: Thu, 17 Mar 2022 21:34:38 GMT  
		Size: 293.7 KB (293720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8763c1a56f6f74d41630bbb545d52602505e99c0e311f1ccfc50c001aa5c705c`  
		Last Modified: Thu, 17 Mar 2022 21:34:37 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e19db97ec3aacb5588ff43135ffccf7eef8281b28c0f3e95f8fa4a4c6e9f554`  
		Last Modified: Thu, 17 Mar 2022 21:34:40 GMT  
		Size: 10.3 MB (10302291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5f036cbadaf9e63bb1584d58115f79a3f4f9fdbce665e25642178129efa74b`  
		Last Modified: Thu, 17 Mar 2022 21:34:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; s390x

```console
$ docker pull caddy@sha256:f710373b7c95e8c39a1e57b06884bac2548574d182889812998295c8b120c1ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14226716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced9b4438f1c256b9508d7d3dbf5048aed06c31b8a05cfbda638e5292d0dee83`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:00:36 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 21:00:37 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 21:00:37 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 21:00:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 21:00:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 21:00:40 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 21:00:40 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 21:00:40 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 21:00:41 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 21:00:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 443
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 21:00:42 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 21:00:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c5df2f20a519a7f78f07f63378f86b2481339dccb5001000518f146e1ef5c0`  
		Last Modified: Thu, 17 Mar 2022 21:01:48 GMT  
		Size: 291.8 KB (291797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6179022673cadc5a23974fa435eaa88fbe3c46ae7f0e61e3a80fa34f7cb6c846`  
		Last Modified: Thu, 17 Mar 2022 21:01:47 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a36f8de1aad1bf91018c94013e0cf58d27a1e6c141c8c11cb4beae1b0aaa78`  
		Last Modified: Thu, 17 Mar 2022 21:01:49 GMT  
		Size: 11.3 MB (11323729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f17a5362f8b342e5c3ac44e83b09ad5a9c93dabbea07012c1a32399962536e`  
		Last Modified: Thu, 17 Mar 2022 21:01:48 GMT  
		Size: 152.0 B  
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
$ docker pull caddy@sha256:b5a59725783bab0d65803f87028c68dd6611ca6184040bd98b18797cbe26bdd9
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
$ docker pull caddy@sha256:e9451e07cc2803c7a90963bf251e0b81abcc9967ca49fb7a87c3301fad5e60dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735d6b37a42653d291d2a89384895976357b1437fb674a07614cbd3fb35f00e0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:02:43 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 19 Mar 2022 00:02:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 19 Mar 2022 00:02:45 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 19 Mar 2022 00:02:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 19 Mar 2022 00:02:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 19 Mar 2022 00:02:49 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Mar 2022 00:02:49 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Mar 2022 00:02:49 GMT
VOLUME [/config]
# Sat, 19 Mar 2022 00:02:50 GMT
VOLUME [/data]
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 80
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 443
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 2019
# Sat, 19 Mar 2022 00:02:52 GMT
WORKDIR /srv
# Sat, 19 Mar 2022 00:02:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c225d4ce3a38a8a3e6febdc9bbb81aa1faff22dfdccfc44d557d61621d8c3b3`  
		Last Modified: Sat, 19 Mar 2022 00:03:30 GMT  
		Size: 291.2 KB (291236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b48903a98ce96620ab34d505f9fd3337e46ef729e6b93f4c31442a01c031958`  
		Last Modified: Sat, 19 Mar 2022 00:03:29 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9a49498837c179e70172feedd8b5b1684fda96fc85932d533d15fb395d2d25`  
		Last Modified: Sat, 19 Mar 2022 00:03:32 GMT  
		Size: 11.7 MB (11726453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f986cb0c37bc3e0802acdfcb21bfebfdfadce1af2753530be51de31642dc8db5`  
		Last Modified: Sat, 19 Mar 2022 00:03:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5f09a9314e7bcb6c997fafb0c72623e4fe1333f5ffacf717901b8d71992a6314
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14052796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23651bcdf82f31f580af8bb2a691742988178ec24273cc7d427790fc899b70d2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 14:58:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 14:58:06 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 14:58:07 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 14:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 14:58:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 14:58:13 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 14:58:14 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 14:58:14 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 14:58:15 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 14:58:15 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 14:58:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 14:58:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 14:58:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 14:58:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 14:58:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 14:58:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 14:58:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 14:58:19 GMT
EXPOSE 80
# Thu, 17 Mar 2022 14:58:19 GMT
EXPOSE 443
# Thu, 17 Mar 2022 14:58:20 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 14:58:20 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 14:58:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe387c61070bfe1fbf52bdf2f034ca39f369605473616ebfc4b89287058a395d`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 291.6 KB (291648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bc40a5454d774d40dfddbe6f85673f34aed00cd8e9a3035963763b18376639`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81988b3231106e730dc6c7d0b24ebc84826809dd090bff899495129990559e78`  
		Last Modified: Thu, 17 Mar 2022 15:00:19 GMT  
		Size: 11.1 MB (11125802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd1a3665abdbac555066d2695c45980beba49a104e3a55b2d2cf31f8da4c2da`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5d40c99ca31d7c7cc087a8c0059966c8b9e43f0bafbf525cf4fb1494a45da5b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13833799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde5bec726177426cb4d320b0f016f0a8e4569182c6de303c9c9d042446b6197`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 17:21:06 GMT
ADD file:c25fcf153ea349f64e08a1bd0756ce550f2a081ad56cc40c89027d85d1bc26da in / 
# Thu, 17 Mar 2022 17:21:06 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 18:17:11 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 18:17:12 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 18:17:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 18:17:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 18:17:19 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 18:17:19 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 18:17:20 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 18:17:20 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 18:17:21 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 18:17:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 18:17:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 18:17:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 18:17:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 18:17:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 18:17:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 18:17:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 18:17:25 GMT
EXPOSE 80
# Thu, 17 Mar 2022 18:17:25 GMT
EXPOSE 443
# Thu, 17 Mar 2022 18:17:26 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 18:17:26 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 18:17:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c3a1157c36d8d156f7664fa098212ab2149a64bcb59767cdf4595a86617c17fd`  
		Last Modified: Thu, 17 Mar 2022 17:22:45 GMT  
		Size: 2.4 MB (2430456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376a93fbfdd661b6ba92aa7097c65e646f83c50d150e4227f42141e158b7928b`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 290.6 KB (290632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3bd6226dffa9763d44b0e5688ab7b844b744846e3cc0fa7d8ab6d3c068e466`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9ffbfdd3e888d3f9a94270e0b47ca758645b21ec38f6a203223475052b2802`  
		Last Modified: Thu, 17 Mar 2022 18:19:42 GMT  
		Size: 11.1 MB (11106727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb6dc1be2f2389fa78d2d0002c63575d8d14197e59e0347dbca9ae951a38d4f`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:a4e7a7a9d505b716122bbfb9b41e25b8189dafc8115284279687c2021de7aca1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13751720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a574b32ce3c98bd1848efe2e07ad86e55789b4da7fe02909566fa06a0fdbe6a1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 07:13:27 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 18 Mar 2022 07:13:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 18 Mar 2022 07:13:30 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 18 Mar 2022 07:13:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 18 Mar 2022 07:13:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 18 Mar 2022 07:13:34 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 18 Mar 2022 07:13:35 GMT
ENV XDG_DATA_HOME=/data
# Fri, 18 Mar 2022 07:13:36 GMT
VOLUME [/config]
# Fri, 18 Mar 2022 07:13:37 GMT
VOLUME [/data]
# Fri, 18 Mar 2022 07:13:38 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 18 Mar 2022 07:13:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 18 Mar 2022 07:13:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 18 Mar 2022 07:13:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 18 Mar 2022 07:13:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 18 Mar 2022 07:13:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 18 Mar 2022 07:13:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 18 Mar 2022 07:13:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 18 Mar 2022 07:13:46 GMT
EXPOSE 80
# Fri, 18 Mar 2022 07:13:47 GMT
EXPOSE 443
# Fri, 18 Mar 2022 07:13:48 GMT
EXPOSE 2019
# Fri, 18 Mar 2022 07:13:49 GMT
WORKDIR /srv
# Fri, 18 Mar 2022 07:13:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649e3e65430e0077032ab20dedb081c00e1be3a1f4660b94275f242d1dcd295d`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 291.3 KB (291292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048be0a2d569af2daf2b6cd4728a72f8fecd26611069441023a70b360d3850a0`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 5.8 KB (5751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e382adfd8256a09e2e4bed4c90c8755fc3ee3c58e0679734cd85e4da6ac486`  
		Last Modified: Fri, 18 Mar 2022 07:14:59 GMT  
		Size: 10.7 MB (10738636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d589a4f582ad58b1be3ac310f968793927b5d1629ae84b5c78100265bd825d`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b91b55c6bdcfe17f047217339ace7c264f76e9011d077d7f84cb4852667273e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13419279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0272ad9824009f684ca3ecddd7e61583b5994b0c08a6db63295222a0dbf8a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 18:18:43 GMT
ADD file:bf9c99d8209e0bed9fd3b62cbe691ebf3829d5a35e63e2b066f1f842577a6d24 in / 
# Thu, 17 Mar 2022 18:18:48 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:30:55 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 21:31:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 21:31:03 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 21:31:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 21:31:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 21:31:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 21:31:22 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 21:31:24 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 21:31:27 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 21:31:29 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 21:31:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 21:31:34 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 21:31:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 21:31:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 21:31:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 21:31:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 21:31:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 21:31:49 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:31:55 GMT
EXPOSE 443
# Thu, 17 Mar 2022 21:31:58 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 21:32:01 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 21:32:03 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8b7e8363a93630a772b70e3cf72231f43c62addae0ee8e507c61d43e3781c4e7`  
		Last Modified: Thu, 17 Mar 2022 18:20:01 GMT  
		Size: 2.8 MB (2817281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e91dcc90eb989323abf507cb545731e08fdb7ae99452318650960f3b2bc29b8`  
		Last Modified: Thu, 17 Mar 2022 21:34:38 GMT  
		Size: 293.7 KB (293720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8763c1a56f6f74d41630bbb545d52602505e99c0e311f1ccfc50c001aa5c705c`  
		Last Modified: Thu, 17 Mar 2022 21:34:37 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e19db97ec3aacb5588ff43135ffccf7eef8281b28c0f3e95f8fa4a4c6e9f554`  
		Last Modified: Thu, 17 Mar 2022 21:34:40 GMT  
		Size: 10.3 MB (10302291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5f036cbadaf9e63bb1584d58115f79a3f4f9fdbce665e25642178129efa74b`  
		Last Modified: Thu, 17 Mar 2022 21:34:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:f710373b7c95e8c39a1e57b06884bac2548574d182889812998295c8b120c1ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14226716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced9b4438f1c256b9508d7d3dbf5048aed06c31b8a05cfbda638e5292d0dee83`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:00:36 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 21:00:37 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 21:00:37 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 21:00:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 21:00:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 21:00:40 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 21:00:40 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 21:00:40 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 21:00:41 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 21:00:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 443
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 21:00:42 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 21:00:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c5df2f20a519a7f78f07f63378f86b2481339dccb5001000518f146e1ef5c0`  
		Last Modified: Thu, 17 Mar 2022 21:01:48 GMT  
		Size: 291.8 KB (291797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6179022673cadc5a23974fa435eaa88fbe3c46ae7f0e61e3a80fa34f7cb6c846`  
		Last Modified: Thu, 17 Mar 2022 21:01:47 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a36f8de1aad1bf91018c94013e0cf58d27a1e6c141c8c11cb4beae1b0aaa78`  
		Last Modified: Thu, 17 Mar 2022 21:01:49 GMT  
		Size: 11.3 MB (11323729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f17a5362f8b342e5c3ac44e83b09ad5a9c93dabbea07012c1a32399962536e`  
		Last Modified: Thu, 17 Mar 2022 21:01:48 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-builder`

```console
$ docker pull caddy@sha256:d68bc5f41d6aa3c85abcf9601715ad226a9a29f9e33b7d47c6d963804a3777cd
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
$ docker pull caddy@sha256:2cde19d722eecd94ceaa9bab9a6c4347f74ce5a2fd3a0a48a509e971f13591c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121339146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09d14008da07e14004b96c64f6845c57e0e194ca4de036a13fdf51fe4187d75`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 17:33:52 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 17:47:17 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 17:47:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:49:48 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 17:51:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 17:51:49 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 17:51:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:51:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 17:51:50 GMT
WORKDIR /go
# Wed, 23 Mar 2022 20:57:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 23 Mar 2022 20:57:03 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 23 Mar 2022 20:57:03 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 23 Mar 2022 20:57:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 23 Mar 2022 20:57:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 23 Mar 2022 20:57:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 23 Mar 2022 20:57:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ae170c2a8ceb6dfe7dd52edb58d7be5583518415f0e441c5b7d4f0f8bad244`  
		Last Modified: Wed, 23 Mar 2022 17:34:04 GMT  
		Size: 272.0 KB (271973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb35b180f41941e8ec9af85110ff412f204e4afaf593ac8fc601c07b7449304d`  
		Last Modified: Wed, 23 Mar 2022 17:52:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367011ddbc177b50e507d24a640d8fdbdd64a32a4b0e2a3549ad26a1c0581da5`  
		Last Modified: Wed, 23 Mar 2022 17:53:41 GMT  
		Size: 110.2 MB (110186567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318840287a8912b4d3a5caf13e21932dd668cfa441f84c3f7cb89884f12bc498`  
		Last Modified: Wed, 23 Mar 2022 17:53:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c39dbaf7c7b7fee5c862d4a01ade30b6cc7ab1640f4d9768f164f020ebb0df`  
		Last Modified: Wed, 23 Mar 2022 20:57:42 GMT  
		Size: 6.8 MB (6821487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7c788e131725ef62ff805cf02500b08d59ffe6c17a83e2dfa2c19a5999259e`  
		Last Modified: Wed, 23 Mar 2022 20:57:42 GMT  
		Size: 1.2 MB (1245716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66404f523f94bed92b342dc3d6d751110fe89285e41d3428c8961f4ff8c970ae`  
		Last Modified: Wed, 23 Mar 2022 20:57:41 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f1da3f8fa8aed1df028de4dbfa4512d40b857dae6a2a67f37a3359059c6c8252
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115822199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4371bb88d2b11615cd2bbf5613374b41164d11cf83b1ea4ddc7560961210c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:49:35 GMT
ADD file:fd7f6da4a48df653ae6dd18e6d5959008daf5ce429845c974982dc7d213342d9 in / 
# Wed, 23 Mar 2022 15:49:35 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:19:47 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:19:48 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:19:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:24:07 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:27:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:27:24 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:27:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:27:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:27:26 GMT
WORKDIR /go
# Thu, 24 Mar 2022 02:26:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 02:26:42 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 02:26:43 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 02:26:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 02:26:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 02:26:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 02:26:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4e012d7cd81aa4570d9d209a75131b32f34a3533d5d449d23fd875513922588e`  
		Last Modified: Wed, 23 Mar 2022 15:51:07 GMT  
		Size: 2.6 MB (2624816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b4a951e94c8a6946a91154ab5ace93adbd78d1ebd435a602fb836ac671efd7`  
		Last Modified: Wed, 23 Mar 2022 19:29:03 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63d00ec81dafe9f0ca510122a4959c5a6a1f1c1acf4be47bf25c3cff6cd4be9`  
		Last Modified: Wed, 23 Mar 2022 19:29:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71824796f74f5fbac9812755baf9bc693e67715490b2b7bf6b83484476796f9c`  
		Last Modified: Wed, 23 Mar 2022 19:32:09 GMT  
		Size: 105.1 MB (105068610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5b249d15fb3bdb66c75a0883f0d10c153c767bb066d86c428791a5478ccb1a`  
		Last Modified: Wed, 23 Mar 2022 19:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0daf81a4e5a849bf96c5aea4c17ac34d6b76e6f4d6de637fdc6b71a37fb17aba`  
		Last Modified: Thu, 24 Mar 2022 02:28:34 GMT  
		Size: 6.7 MB (6677403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd152783b4ba077867dc853a8a18f0a188c9416b1df4a65852513c0199c6e68`  
		Last Modified: Thu, 24 Mar 2022 02:28:32 GMT  
		Size: 1.2 MB (1178511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e80b5acad3274c86d1c575b8370883cbc92a0bcf8f69787011ab5e9ad0309d`  
		Last Modified: Thu, 24 Mar 2022 02:28:31 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:02f8b98f2d7f610839150ec7c8b2cb28303ae5b928a3c46827dba569edcd4cc2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114681140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3173e35645f6e2df7cbb70ab3f0caa9e2e9d580c868b7323cbd4daa9fdf36a95`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:43:55 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:43:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:43:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:48:35 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:51:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:51:52 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:51:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:51:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:51:54 GMT
WORKDIR /go
# Thu, 24 Mar 2022 04:35:30 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 04:35:31 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 04:35:31 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 04:35:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 04:35:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 04:35:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 04:35:35 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331b3631dc9d8ace1881c2cb1c28eb266b0ec19c778721faa865e7bb38223ff6`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 271.1 KB (271107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac904122a78116e4100e90af49a2891c00345dbccfae86db8d59e7eb485212d1`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba6f0fdfa168bee61b63cce8a65b54fc5a493c16656abe13d65fb568c83352f`  
		Last Modified: Wed, 23 Mar 2022 21:39:45 GMT  
		Size: 104.9 MB (104853378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137658965282de05bacdac1471373fd69acaae9418ca2169e043327d833e27ca`  
		Last Modified: Wed, 23 Mar 2022 21:38:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52955aeb924042d48cdbb607de289b7457f6a5d6a0e9739931f61fdfe427f344`  
		Last Modified: Thu, 24 Mar 2022 04:37:20 GMT  
		Size: 6.0 MB (5952171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4014b68d35871bfdbe2e53206c7c5d4ced7c200ae0fcd28605f203330c4bfe1`  
		Last Modified: Thu, 24 Mar 2022 04:37:18 GMT  
		Size: 1.2 MB (1176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fba897ff3f805fe40858af1887544e7fa2e99543c8410fbfb002a3a21ddaf8`  
		Last Modified: Thu, 24 Mar 2022 04:37:18 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:ea3dfbed453c77f5f75be7cb81c2ccee9dce3c65b654e8ef309dfe32b33652e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115485391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15729f70afc23409c5069a96dd3a3a35df28d19c5becc3bdc6dacc7c156a3777`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 08:40:42 GMT
RUN apk add --no-cache ca-certificates
# Thu, 24 Mar 2022 09:03:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Mar 2022 09:03:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 09:05:34 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 24 Mar 2022 09:06:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 24 Mar 2022 09:06:52 GMT
ENV GOPATH=/go
# Thu, 24 Mar 2022 09:06:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 09:06:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 24 Mar 2022 09:06:55 GMT
WORKDIR /go
# Thu, 24 Mar 2022 12:06:47 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 12:06:48 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 12:06:49 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 12:06:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 12:06:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 12:06:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 12:06:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b0b4c4587fbfa6f0755490bb53175932c8f0348926efd629b5e26b281aaa57`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 271.8 KB (271767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bc71a7e8dd1d9668121710be981aa07a74660d94ff3bc08a49ec70e7654c7f`  
		Last Modified: Thu, 24 Mar 2022 09:08:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f22eeb6ec86e713b0a2cb7da0cc984bba811a2fd1d3aef57ac8a509969f9a2e`  
		Last Modified: Thu, 24 Mar 2022 09:09:26 GMT  
		Size: 104.4 MB (104423565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1374803ba168889172986189f9d0d20f5b1491771af58ebe714cb84f99fa3a15`  
		Last Modified: Thu, 24 Mar 2022 09:09:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a9f8667a88f626fef41f02488af5fd79509d422aa4e00fe721fd704c067f87`  
		Last Modified: Thu, 24 Mar 2022 12:07:47 GMT  
		Size: 6.9 MB (6925978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b55c23fcf50b7be62fd87f864eb47347cc2bffb823221798cbfcf40d994fdd`  
		Last Modified: Thu, 24 Mar 2022 12:07:46 GMT  
		Size: 1.1 MB (1148676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d38bff84bce7d7ee9ea1a3bfe3473790a3681d0ecec05d0bdd077af8a567ab1`  
		Last Modified: Thu, 24 Mar 2022 12:07:46 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:11649bbf1cf06ebea3bcef630c8601cc35feaa553ade9923fa62f53c282db438
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114315662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc5080a9dc71d919e80a3f561c2b9af0560976209f3535b1c327b1f26650fff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:57:35 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:57:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:57:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 20:14:48 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 20:17:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 20:17:23 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 20:17:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 20:17:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 20:17:52 GMT
WORKDIR /go
# Thu, 24 Mar 2022 03:31:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 03:31:15 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 03:31:18 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 03:31:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 03:31:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 03:31:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 03:31:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1638cef9b912d53eb425be9e028b98f20521ef09b221e120180e69b238a14321`  
		Last Modified: Wed, 23 Mar 2022 20:19:18 GMT  
		Size: 274.2 KB (274168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611046ca672b25224535bd7440ddf58c8b3f23db1f3b3a079dd7411ea06aafa1`  
		Last Modified: Wed, 23 Mar 2022 20:19:17 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5277b684f884438c817309578480b4bbaf44dec0767ea8c51ceb76bb9b9b60`  
		Last Modified: Wed, 23 Mar 2022 20:19:35 GMT  
		Size: 102.8 MB (102784907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb475fbb9abdc19e3bb6e3ce9caedb03b0cfb03f91dffdc01117daa32d36dfa`  
		Last Modified: Wed, 23 Mar 2022 20:19:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53cb43e7adeb1ac72bd05420bc8de466a4b23f7ef2834419cbbe6f04415022f1`  
		Last Modified: Thu, 24 Mar 2022 03:33:11 GMT  
		Size: 7.3 MB (7320988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c822ff2754104c9cdf880adb708e4dec3d253566eb6e2287220bab202d462abc`  
		Last Modified: Thu, 24 Mar 2022 03:33:09 GMT  
		Size: 1.1 MB (1120846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016dbe0d502dc8e63e4f16f1f7936c74e076cbf990aaea69795c2a56b4c137df`  
		Last Modified: Thu, 24 Mar 2022 03:33:09 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; s390x

```console
$ docker pull caddy@sha256:dfcf236ef9b39bb046ee1f48ecd09d1c7fc7a1f577993d7f7853f55eae3d648b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118748542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e7df7a28241422c766fb3b02badc9125abfd33f30709757ca435b65bc47adb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:03:22 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:03:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:03:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:05:28 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:06:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:06:54 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:06:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:06:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:06:55 GMT
WORKDIR /go
# Wed, 23 Mar 2022 22:22:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 23 Mar 2022 22:22:04 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 23 Mar 2022 22:22:04 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 23 Mar 2022 22:22:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 23 Mar 2022 22:22:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 23 Mar 2022 22:22:05 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 23 Mar 2022 22:22:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332d95e018732d014fb48555d26ed3b1acdc693fa15e5e47a76df80ae10a5fb1`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 272.3 KB (272259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f72ff5871bf659daab8a8511372fe2c96cedb9bcf381d83295e789a93f4b07`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80339d6bea83256c3717aaab67711c55ac89a9bc146b9c891fe826e0462b6b5`  
		Last Modified: Wed, 23 Mar 2022 19:09:18 GMT  
		Size: 107.7 MB (107739195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20716e4f8fc56be1943b49531d073a7a30112a97e9c1772dd2d67f495afab1`  
		Last Modified: Wed, 23 Mar 2022 19:09:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cb1e266fa8a15e2d1a81bc572482e40c95b2db376d37a0935415cb96404132`  
		Last Modified: Wed, 23 Mar 2022 22:23:01 GMT  
		Size: 6.9 MB (6930889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b96c8a99cb7674ba09bf70886a1b327bd8dc19b439c6e828dd8fa8de98261d`  
		Last Modified: Wed, 23 Mar 2022 22:23:01 GMT  
		Size: 1.2 MB (1203789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1572768c5198e65924f57fb4f9008d0847a676367109b9e0d0aad64521b498`  
		Last Modified: Wed, 23 Mar 2022 22:23:00 GMT  
		Size: 403.0 B  
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
$ docker pull caddy@sha256:a2ce0b7552206ba989201ea58d325b7c3ddab4ac035b017775e800bf42e224cb
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
$ docker pull caddy@sha256:2cde19d722eecd94ceaa9bab9a6c4347f74ce5a2fd3a0a48a509e971f13591c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121339146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09d14008da07e14004b96c64f6845c57e0e194ca4de036a13fdf51fe4187d75`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 17:33:52 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 17:47:17 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 17:47:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:49:48 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 17:51:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 17:51:49 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 17:51:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:51:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 17:51:50 GMT
WORKDIR /go
# Wed, 23 Mar 2022 20:57:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 23 Mar 2022 20:57:03 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 23 Mar 2022 20:57:03 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 23 Mar 2022 20:57:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 23 Mar 2022 20:57:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 23 Mar 2022 20:57:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 23 Mar 2022 20:57:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ae170c2a8ceb6dfe7dd52edb58d7be5583518415f0e441c5b7d4f0f8bad244`  
		Last Modified: Wed, 23 Mar 2022 17:34:04 GMT  
		Size: 272.0 KB (271973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb35b180f41941e8ec9af85110ff412f204e4afaf593ac8fc601c07b7449304d`  
		Last Modified: Wed, 23 Mar 2022 17:52:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367011ddbc177b50e507d24a640d8fdbdd64a32a4b0e2a3549ad26a1c0581da5`  
		Last Modified: Wed, 23 Mar 2022 17:53:41 GMT  
		Size: 110.2 MB (110186567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318840287a8912b4d3a5caf13e21932dd668cfa441f84c3f7cb89884f12bc498`  
		Last Modified: Wed, 23 Mar 2022 17:53:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c39dbaf7c7b7fee5c862d4a01ade30b6cc7ab1640f4d9768f164f020ebb0df`  
		Last Modified: Wed, 23 Mar 2022 20:57:42 GMT  
		Size: 6.8 MB (6821487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7c788e131725ef62ff805cf02500b08d59ffe6c17a83e2dfa2c19a5999259e`  
		Last Modified: Wed, 23 Mar 2022 20:57:42 GMT  
		Size: 1.2 MB (1245716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66404f523f94bed92b342dc3d6d751110fe89285e41d3428c8961f4ff8c970ae`  
		Last Modified: Wed, 23 Mar 2022 20:57:41 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f1da3f8fa8aed1df028de4dbfa4512d40b857dae6a2a67f37a3359059c6c8252
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115822199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4371bb88d2b11615cd2bbf5613374b41164d11cf83b1ea4ddc7560961210c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:49:35 GMT
ADD file:fd7f6da4a48df653ae6dd18e6d5959008daf5ce429845c974982dc7d213342d9 in / 
# Wed, 23 Mar 2022 15:49:35 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:19:47 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:19:48 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:19:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:24:07 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:27:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:27:24 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:27:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:27:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:27:26 GMT
WORKDIR /go
# Thu, 24 Mar 2022 02:26:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 02:26:42 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 02:26:43 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 02:26:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 02:26:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 02:26:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 02:26:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4e012d7cd81aa4570d9d209a75131b32f34a3533d5d449d23fd875513922588e`  
		Last Modified: Wed, 23 Mar 2022 15:51:07 GMT  
		Size: 2.6 MB (2624816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b4a951e94c8a6946a91154ab5ace93adbd78d1ebd435a602fb836ac671efd7`  
		Last Modified: Wed, 23 Mar 2022 19:29:03 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63d00ec81dafe9f0ca510122a4959c5a6a1f1c1acf4be47bf25c3cff6cd4be9`  
		Last Modified: Wed, 23 Mar 2022 19:29:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71824796f74f5fbac9812755baf9bc693e67715490b2b7bf6b83484476796f9c`  
		Last Modified: Wed, 23 Mar 2022 19:32:09 GMT  
		Size: 105.1 MB (105068610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5b249d15fb3bdb66c75a0883f0d10c153c767bb066d86c428791a5478ccb1a`  
		Last Modified: Wed, 23 Mar 2022 19:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0daf81a4e5a849bf96c5aea4c17ac34d6b76e6f4d6de637fdc6b71a37fb17aba`  
		Last Modified: Thu, 24 Mar 2022 02:28:34 GMT  
		Size: 6.7 MB (6677403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd152783b4ba077867dc853a8a18f0a188c9416b1df4a65852513c0199c6e68`  
		Last Modified: Thu, 24 Mar 2022 02:28:32 GMT  
		Size: 1.2 MB (1178511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e80b5acad3274c86d1c575b8370883cbc92a0bcf8f69787011ab5e9ad0309d`  
		Last Modified: Thu, 24 Mar 2022 02:28:31 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:02f8b98f2d7f610839150ec7c8b2cb28303ae5b928a3c46827dba569edcd4cc2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114681140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3173e35645f6e2df7cbb70ab3f0caa9e2e9d580c868b7323cbd4daa9fdf36a95`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:43:55 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:43:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:43:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:48:35 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:51:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:51:52 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:51:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:51:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:51:54 GMT
WORKDIR /go
# Thu, 24 Mar 2022 04:35:30 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 04:35:31 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 04:35:31 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 04:35:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 04:35:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 04:35:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 04:35:35 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331b3631dc9d8ace1881c2cb1c28eb266b0ec19c778721faa865e7bb38223ff6`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 271.1 KB (271107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac904122a78116e4100e90af49a2891c00345dbccfae86db8d59e7eb485212d1`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba6f0fdfa168bee61b63cce8a65b54fc5a493c16656abe13d65fb568c83352f`  
		Last Modified: Wed, 23 Mar 2022 21:39:45 GMT  
		Size: 104.9 MB (104853378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137658965282de05bacdac1471373fd69acaae9418ca2169e043327d833e27ca`  
		Last Modified: Wed, 23 Mar 2022 21:38:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52955aeb924042d48cdbb607de289b7457f6a5d6a0e9739931f61fdfe427f344`  
		Last Modified: Thu, 24 Mar 2022 04:37:20 GMT  
		Size: 6.0 MB (5952171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4014b68d35871bfdbe2e53206c7c5d4ced7c200ae0fcd28605f203330c4bfe1`  
		Last Modified: Thu, 24 Mar 2022 04:37:18 GMT  
		Size: 1.2 MB (1176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fba897ff3f805fe40858af1887544e7fa2e99543c8410fbfb002a3a21ddaf8`  
		Last Modified: Thu, 24 Mar 2022 04:37:18 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:ea3dfbed453c77f5f75be7cb81c2ccee9dce3c65b654e8ef309dfe32b33652e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115485391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15729f70afc23409c5069a96dd3a3a35df28d19c5becc3bdc6dacc7c156a3777`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 08:40:42 GMT
RUN apk add --no-cache ca-certificates
# Thu, 24 Mar 2022 09:03:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Mar 2022 09:03:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 09:05:34 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 24 Mar 2022 09:06:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 24 Mar 2022 09:06:52 GMT
ENV GOPATH=/go
# Thu, 24 Mar 2022 09:06:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 09:06:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 24 Mar 2022 09:06:55 GMT
WORKDIR /go
# Thu, 24 Mar 2022 12:06:47 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 12:06:48 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 12:06:49 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 12:06:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 12:06:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 12:06:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 12:06:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b0b4c4587fbfa6f0755490bb53175932c8f0348926efd629b5e26b281aaa57`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 271.8 KB (271767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bc71a7e8dd1d9668121710be981aa07a74660d94ff3bc08a49ec70e7654c7f`  
		Last Modified: Thu, 24 Mar 2022 09:08:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f22eeb6ec86e713b0a2cb7da0cc984bba811a2fd1d3aef57ac8a509969f9a2e`  
		Last Modified: Thu, 24 Mar 2022 09:09:26 GMT  
		Size: 104.4 MB (104423565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1374803ba168889172986189f9d0d20f5b1491771af58ebe714cb84f99fa3a15`  
		Last Modified: Thu, 24 Mar 2022 09:09:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a9f8667a88f626fef41f02488af5fd79509d422aa4e00fe721fd704c067f87`  
		Last Modified: Thu, 24 Mar 2022 12:07:47 GMT  
		Size: 6.9 MB (6925978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b55c23fcf50b7be62fd87f864eb47347cc2bffb823221798cbfcf40d994fdd`  
		Last Modified: Thu, 24 Mar 2022 12:07:46 GMT  
		Size: 1.1 MB (1148676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d38bff84bce7d7ee9ea1a3bfe3473790a3681d0ecec05d0bdd077af8a567ab1`  
		Last Modified: Thu, 24 Mar 2022 12:07:46 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:11649bbf1cf06ebea3bcef630c8601cc35feaa553ade9923fa62f53c282db438
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114315662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc5080a9dc71d919e80a3f561c2b9af0560976209f3535b1c327b1f26650fff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:57:35 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:57:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:57:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 20:14:48 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 20:17:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 20:17:23 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 20:17:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 20:17:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 20:17:52 GMT
WORKDIR /go
# Thu, 24 Mar 2022 03:31:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 03:31:15 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 03:31:18 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 03:31:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 03:31:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 03:31:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 03:31:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1638cef9b912d53eb425be9e028b98f20521ef09b221e120180e69b238a14321`  
		Last Modified: Wed, 23 Mar 2022 20:19:18 GMT  
		Size: 274.2 KB (274168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611046ca672b25224535bd7440ddf58c8b3f23db1f3b3a079dd7411ea06aafa1`  
		Last Modified: Wed, 23 Mar 2022 20:19:17 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5277b684f884438c817309578480b4bbaf44dec0767ea8c51ceb76bb9b9b60`  
		Last Modified: Wed, 23 Mar 2022 20:19:35 GMT  
		Size: 102.8 MB (102784907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb475fbb9abdc19e3bb6e3ce9caedb03b0cfb03f91dffdc01117daa32d36dfa`  
		Last Modified: Wed, 23 Mar 2022 20:19:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53cb43e7adeb1ac72bd05420bc8de466a4b23f7ef2834419cbbe6f04415022f1`  
		Last Modified: Thu, 24 Mar 2022 03:33:11 GMT  
		Size: 7.3 MB (7320988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c822ff2754104c9cdf880adb708e4dec3d253566eb6e2287220bab202d462abc`  
		Last Modified: Thu, 24 Mar 2022 03:33:09 GMT  
		Size: 1.1 MB (1120846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016dbe0d502dc8e63e4f16f1f7936c74e076cbf990aaea69795c2a56b4c137df`  
		Last Modified: Thu, 24 Mar 2022 03:33:09 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:dfcf236ef9b39bb046ee1f48ecd09d1c7fc7a1f577993d7f7853f55eae3d648b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118748542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e7df7a28241422c766fb3b02badc9125abfd33f30709757ca435b65bc47adb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:03:22 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:03:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:03:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:05:28 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:06:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:06:54 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:06:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:06:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:06:55 GMT
WORKDIR /go
# Wed, 23 Mar 2022 22:22:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 23 Mar 2022 22:22:04 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 23 Mar 2022 22:22:04 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 23 Mar 2022 22:22:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 23 Mar 2022 22:22:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 23 Mar 2022 22:22:05 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 23 Mar 2022 22:22:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332d95e018732d014fb48555d26ed3b1acdc693fa15e5e47a76df80ae10a5fb1`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 272.3 KB (272259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f72ff5871bf659daab8a8511372fe2c96cedb9bcf381d83295e789a93f4b07`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80339d6bea83256c3717aaab67711c55ac89a9bc146b9c891fe826e0462b6b5`  
		Last Modified: Wed, 23 Mar 2022 19:09:18 GMT  
		Size: 107.7 MB (107739195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20716e4f8fc56be1943b49531d073a7a30112a97e9c1772dd2d67f495afab1`  
		Last Modified: Wed, 23 Mar 2022 19:09:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cb1e266fa8a15e2d1a81bc572482e40c95b2db376d37a0935415cb96404132`  
		Last Modified: Wed, 23 Mar 2022 22:23:01 GMT  
		Size: 6.9 MB (6930889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b96c8a99cb7674ba09bf70886a1b327bd8dc19b439c6e828dd8fa8de98261d`  
		Last Modified: Wed, 23 Mar 2022 22:23:01 GMT  
		Size: 1.2 MB (1203789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1572768c5198e65924f57fb4f9008d0847a676367109b9e0d0aad64521b498`  
		Last Modified: Wed, 23 Mar 2022 22:23:00 GMT  
		Size: 403.0 B  
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
$ docker pull caddy@sha256:474b5eb02d1ee6c7eab48839537c44bc6bc701664db7f491a23454df3fec8027
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
$ docker pull caddy@sha256:17b537097b5d9890df1685347555fc90a58886754388088718400f80c30e196d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15279414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a298581a817c0ec3cff52a2efb6b72b25e31dff9934c549531108e9df8c888`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 20:57:08 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 23 Mar 2022 20:57:09 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Wed, 23 Mar 2022 20:57:09 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 23 Mar 2022 20:57:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 23 Mar 2022 20:57:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 20:57:14 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 23 Mar 2022 20:57:14 GMT
ENV XDG_DATA_HOME=/data
# Wed, 23 Mar 2022 20:57:14 GMT
VOLUME [/config]
# Wed, 23 Mar 2022 20:57:14 GMT
VOLUME [/data]
# Wed, 23 Mar 2022 20:57:14 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Wed, 23 Mar 2022 20:57:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 23 Mar 2022 20:57:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 23 Mar 2022 20:57:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 23 Mar 2022 20:57:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 23 Mar 2022 20:57:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 23 Mar 2022 20:57:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 23 Mar 2022 20:57:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 23 Mar 2022 20:57:15 GMT
EXPOSE 80
# Wed, 23 Mar 2022 20:57:15 GMT
EXPOSE 443
# Wed, 23 Mar 2022 20:57:15 GMT
EXPOSE 2019
# Wed, 23 Mar 2022 20:57:15 GMT
WORKDIR /srv
# Wed, 23 Mar 2022 20:57:15 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298eeedc5b642849197ed5163f7464251176a2e9fee965bff79279a7d88aa5b9`  
		Last Modified: Wed, 23 Mar 2022 20:57:55 GMT  
		Size: 291.5 KB (291525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fd06ea5a5b3e64cec5d487772e6f803afc8b87a29760113024fe2888295bf0`  
		Last Modified: Wed, 23 Mar 2022 20:57:54 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad5c614bd5628f34a19de4ba908cf947ce291c06307759a825d85eff67753f1`  
		Last Modified: Wed, 23 Mar 2022 20:57:57 GMT  
		Size: 12.2 MB (12169215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d44cc840206b153d189b0d102bd95a0c86d3ddd98adaf07bc89abee28a8cf7`  
		Last Modified: Wed, 23 Mar 2022 20:57:54 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1` - linux; arm variant v6

```console
$ docker pull caddy@sha256:2f81455d07cabf269db9571065790cf01251f11ebc0209566768e0ed983c0b6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14454131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779c849af631bb3bb0759ad99cdc337390f1032a79cdc5ddb23b2ad65db44ad2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 23 Mar 2022 15:49:35 GMT
ADD file:fd7f6da4a48df653ae6dd18e6d5959008daf5ce429845c974982dc7d213342d9 in / 
# Wed, 23 Mar 2022 15:49:35 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:01:06 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 23 Mar 2022 19:01:08 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Wed, 23 Mar 2022 19:01:08 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 23 Mar 2022 19:01:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 23 Mar 2022 19:01:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:01:15 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 23 Mar 2022 19:01:15 GMT
ENV XDG_DATA_HOME=/data
# Wed, 23 Mar 2022 19:01:16 GMT
VOLUME [/config]
# Wed, 23 Mar 2022 19:01:16 GMT
VOLUME [/data]
# Wed, 23 Mar 2022 19:01:17 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Wed, 23 Mar 2022 19:01:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 23 Mar 2022 19:01:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 23 Mar 2022 19:01:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 23 Mar 2022 19:01:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 23 Mar 2022 19:01:19 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 23 Mar 2022 19:01:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 23 Mar 2022 19:01:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 23 Mar 2022 19:01:20 GMT
EXPOSE 80
# Wed, 23 Mar 2022 19:01:21 GMT
EXPOSE 443
# Wed, 23 Mar 2022 19:01:21 GMT
EXPOSE 2019
# Wed, 23 Mar 2022 19:01:22 GMT
WORKDIR /srv
# Wed, 23 Mar 2022 19:01:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4e012d7cd81aa4570d9d209a75131b32f34a3533d5d449d23fd875513922588e`  
		Last Modified: Wed, 23 Mar 2022 15:51:07 GMT  
		Size: 2.6 MB (2624816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914f120f407c3391e4d6f934335794898779e26d28910ec1b39c9ebf23b779a6`  
		Last Modified: Wed, 23 Mar 2022 19:02:52 GMT  
		Size: 291.7 KB (291694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0923dd4bad3a9af277324fa79a59a3ad1adeeb10ed571e8e39a185f710b9dd`  
		Last Modified: Wed, 23 Mar 2022 19:02:52 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762aade2c36f17eaf9a6830903680eff866ec0d6d64c3498e6b8ba040d61df48`  
		Last Modified: Wed, 23 Mar 2022 19:02:59 GMT  
		Size: 11.5 MB (11531638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2636dad30933abbf86b178d09a172c885d0ab031cf67be5319c3fe85f7c46d`  
		Last Modified: Wed, 23 Mar 2022 19:02:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1` - linux; arm variant v7

```console
$ docker pull caddy@sha256:0d2cc67ebdd2755a07241b03588fb28099e19cbb6844ccfc2d3f74e13709ba1b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14235680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a7ea7449c7db8beb160e2726d10de28073435b7ead459afa0a20e1ff20326b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:40:33 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 23 Mar 2022 19:40:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Wed, 23 Mar 2022 19:40:35 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 23 Mar 2022 19:40:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 23 Mar 2022 19:40:41 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:40:42 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 23 Mar 2022 19:40:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 23 Mar 2022 19:40:42 GMT
VOLUME [/config]
# Wed, 23 Mar 2022 19:40:43 GMT
VOLUME [/data]
# Wed, 23 Mar 2022 19:40:43 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Wed, 23 Mar 2022 19:40:44 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 23 Mar 2022 19:40:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 23 Mar 2022 19:40:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 23 Mar 2022 19:40:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 23 Mar 2022 19:40:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 23 Mar 2022 19:40:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 23 Mar 2022 19:40:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 23 Mar 2022 19:40:46 GMT
EXPOSE 80
# Wed, 23 Mar 2022 19:40:47 GMT
EXPOSE 443
# Wed, 23 Mar 2022 19:40:47 GMT
EXPOSE 2019
# Wed, 23 Mar 2022 19:40:48 GMT
WORKDIR /srv
# Wed, 23 Mar 2022 19:40:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81532be62f77e3aa52dbfe8b2fbf3bbfdedcfd55a16fa5cc6e1a7a55ecb6bfd9`  
		Last Modified: Wed, 23 Mar 2022 19:42:18 GMT  
		Size: 290.7 KB (290660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbe80d47f15656264a0dc1ddf8409aa2d127e129940588a4e53b3e3be6eaebc`  
		Last Modified: Wed, 23 Mar 2022 19:42:17 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb5e80473829e0a7a31cce02ceb86f63b18425e2a431fc34c42826ed4698a1d`  
		Last Modified: Wed, 23 Mar 2022 19:42:24 GMT  
		Size: 11.5 MB (11511977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aea8e3a25585a05d92ce8afcd476c1b10f0b2f6680c3f46aa7e3ae88fd1615b`  
		Last Modified: Wed, 23 Mar 2022 19:42:17 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:2964a0433893b411b04d9e61cbcd02d9b985761a978eb27e6673800ae1c79384
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14149918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd15d6d7970c54489bb92b5a28bfb390b3dc08be4a6f923281cca4a935823b0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 05:03:31 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 24 Mar 2022 05:03:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 24 Mar 2022 05:03:34 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 24 Mar 2022 05:03:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 24 Mar 2022 05:03:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Mar 2022 05:03:38 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 24 Mar 2022 05:03:39 GMT
ENV XDG_DATA_HOME=/data
# Thu, 24 Mar 2022 05:03:40 GMT
VOLUME [/config]
# Thu, 24 Mar 2022 05:03:41 GMT
VOLUME [/data]
# Thu, 24 Mar 2022 05:03:42 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Thu, 24 Mar 2022 05:03:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 24 Mar 2022 05:03:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 24 Mar 2022 05:03:45 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 24 Mar 2022 05:03:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 24 Mar 2022 05:03:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 24 Mar 2022 05:03:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Mar 2022 05:03:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 24 Mar 2022 05:03:50 GMT
EXPOSE 80
# Thu, 24 Mar 2022 05:03:51 GMT
EXPOSE 443
# Thu, 24 Mar 2022 05:03:52 GMT
EXPOSE 2019
# Thu, 24 Mar 2022 05:03:53 GMT
WORKDIR /srv
# Thu, 24 Mar 2022 05:03:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73538784ebea742009c3b6faa09832bf078a7c06369c1267d26f304313bbbca`  
		Last Modified: Thu, 24 Mar 2022 05:04:38 GMT  
		Size: 291.3 KB (291299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30be15f341c17956a237ff6b02ecd3ac81e31878b626c5417701567deefbbc3d`  
		Last Modified: Thu, 24 Mar 2022 05:04:38 GMT  
		Size: 5.8 KB (5751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df84a84149a43695c428691b884500744e0b4aad01690336fb987c7b7f278abc`  
		Last Modified: Thu, 24 Mar 2022 05:04:40 GMT  
		Size: 11.1 MB (11137995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d36676e4149bdc15be1e26e7b7d7ca8f990981f54db804ae46d326f3aec0d5`  
		Last Modified: Thu, 24 Mar 2022 05:04:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1` - linux; ppc64le

```console
$ docker pull caddy@sha256:26a663fd52bd24f4dd204a9a1448b717b1732462fbeb304083d4a6c90d391cee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13789396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d0391b067cd7ccf2237bb995bfdb775b5289e937c44ebe8569839391c1cf282`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:31:12 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 23 Mar 2022 19:31:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Wed, 23 Mar 2022 19:31:25 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 23 Mar 2022 19:31:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 23 Mar 2022 19:31:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:31:54 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 23 Mar 2022 19:31:56 GMT
ENV XDG_DATA_HOME=/data
# Wed, 23 Mar 2022 19:31:58 GMT
VOLUME [/config]
# Wed, 23 Mar 2022 19:32:01 GMT
VOLUME [/data]
# Wed, 23 Mar 2022 19:32:07 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Wed, 23 Mar 2022 19:32:10 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 23 Mar 2022 19:32:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 23 Mar 2022 19:32:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 23 Mar 2022 19:32:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 23 Mar 2022 19:32:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 23 Mar 2022 19:32:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 23 Mar 2022 19:32:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 23 Mar 2022 19:32:34 GMT
EXPOSE 80
# Wed, 23 Mar 2022 19:32:38 GMT
EXPOSE 443
# Wed, 23 Mar 2022 19:32:42 GMT
EXPOSE 2019
# Wed, 23 Mar 2022 19:32:46 GMT
WORKDIR /srv
# Wed, 23 Mar 2022 19:32:51 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5a9e090743ab1d7208564ff31dd14cd4da34c81fb55b89e600769334b95687`  
		Last Modified: Wed, 23 Mar 2022 19:33:55 GMT  
		Size: 293.7 KB (293716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58058db3aeed598e9733beb18343a1a0bc4a2ceb5e2cd25fc4b449ae9b4d4d4`  
		Last Modified: Wed, 23 Mar 2022 19:33:54 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce132a6ce3d7e7b3f4e411d42c248db749460939842f613df4e03cc5fef68b50`  
		Last Modified: Wed, 23 Mar 2022 19:33:57 GMT  
		Size: 10.7 MB (10675662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8873dd15e77a76e5539ca5dd68d1428bd95b634e78e8c6aa06524428f7612ed4`  
		Last Modified: Wed, 23 Mar 2022 19:33:54 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1` - linux; s390x

```console
$ docker pull caddy@sha256:5a3017be8c1e8852ab662902a32084fcab34d7a6bfd1256fee311d8f2178a5b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14628982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c662bb43b9a175380a39f841ecb158b708d817aa2ccd07cfe04ac051e4d73901`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 18:47:24 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 23 Mar 2022 18:47:25 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Wed, 23 Mar 2022 18:47:25 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 23 Mar 2022 18:47:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 23 Mar 2022 18:47:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 18:47:28 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 23 Mar 2022 18:47:28 GMT
ENV XDG_DATA_HOME=/data
# Wed, 23 Mar 2022 18:47:29 GMT
VOLUME [/config]
# Wed, 23 Mar 2022 18:47:29 GMT
VOLUME [/data]
# Wed, 23 Mar 2022 18:47:29 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Wed, 23 Mar 2022 18:47:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 23 Mar 2022 18:47:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 23 Mar 2022 18:47:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 23 Mar 2022 18:47:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 23 Mar 2022 18:47:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 23 Mar 2022 18:47:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 23 Mar 2022 18:47:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 23 Mar 2022 18:47:30 GMT
EXPOSE 80
# Wed, 23 Mar 2022 18:47:30 GMT
EXPOSE 443
# Wed, 23 Mar 2022 18:47:30 GMT
EXPOSE 2019
# Wed, 23 Mar 2022 18:47:30 GMT
WORKDIR /srv
# Wed, 23 Mar 2022 18:47:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8855943d0cd2803c436adcf2c0a4eb120c432bb722098dc05e312068eeae6458`  
		Last Modified: Wed, 23 Mar 2022 18:48:22 GMT  
		Size: 291.8 KB (291819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577987fc87892897c8faebcb11dea9a58ee4d0a1243c9937e838bd38e00e7967`  
		Last Modified: Wed, 23 Mar 2022 18:48:21 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f25b14d452f12d95d36954dcb8242c76f2dc1c0a55b63d538768ffd9e70d0a`  
		Last Modified: Wed, 23 Mar 2022 18:48:23 GMT  
		Size: 11.7 MB (11729482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d156a4ecb638b0238fff59c78abe59feeb567fca4e594900e8e53d3d67d33a`  
		Last Modified: Wed, 23 Mar 2022 18:48:21 GMT  
		Size: 154.0 B  
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
$ docker pull caddy@sha256:fc4949821de4a1f9543769abd6463ec4da3be92d2bb3806def5000f1583ed093
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
$ docker pull caddy@sha256:17b537097b5d9890df1685347555fc90a58886754388088718400f80c30e196d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15279414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a298581a817c0ec3cff52a2efb6b72b25e31dff9934c549531108e9df8c888`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 20:57:08 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 23 Mar 2022 20:57:09 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Wed, 23 Mar 2022 20:57:09 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 23 Mar 2022 20:57:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 23 Mar 2022 20:57:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 20:57:14 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 23 Mar 2022 20:57:14 GMT
ENV XDG_DATA_HOME=/data
# Wed, 23 Mar 2022 20:57:14 GMT
VOLUME [/config]
# Wed, 23 Mar 2022 20:57:14 GMT
VOLUME [/data]
# Wed, 23 Mar 2022 20:57:14 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Wed, 23 Mar 2022 20:57:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 23 Mar 2022 20:57:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 23 Mar 2022 20:57:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 23 Mar 2022 20:57:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 23 Mar 2022 20:57:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 23 Mar 2022 20:57:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 23 Mar 2022 20:57:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 23 Mar 2022 20:57:15 GMT
EXPOSE 80
# Wed, 23 Mar 2022 20:57:15 GMT
EXPOSE 443
# Wed, 23 Mar 2022 20:57:15 GMT
EXPOSE 2019
# Wed, 23 Mar 2022 20:57:15 GMT
WORKDIR /srv
# Wed, 23 Mar 2022 20:57:15 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298eeedc5b642849197ed5163f7464251176a2e9fee965bff79279a7d88aa5b9`  
		Last Modified: Wed, 23 Mar 2022 20:57:55 GMT  
		Size: 291.5 KB (291525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fd06ea5a5b3e64cec5d487772e6f803afc8b87a29760113024fe2888295bf0`  
		Last Modified: Wed, 23 Mar 2022 20:57:54 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad5c614bd5628f34a19de4ba908cf947ce291c06307759a825d85eff67753f1`  
		Last Modified: Wed, 23 Mar 2022 20:57:57 GMT  
		Size: 12.2 MB (12169215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d44cc840206b153d189b0d102bd95a0c86d3ddd98adaf07bc89abee28a8cf7`  
		Last Modified: Wed, 23 Mar 2022 20:57:54 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:2f81455d07cabf269db9571065790cf01251f11ebc0209566768e0ed983c0b6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14454131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779c849af631bb3bb0759ad99cdc337390f1032a79cdc5ddb23b2ad65db44ad2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 23 Mar 2022 15:49:35 GMT
ADD file:fd7f6da4a48df653ae6dd18e6d5959008daf5ce429845c974982dc7d213342d9 in / 
# Wed, 23 Mar 2022 15:49:35 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:01:06 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 23 Mar 2022 19:01:08 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Wed, 23 Mar 2022 19:01:08 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 23 Mar 2022 19:01:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 23 Mar 2022 19:01:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:01:15 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 23 Mar 2022 19:01:15 GMT
ENV XDG_DATA_HOME=/data
# Wed, 23 Mar 2022 19:01:16 GMT
VOLUME [/config]
# Wed, 23 Mar 2022 19:01:16 GMT
VOLUME [/data]
# Wed, 23 Mar 2022 19:01:17 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Wed, 23 Mar 2022 19:01:17 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 23 Mar 2022 19:01:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 23 Mar 2022 19:01:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 23 Mar 2022 19:01:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 23 Mar 2022 19:01:19 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 23 Mar 2022 19:01:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 23 Mar 2022 19:01:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 23 Mar 2022 19:01:20 GMT
EXPOSE 80
# Wed, 23 Mar 2022 19:01:21 GMT
EXPOSE 443
# Wed, 23 Mar 2022 19:01:21 GMT
EXPOSE 2019
# Wed, 23 Mar 2022 19:01:22 GMT
WORKDIR /srv
# Wed, 23 Mar 2022 19:01:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4e012d7cd81aa4570d9d209a75131b32f34a3533d5d449d23fd875513922588e`  
		Last Modified: Wed, 23 Mar 2022 15:51:07 GMT  
		Size: 2.6 MB (2624816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914f120f407c3391e4d6f934335794898779e26d28910ec1b39c9ebf23b779a6`  
		Last Modified: Wed, 23 Mar 2022 19:02:52 GMT  
		Size: 291.7 KB (291694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0923dd4bad3a9af277324fa79a59a3ad1adeeb10ed571e8e39a185f710b9dd`  
		Last Modified: Wed, 23 Mar 2022 19:02:52 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762aade2c36f17eaf9a6830903680eff866ec0d6d64c3498e6b8ba040d61df48`  
		Last Modified: Wed, 23 Mar 2022 19:02:59 GMT  
		Size: 11.5 MB (11531638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2636dad30933abbf86b178d09a172c885d0ab031cf67be5319c3fe85f7c46d`  
		Last Modified: Wed, 23 Mar 2022 19:02:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:0d2cc67ebdd2755a07241b03588fb28099e19cbb6844ccfc2d3f74e13709ba1b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14235680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a7ea7449c7db8beb160e2726d10de28073435b7ead459afa0a20e1ff20326b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:40:33 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 23 Mar 2022 19:40:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Wed, 23 Mar 2022 19:40:35 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 23 Mar 2022 19:40:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 23 Mar 2022 19:40:41 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:40:42 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 23 Mar 2022 19:40:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 23 Mar 2022 19:40:42 GMT
VOLUME [/config]
# Wed, 23 Mar 2022 19:40:43 GMT
VOLUME [/data]
# Wed, 23 Mar 2022 19:40:43 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Wed, 23 Mar 2022 19:40:44 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 23 Mar 2022 19:40:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 23 Mar 2022 19:40:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 23 Mar 2022 19:40:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 23 Mar 2022 19:40:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 23 Mar 2022 19:40:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 23 Mar 2022 19:40:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 23 Mar 2022 19:40:46 GMT
EXPOSE 80
# Wed, 23 Mar 2022 19:40:47 GMT
EXPOSE 443
# Wed, 23 Mar 2022 19:40:47 GMT
EXPOSE 2019
# Wed, 23 Mar 2022 19:40:48 GMT
WORKDIR /srv
# Wed, 23 Mar 2022 19:40:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81532be62f77e3aa52dbfe8b2fbf3bbfdedcfd55a16fa5cc6e1a7a55ecb6bfd9`  
		Last Modified: Wed, 23 Mar 2022 19:42:18 GMT  
		Size: 290.7 KB (290660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbe80d47f15656264a0dc1ddf8409aa2d127e129940588a4e53b3e3be6eaebc`  
		Last Modified: Wed, 23 Mar 2022 19:42:17 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb5e80473829e0a7a31cce02ceb86f63b18425e2a431fc34c42826ed4698a1d`  
		Last Modified: Wed, 23 Mar 2022 19:42:24 GMT  
		Size: 11.5 MB (11511977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aea8e3a25585a05d92ce8afcd476c1b10f0b2f6680c3f46aa7e3ae88fd1615b`  
		Last Modified: Wed, 23 Mar 2022 19:42:17 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:2964a0433893b411b04d9e61cbcd02d9b985761a978eb27e6673800ae1c79384
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14149918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd15d6d7970c54489bb92b5a28bfb390b3dc08be4a6f923281cca4a935823b0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 05:03:31 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 24 Mar 2022 05:03:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 24 Mar 2022 05:03:34 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 24 Mar 2022 05:03:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 24 Mar 2022 05:03:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Mar 2022 05:03:38 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 24 Mar 2022 05:03:39 GMT
ENV XDG_DATA_HOME=/data
# Thu, 24 Mar 2022 05:03:40 GMT
VOLUME [/config]
# Thu, 24 Mar 2022 05:03:41 GMT
VOLUME [/data]
# Thu, 24 Mar 2022 05:03:42 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Thu, 24 Mar 2022 05:03:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 24 Mar 2022 05:03:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 24 Mar 2022 05:03:45 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 24 Mar 2022 05:03:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 24 Mar 2022 05:03:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 24 Mar 2022 05:03:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Mar 2022 05:03:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 24 Mar 2022 05:03:50 GMT
EXPOSE 80
# Thu, 24 Mar 2022 05:03:51 GMT
EXPOSE 443
# Thu, 24 Mar 2022 05:03:52 GMT
EXPOSE 2019
# Thu, 24 Mar 2022 05:03:53 GMT
WORKDIR /srv
# Thu, 24 Mar 2022 05:03:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73538784ebea742009c3b6faa09832bf078a7c06369c1267d26f304313bbbca`  
		Last Modified: Thu, 24 Mar 2022 05:04:38 GMT  
		Size: 291.3 KB (291299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30be15f341c17956a237ff6b02ecd3ac81e31878b626c5417701567deefbbc3d`  
		Last Modified: Thu, 24 Mar 2022 05:04:38 GMT  
		Size: 5.8 KB (5751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df84a84149a43695c428691b884500744e0b4aad01690336fb987c7b7f278abc`  
		Last Modified: Thu, 24 Mar 2022 05:04:40 GMT  
		Size: 11.1 MB (11137995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d36676e4149bdc15be1e26e7b7d7ca8f990981f54db804ae46d326f3aec0d5`  
		Last Modified: Thu, 24 Mar 2022 05:04:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:26a663fd52bd24f4dd204a9a1448b717b1732462fbeb304083d4a6c90d391cee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13789396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d0391b067cd7ccf2237bb995bfdb775b5289e937c44ebe8569839391c1cf282`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:31:12 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 23 Mar 2022 19:31:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Wed, 23 Mar 2022 19:31:25 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 23 Mar 2022 19:31:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 23 Mar 2022 19:31:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:31:54 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 23 Mar 2022 19:31:56 GMT
ENV XDG_DATA_HOME=/data
# Wed, 23 Mar 2022 19:31:58 GMT
VOLUME [/config]
# Wed, 23 Mar 2022 19:32:01 GMT
VOLUME [/data]
# Wed, 23 Mar 2022 19:32:07 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Wed, 23 Mar 2022 19:32:10 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 23 Mar 2022 19:32:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 23 Mar 2022 19:32:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 23 Mar 2022 19:32:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 23 Mar 2022 19:32:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 23 Mar 2022 19:32:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 23 Mar 2022 19:32:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 23 Mar 2022 19:32:34 GMT
EXPOSE 80
# Wed, 23 Mar 2022 19:32:38 GMT
EXPOSE 443
# Wed, 23 Mar 2022 19:32:42 GMT
EXPOSE 2019
# Wed, 23 Mar 2022 19:32:46 GMT
WORKDIR /srv
# Wed, 23 Mar 2022 19:32:51 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5a9e090743ab1d7208564ff31dd14cd4da34c81fb55b89e600769334b95687`  
		Last Modified: Wed, 23 Mar 2022 19:33:55 GMT  
		Size: 293.7 KB (293716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58058db3aeed598e9733beb18343a1a0bc4a2ceb5e2cd25fc4b449ae9b4d4d4`  
		Last Modified: Wed, 23 Mar 2022 19:33:54 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce132a6ce3d7e7b3f4e411d42c248db749460939842f613df4e03cc5fef68b50`  
		Last Modified: Wed, 23 Mar 2022 19:33:57 GMT  
		Size: 10.7 MB (10675662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8873dd15e77a76e5539ca5dd68d1428bd95b634e78e8c6aa06524428f7612ed4`  
		Last Modified: Wed, 23 Mar 2022 19:33:54 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:5a3017be8c1e8852ab662902a32084fcab34d7a6bfd1256fee311d8f2178a5b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14628982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c662bb43b9a175380a39f841ecb158b708d817aa2ccd07cfe04ac051e4d73901`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 18:47:24 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 23 Mar 2022 18:47:25 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Wed, 23 Mar 2022 18:47:25 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 23 Mar 2022 18:47:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 23 Mar 2022 18:47:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 18:47:28 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 23 Mar 2022 18:47:28 GMT
ENV XDG_DATA_HOME=/data
# Wed, 23 Mar 2022 18:47:29 GMT
VOLUME [/config]
# Wed, 23 Mar 2022 18:47:29 GMT
VOLUME [/data]
# Wed, 23 Mar 2022 18:47:29 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Wed, 23 Mar 2022 18:47:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 23 Mar 2022 18:47:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 23 Mar 2022 18:47:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 23 Mar 2022 18:47:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 23 Mar 2022 18:47:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 23 Mar 2022 18:47:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 23 Mar 2022 18:47:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 23 Mar 2022 18:47:30 GMT
EXPOSE 80
# Wed, 23 Mar 2022 18:47:30 GMT
EXPOSE 443
# Wed, 23 Mar 2022 18:47:30 GMT
EXPOSE 2019
# Wed, 23 Mar 2022 18:47:30 GMT
WORKDIR /srv
# Wed, 23 Mar 2022 18:47:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8855943d0cd2803c436adcf2c0a4eb120c432bb722098dc05e312068eeae6458`  
		Last Modified: Wed, 23 Mar 2022 18:48:22 GMT  
		Size: 291.8 KB (291819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577987fc87892897c8faebcb11dea9a58ee4d0a1243c9937e838bd38e00e7967`  
		Last Modified: Wed, 23 Mar 2022 18:48:21 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f25b14d452f12d95d36954dcb8242c76f2dc1c0a55b63d538768ffd9e70d0a`  
		Last Modified: Wed, 23 Mar 2022 18:48:23 GMT  
		Size: 11.7 MB (11729482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d156a4ecb638b0238fff59c78abe59feeb567fca4e594900e8e53d3d67d33a`  
		Last Modified: Wed, 23 Mar 2022 18:48:21 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-beta.1-builder`

```console
$ docker pull caddy@sha256:a031939a82f0a8fb14ca499072e34b48ed6e4ab976cd55e9a4c99f80f72c99c9
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
$ docker pull caddy@sha256:449c17c757c809d2d70c6ee278e9fbe0af5a498ffbdc750d5c5fb47d1fa0e788
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121339144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58feeae1ebacc72bc5b0d749c53960ed173d91a9804db434e61f7618acebbbf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 17:33:52 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 17:47:17 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 17:47:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:49:48 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 17:51:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 17:51:49 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 17:51:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:51:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 17:51:50 GMT
WORKDIR /go
# Wed, 23 Mar 2022 20:57:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 23 Mar 2022 20:57:03 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 23 Mar 2022 20:57:19 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 23 Mar 2022 20:57:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 23 Mar 2022 20:57:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 23 Mar 2022 20:57:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 23 Mar 2022 20:57:20 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ae170c2a8ceb6dfe7dd52edb58d7be5583518415f0e441c5b7d4f0f8bad244`  
		Last Modified: Wed, 23 Mar 2022 17:34:04 GMT  
		Size: 272.0 KB (271973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb35b180f41941e8ec9af85110ff412f204e4afaf593ac8fc601c07b7449304d`  
		Last Modified: Wed, 23 Mar 2022 17:52:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367011ddbc177b50e507d24a640d8fdbdd64a32a4b0e2a3549ad26a1c0581da5`  
		Last Modified: Wed, 23 Mar 2022 17:53:41 GMT  
		Size: 110.2 MB (110186567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318840287a8912b4d3a5caf13e21932dd668cfa441f84c3f7cb89884f12bc498`  
		Last Modified: Wed, 23 Mar 2022 17:53:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c39dbaf7c7b7fee5c862d4a01ade30b6cc7ab1640f4d9768f164f020ebb0df`  
		Last Modified: Wed, 23 Mar 2022 20:57:42 GMT  
		Size: 6.8 MB (6821487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d185a70589c07012e7bc82ffd94e082db699e78368161203b4fc3b224cfe2a4`  
		Last Modified: Wed, 23 Mar 2022 20:58:04 GMT  
		Size: 1.2 MB (1245715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3cd6fce2802865a8b64aca3bbbc99b878b27adfe49d92dd2a3d71a56e4ae35`  
		Last Modified: Wed, 23 Mar 2022 20:58:03 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:0aa1f5643052d2b748df91b1b644a7a784565407bbd9d3d2779cfece919c1c3d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115822194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91ba87cbff05ceb317b4ac864cc97903a3c874eed274b191fa5cf67c8204342`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:49:35 GMT
ADD file:fd7f6da4a48df653ae6dd18e6d5959008daf5ce429845c974982dc7d213342d9 in / 
# Wed, 23 Mar 2022 15:49:35 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:19:47 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:19:48 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:19:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:24:07 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:27:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:27:24 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:27:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:27:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:27:26 GMT
WORKDIR /go
# Thu, 24 Mar 2022 02:26:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 02:26:42 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 02:27:11 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 24 Mar 2022 02:27:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 02:27:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 02:27:14 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 02:27:14 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4e012d7cd81aa4570d9d209a75131b32f34a3533d5d449d23fd875513922588e`  
		Last Modified: Wed, 23 Mar 2022 15:51:07 GMT  
		Size: 2.6 MB (2624816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b4a951e94c8a6946a91154ab5ace93adbd78d1ebd435a602fb836ac671efd7`  
		Last Modified: Wed, 23 Mar 2022 19:29:03 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63d00ec81dafe9f0ca510122a4959c5a6a1f1c1acf4be47bf25c3cff6cd4be9`  
		Last Modified: Wed, 23 Mar 2022 19:29:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71824796f74f5fbac9812755baf9bc693e67715490b2b7bf6b83484476796f9c`  
		Last Modified: Wed, 23 Mar 2022 19:32:09 GMT  
		Size: 105.1 MB (105068610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5b249d15fb3bdb66c75a0883f0d10c153c767bb066d86c428791a5478ccb1a`  
		Last Modified: Wed, 23 Mar 2022 19:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0daf81a4e5a849bf96c5aea4c17ac34d6b76e6f4d6de637fdc6b71a37fb17aba`  
		Last Modified: Thu, 24 Mar 2022 02:28:34 GMT  
		Size: 6.7 MB (6677403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee04b08f8d6e6c142ea1315cb5af3d4e1128993694ecbc844cf8142701e77cc`  
		Last Modified: Thu, 24 Mar 2022 02:28:53 GMT  
		Size: 1.2 MB (1178504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56110c558a09687d4b1566c4c5f063c9207ccab44ab0810d3e4e189d46c7983`  
		Last Modified: Thu, 24 Mar 2022 02:28:51 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ecbc10f3f810710b018049c60fc8e6eee68603d6e143125d52c698049bfe4ab4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114681142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422a80d5b1020e2f6ea922c1ee34808bfc55b24c0a0ca63811e610bd56c7c31d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:43:55 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:43:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:43:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:48:35 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:51:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:51:52 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:51:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:51:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:51:54 GMT
WORKDIR /go
# Thu, 24 Mar 2022 04:35:30 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 04:35:31 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 04:36:00 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 24 Mar 2022 04:36:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 04:36:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 04:36:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 04:36:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331b3631dc9d8ace1881c2cb1c28eb266b0ec19c778721faa865e7bb38223ff6`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 271.1 KB (271107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac904122a78116e4100e90af49a2891c00345dbccfae86db8d59e7eb485212d1`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba6f0fdfa168bee61b63cce8a65b54fc5a493c16656abe13d65fb568c83352f`  
		Last Modified: Wed, 23 Mar 2022 21:39:45 GMT  
		Size: 104.9 MB (104853378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137658965282de05bacdac1471373fd69acaae9418ca2169e043327d833e27ca`  
		Last Modified: Wed, 23 Mar 2022 21:38:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52955aeb924042d48cdbb607de289b7457f6a5d6a0e9739931f61fdfe427f344`  
		Last Modified: Thu, 24 Mar 2022 04:37:20 GMT  
		Size: 6.0 MB (5952171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e57ba208689f1e427c40a667a2cbf3edb416f56bcb0ccd9acf9d92ff64cf7ec`  
		Last Modified: Thu, 24 Mar 2022 04:37:37 GMT  
		Size: 1.2 MB (1176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c01f8f1215d9923669ae5bfd5ff09d671cc335546f613cb8dc65185fce8f4d9`  
		Last Modified: Thu, 24 Mar 2022 04:37:36 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:e03d21b158b53739152a61e319318968c01bb7f87b7b2ca75b4dfa81eebc14e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115485391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298230d91553e6791cd20293b4590be6d4c1f50bae2c1d1a73828b2f37963ff0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 08:40:42 GMT
RUN apk add --no-cache ca-certificates
# Thu, 24 Mar 2022 09:03:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Mar 2022 09:03:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 09:05:34 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 24 Mar 2022 09:06:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 24 Mar 2022 09:06:52 GMT
ENV GOPATH=/go
# Thu, 24 Mar 2022 09:06:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 09:06:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 24 Mar 2022 09:06:55 GMT
WORKDIR /go
# Thu, 24 Mar 2022 12:06:47 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 12:06:48 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 12:07:05 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 24 Mar 2022 12:07:06 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 12:07:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 12:07:09 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 12:07:09 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b0b4c4587fbfa6f0755490bb53175932c8f0348926efd629b5e26b281aaa57`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 271.8 KB (271767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bc71a7e8dd1d9668121710be981aa07a74660d94ff3bc08a49ec70e7654c7f`  
		Last Modified: Thu, 24 Mar 2022 09:08:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f22eeb6ec86e713b0a2cb7da0cc984bba811a2fd1d3aef57ac8a509969f9a2e`  
		Last Modified: Thu, 24 Mar 2022 09:09:26 GMT  
		Size: 104.4 MB (104423565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1374803ba168889172986189f9d0d20f5b1491771af58ebe714cb84f99fa3a15`  
		Last Modified: Thu, 24 Mar 2022 09:09:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a9f8667a88f626fef41f02488af5fd79509d422aa4e00fe721fd704c067f87`  
		Last Modified: Thu, 24 Mar 2022 12:07:47 GMT  
		Size: 6.9 MB (6925978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc1f36fe97759a3c941c9bbb783a066a205d6a7641df288c8e398cf745c0adf`  
		Last Modified: Thu, 24 Mar 2022 12:08:01 GMT  
		Size: 1.1 MB (1148676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42056a5405a9966a5c1873220813b7c5dfd11720c840128f601dd8591eb0871`  
		Last Modified: Thu, 24 Mar 2022 12:08:01 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:e483074a29e546b36e2203bf14bb58c153e5ff44e11e808abdfab6fa82e461c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114315661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:944022d2960c692dc7335ab921050060ff9f7023e99a428263163792fc7c81ff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:57:35 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:57:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:57:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 20:14:48 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 20:17:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 20:17:23 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 20:17:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 20:17:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 20:17:52 GMT
WORKDIR /go
# Thu, 24 Mar 2022 03:31:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 03:31:15 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 03:32:03 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 24 Mar 2022 03:32:09 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 03:32:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 03:32:18 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 03:32:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1638cef9b912d53eb425be9e028b98f20521ef09b221e120180e69b238a14321`  
		Last Modified: Wed, 23 Mar 2022 20:19:18 GMT  
		Size: 274.2 KB (274168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611046ca672b25224535bd7440ddf58c8b3f23db1f3b3a079dd7411ea06aafa1`  
		Last Modified: Wed, 23 Mar 2022 20:19:17 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5277b684f884438c817309578480b4bbaf44dec0767ea8c51ceb76bb9b9b60`  
		Last Modified: Wed, 23 Mar 2022 20:19:35 GMT  
		Size: 102.8 MB (102784907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb475fbb9abdc19e3bb6e3ce9caedb03b0cfb03f91dffdc01117daa32d36dfa`  
		Last Modified: Wed, 23 Mar 2022 20:19:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53cb43e7adeb1ac72bd05420bc8de466a4b23f7ef2834419cbbe6f04415022f1`  
		Last Modified: Thu, 24 Mar 2022 03:33:11 GMT  
		Size: 7.3 MB (7320988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be52f569cec212bde962ac7e9b67f50a0939d936c96865cea5e497eb040db36`  
		Last Modified: Thu, 24 Mar 2022 03:33:29 GMT  
		Size: 1.1 MB (1120845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b792fe773414624529314bb651b4cb7e8ec707a5be98b213dc5c2a52bd2a5`  
		Last Modified: Thu, 24 Mar 2022 03:33:29 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder` - linux; s390x

```console
$ docker pull caddy@sha256:60e293a1beb396dac5ddeca98fe7f194f70e8b7bf1b535d7c2681d4c4e9b6d1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118748535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b90d3c913d4b2c1b3677c3d297e12ff63b20561cca0a1120253b1bce0d9414e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:03:22 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:03:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:03:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:05:28 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:06:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:06:54 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:06:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:06:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:06:55 GMT
WORKDIR /go
# Wed, 23 Mar 2022 22:22:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 23 Mar 2022 22:22:04 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 23 Mar 2022 22:22:18 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 23 Mar 2022 22:22:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 23 Mar 2022 22:22:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 23 Mar 2022 22:22:19 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 23 Mar 2022 22:22:20 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332d95e018732d014fb48555d26ed3b1acdc693fa15e5e47a76df80ae10a5fb1`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 272.3 KB (272259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f72ff5871bf659daab8a8511372fe2c96cedb9bcf381d83295e789a93f4b07`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80339d6bea83256c3717aaab67711c55ac89a9bc146b9c891fe826e0462b6b5`  
		Last Modified: Wed, 23 Mar 2022 19:09:18 GMT  
		Size: 107.7 MB (107739195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20716e4f8fc56be1943b49531d073a7a30112a97e9c1772dd2d67f495afab1`  
		Last Modified: Wed, 23 Mar 2022 19:09:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cb1e266fa8a15e2d1a81bc572482e40c95b2db376d37a0935415cb96404132`  
		Last Modified: Wed, 23 Mar 2022 22:23:01 GMT  
		Size: 6.9 MB (6930889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38005ba0732ecf7fa5f1ab285724f8283369616bb88bfe66ae4cd4545ab98429`  
		Last Modified: Wed, 23 Mar 2022 22:23:17 GMT  
		Size: 1.2 MB (1203782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e08e3235979b535ee78a676613109e9ce8a5d43366ef9353d38047ccf533df`  
		Last Modified: Wed, 23 Mar 2022 22:23:17 GMT  
		Size: 403.0 B  
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
$ docker pull caddy@sha256:da558afcc53aea76252c1413558dfae594aac92121d40f9d4fc6ee03acabec90
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
$ docker pull caddy@sha256:449c17c757c809d2d70c6ee278e9fbe0af5a498ffbdc750d5c5fb47d1fa0e788
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121339144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58feeae1ebacc72bc5b0d749c53960ed173d91a9804db434e61f7618acebbbf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 17:33:52 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 17:47:17 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 17:47:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:49:48 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 17:51:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 17:51:49 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 17:51:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:51:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 17:51:50 GMT
WORKDIR /go
# Wed, 23 Mar 2022 20:57:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 23 Mar 2022 20:57:03 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 23 Mar 2022 20:57:19 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 23 Mar 2022 20:57:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 23 Mar 2022 20:57:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 23 Mar 2022 20:57:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 23 Mar 2022 20:57:20 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ae170c2a8ceb6dfe7dd52edb58d7be5583518415f0e441c5b7d4f0f8bad244`  
		Last Modified: Wed, 23 Mar 2022 17:34:04 GMT  
		Size: 272.0 KB (271973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb35b180f41941e8ec9af85110ff412f204e4afaf593ac8fc601c07b7449304d`  
		Last Modified: Wed, 23 Mar 2022 17:52:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367011ddbc177b50e507d24a640d8fdbdd64a32a4b0e2a3549ad26a1c0581da5`  
		Last Modified: Wed, 23 Mar 2022 17:53:41 GMT  
		Size: 110.2 MB (110186567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318840287a8912b4d3a5caf13e21932dd668cfa441f84c3f7cb89884f12bc498`  
		Last Modified: Wed, 23 Mar 2022 17:53:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c39dbaf7c7b7fee5c862d4a01ade30b6cc7ab1640f4d9768f164f020ebb0df`  
		Last Modified: Wed, 23 Mar 2022 20:57:42 GMT  
		Size: 6.8 MB (6821487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d185a70589c07012e7bc82ffd94e082db699e78368161203b4fc3b224cfe2a4`  
		Last Modified: Wed, 23 Mar 2022 20:58:04 GMT  
		Size: 1.2 MB (1245715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3cd6fce2802865a8b64aca3bbbc99b878b27adfe49d92dd2a3d71a56e4ae35`  
		Last Modified: Wed, 23 Mar 2022 20:58:03 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:0aa1f5643052d2b748df91b1b644a7a784565407bbd9d3d2779cfece919c1c3d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115822194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91ba87cbff05ceb317b4ac864cc97903a3c874eed274b191fa5cf67c8204342`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:49:35 GMT
ADD file:fd7f6da4a48df653ae6dd18e6d5959008daf5ce429845c974982dc7d213342d9 in / 
# Wed, 23 Mar 2022 15:49:35 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:19:47 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:19:48 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:19:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:24:07 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:27:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:27:24 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:27:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:27:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:27:26 GMT
WORKDIR /go
# Thu, 24 Mar 2022 02:26:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 02:26:42 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 02:27:11 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 24 Mar 2022 02:27:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 02:27:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 02:27:14 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 02:27:14 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4e012d7cd81aa4570d9d209a75131b32f34a3533d5d449d23fd875513922588e`  
		Last Modified: Wed, 23 Mar 2022 15:51:07 GMT  
		Size: 2.6 MB (2624816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b4a951e94c8a6946a91154ab5ace93adbd78d1ebd435a602fb836ac671efd7`  
		Last Modified: Wed, 23 Mar 2022 19:29:03 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63d00ec81dafe9f0ca510122a4959c5a6a1f1c1acf4be47bf25c3cff6cd4be9`  
		Last Modified: Wed, 23 Mar 2022 19:29:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71824796f74f5fbac9812755baf9bc693e67715490b2b7bf6b83484476796f9c`  
		Last Modified: Wed, 23 Mar 2022 19:32:09 GMT  
		Size: 105.1 MB (105068610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5b249d15fb3bdb66c75a0883f0d10c153c767bb066d86c428791a5478ccb1a`  
		Last Modified: Wed, 23 Mar 2022 19:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0daf81a4e5a849bf96c5aea4c17ac34d6b76e6f4d6de637fdc6b71a37fb17aba`  
		Last Modified: Thu, 24 Mar 2022 02:28:34 GMT  
		Size: 6.7 MB (6677403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee04b08f8d6e6c142ea1315cb5af3d4e1128993694ecbc844cf8142701e77cc`  
		Last Modified: Thu, 24 Mar 2022 02:28:53 GMT  
		Size: 1.2 MB (1178504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56110c558a09687d4b1566c4c5f063c9207ccab44ab0810d3e4e189d46c7983`  
		Last Modified: Thu, 24 Mar 2022 02:28:51 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ecbc10f3f810710b018049c60fc8e6eee68603d6e143125d52c698049bfe4ab4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114681142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422a80d5b1020e2f6ea922c1ee34808bfc55b24c0a0ca63811e610bd56c7c31d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:43:55 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:43:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:43:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:48:35 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:51:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:51:52 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:51:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:51:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:51:54 GMT
WORKDIR /go
# Thu, 24 Mar 2022 04:35:30 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 04:35:31 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 04:36:00 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 24 Mar 2022 04:36:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 04:36:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 04:36:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 04:36:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331b3631dc9d8ace1881c2cb1c28eb266b0ec19c778721faa865e7bb38223ff6`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 271.1 KB (271107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac904122a78116e4100e90af49a2891c00345dbccfae86db8d59e7eb485212d1`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba6f0fdfa168bee61b63cce8a65b54fc5a493c16656abe13d65fb568c83352f`  
		Last Modified: Wed, 23 Mar 2022 21:39:45 GMT  
		Size: 104.9 MB (104853378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137658965282de05bacdac1471373fd69acaae9418ca2169e043327d833e27ca`  
		Last Modified: Wed, 23 Mar 2022 21:38:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52955aeb924042d48cdbb607de289b7457f6a5d6a0e9739931f61fdfe427f344`  
		Last Modified: Thu, 24 Mar 2022 04:37:20 GMT  
		Size: 6.0 MB (5952171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e57ba208689f1e427c40a667a2cbf3edb416f56bcb0ccd9acf9d92ff64cf7ec`  
		Last Modified: Thu, 24 Mar 2022 04:37:37 GMT  
		Size: 1.2 MB (1176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c01f8f1215d9923669ae5bfd5ff09d671cc335546f613cb8dc65185fce8f4d9`  
		Last Modified: Thu, 24 Mar 2022 04:37:36 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:e03d21b158b53739152a61e319318968c01bb7f87b7b2ca75b4dfa81eebc14e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115485391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298230d91553e6791cd20293b4590be6d4c1f50bae2c1d1a73828b2f37963ff0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 08:40:42 GMT
RUN apk add --no-cache ca-certificates
# Thu, 24 Mar 2022 09:03:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Mar 2022 09:03:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 09:05:34 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 24 Mar 2022 09:06:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 24 Mar 2022 09:06:52 GMT
ENV GOPATH=/go
# Thu, 24 Mar 2022 09:06:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 09:06:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 24 Mar 2022 09:06:55 GMT
WORKDIR /go
# Thu, 24 Mar 2022 12:06:47 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 12:06:48 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 12:07:05 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 24 Mar 2022 12:07:06 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 12:07:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 12:07:09 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 12:07:09 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b0b4c4587fbfa6f0755490bb53175932c8f0348926efd629b5e26b281aaa57`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 271.8 KB (271767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bc71a7e8dd1d9668121710be981aa07a74660d94ff3bc08a49ec70e7654c7f`  
		Last Modified: Thu, 24 Mar 2022 09:08:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f22eeb6ec86e713b0a2cb7da0cc984bba811a2fd1d3aef57ac8a509969f9a2e`  
		Last Modified: Thu, 24 Mar 2022 09:09:26 GMT  
		Size: 104.4 MB (104423565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1374803ba168889172986189f9d0d20f5b1491771af58ebe714cb84f99fa3a15`  
		Last Modified: Thu, 24 Mar 2022 09:09:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a9f8667a88f626fef41f02488af5fd79509d422aa4e00fe721fd704c067f87`  
		Last Modified: Thu, 24 Mar 2022 12:07:47 GMT  
		Size: 6.9 MB (6925978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc1f36fe97759a3c941c9bbb783a066a205d6a7641df288c8e398cf745c0adf`  
		Last Modified: Thu, 24 Mar 2022 12:08:01 GMT  
		Size: 1.1 MB (1148676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42056a5405a9966a5c1873220813b7c5dfd11720c840128f601dd8591eb0871`  
		Last Modified: Thu, 24 Mar 2022 12:08:01 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:e483074a29e546b36e2203bf14bb58c153e5ff44e11e808abdfab6fa82e461c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114315661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:944022d2960c692dc7335ab921050060ff9f7023e99a428263163792fc7c81ff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:57:35 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:57:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:57:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 20:14:48 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 20:17:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 20:17:23 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 20:17:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 20:17:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 20:17:52 GMT
WORKDIR /go
# Thu, 24 Mar 2022 03:31:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 03:31:15 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 03:32:03 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 24 Mar 2022 03:32:09 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 03:32:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 03:32:18 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 03:32:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1638cef9b912d53eb425be9e028b98f20521ef09b221e120180e69b238a14321`  
		Last Modified: Wed, 23 Mar 2022 20:19:18 GMT  
		Size: 274.2 KB (274168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611046ca672b25224535bd7440ddf58c8b3f23db1f3b3a079dd7411ea06aafa1`  
		Last Modified: Wed, 23 Mar 2022 20:19:17 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5277b684f884438c817309578480b4bbaf44dec0767ea8c51ceb76bb9b9b60`  
		Last Modified: Wed, 23 Mar 2022 20:19:35 GMT  
		Size: 102.8 MB (102784907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb475fbb9abdc19e3bb6e3ce9caedb03b0cfb03f91dffdc01117daa32d36dfa`  
		Last Modified: Wed, 23 Mar 2022 20:19:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53cb43e7adeb1ac72bd05420bc8de466a4b23f7ef2834419cbbe6f04415022f1`  
		Last Modified: Thu, 24 Mar 2022 03:33:11 GMT  
		Size: 7.3 MB (7320988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be52f569cec212bde962ac7e9b67f50a0939d936c96865cea5e497eb040db36`  
		Last Modified: Thu, 24 Mar 2022 03:33:29 GMT  
		Size: 1.1 MB (1120845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b792fe773414624529314bb651b4cb7e8ec707a5be98b213dc5c2a52bd2a5`  
		Last Modified: Thu, 24 Mar 2022 03:33:29 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:60e293a1beb396dac5ddeca98fe7f194f70e8b7bf1b535d7c2681d4c4e9b6d1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118748535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b90d3c913d4b2c1b3677c3d297e12ff63b20561cca0a1120253b1bce0d9414e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:03:22 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:03:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:03:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:05:28 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:06:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:06:54 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:06:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:06:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:06:55 GMT
WORKDIR /go
# Wed, 23 Mar 2022 22:22:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 23 Mar 2022 22:22:04 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 23 Mar 2022 22:22:18 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Wed, 23 Mar 2022 22:22:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 23 Mar 2022 22:22:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 23 Mar 2022 22:22:19 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 23 Mar 2022 22:22:20 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332d95e018732d014fb48555d26ed3b1acdc693fa15e5e47a76df80ae10a5fb1`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 272.3 KB (272259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f72ff5871bf659daab8a8511372fe2c96cedb9bcf381d83295e789a93f4b07`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80339d6bea83256c3717aaab67711c55ac89a9bc146b9c891fe826e0462b6b5`  
		Last Modified: Wed, 23 Mar 2022 19:09:18 GMT  
		Size: 107.7 MB (107739195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20716e4f8fc56be1943b49531d073a7a30112a97e9c1772dd2d67f495afab1`  
		Last Modified: Wed, 23 Mar 2022 19:09:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cb1e266fa8a15e2d1a81bc572482e40c95b2db376d37a0935415cb96404132`  
		Last Modified: Wed, 23 Mar 2022 22:23:01 GMT  
		Size: 6.9 MB (6930889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38005ba0732ecf7fa5f1ab285724f8283369616bb88bfe66ae4cd4545ab98429`  
		Last Modified: Wed, 23 Mar 2022 22:23:17 GMT  
		Size: 1.2 MB (1203782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e08e3235979b535ee78a676613109e9ce8a5d43366ef9353d38047ccf533df`  
		Last Modified: Wed, 23 Mar 2022 22:23:17 GMT  
		Size: 403.0 B  
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
$ docker pull caddy@sha256:b5a59725783bab0d65803f87028c68dd6611ca6184040bd98b18797cbe26bdd9
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
$ docker pull caddy@sha256:e9451e07cc2803c7a90963bf251e0b81abcc9967ca49fb7a87c3301fad5e60dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735d6b37a42653d291d2a89384895976357b1437fb674a07614cbd3fb35f00e0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:02:43 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 19 Mar 2022 00:02:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 19 Mar 2022 00:02:45 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 19 Mar 2022 00:02:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 19 Mar 2022 00:02:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 19 Mar 2022 00:02:49 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Mar 2022 00:02:49 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Mar 2022 00:02:49 GMT
VOLUME [/config]
# Sat, 19 Mar 2022 00:02:50 GMT
VOLUME [/data]
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 80
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 443
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 2019
# Sat, 19 Mar 2022 00:02:52 GMT
WORKDIR /srv
# Sat, 19 Mar 2022 00:02:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c225d4ce3a38a8a3e6febdc9bbb81aa1faff22dfdccfc44d557d61621d8c3b3`  
		Last Modified: Sat, 19 Mar 2022 00:03:30 GMT  
		Size: 291.2 KB (291236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b48903a98ce96620ab34d505f9fd3337e46ef729e6b93f4c31442a01c031958`  
		Last Modified: Sat, 19 Mar 2022 00:03:29 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9a49498837c179e70172feedd8b5b1684fda96fc85932d533d15fb395d2d25`  
		Last Modified: Sat, 19 Mar 2022 00:03:32 GMT  
		Size: 11.7 MB (11726453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f986cb0c37bc3e0802acdfcb21bfebfdfadce1af2753530be51de31642dc8db5`  
		Last Modified: Sat, 19 Mar 2022 00:03:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5f09a9314e7bcb6c997fafb0c72623e4fe1333f5ffacf717901b8d71992a6314
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14052796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23651bcdf82f31f580af8bb2a691742988178ec24273cc7d427790fc899b70d2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 14:58:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 14:58:06 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 14:58:07 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 14:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 14:58:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 14:58:13 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 14:58:14 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 14:58:14 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 14:58:15 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 14:58:15 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 14:58:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 14:58:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 14:58:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 14:58:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 14:58:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 14:58:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 14:58:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 14:58:19 GMT
EXPOSE 80
# Thu, 17 Mar 2022 14:58:19 GMT
EXPOSE 443
# Thu, 17 Mar 2022 14:58:20 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 14:58:20 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 14:58:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe387c61070bfe1fbf52bdf2f034ca39f369605473616ebfc4b89287058a395d`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 291.6 KB (291648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bc40a5454d774d40dfddbe6f85673f34aed00cd8e9a3035963763b18376639`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81988b3231106e730dc6c7d0b24ebc84826809dd090bff899495129990559e78`  
		Last Modified: Thu, 17 Mar 2022 15:00:19 GMT  
		Size: 11.1 MB (11125802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd1a3665abdbac555066d2695c45980beba49a104e3a55b2d2cf31f8da4c2da`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5d40c99ca31d7c7cc087a8c0059966c8b9e43f0bafbf525cf4fb1494a45da5b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13833799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde5bec726177426cb4d320b0f016f0a8e4569182c6de303c9c9d042446b6197`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 17:21:06 GMT
ADD file:c25fcf153ea349f64e08a1bd0756ce550f2a081ad56cc40c89027d85d1bc26da in / 
# Thu, 17 Mar 2022 17:21:06 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 18:17:11 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 18:17:12 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 18:17:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 18:17:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 18:17:19 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 18:17:19 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 18:17:20 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 18:17:20 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 18:17:21 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 18:17:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 18:17:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 18:17:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 18:17:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 18:17:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 18:17:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 18:17:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 18:17:25 GMT
EXPOSE 80
# Thu, 17 Mar 2022 18:17:25 GMT
EXPOSE 443
# Thu, 17 Mar 2022 18:17:26 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 18:17:26 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 18:17:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c3a1157c36d8d156f7664fa098212ab2149a64bcb59767cdf4595a86617c17fd`  
		Last Modified: Thu, 17 Mar 2022 17:22:45 GMT  
		Size: 2.4 MB (2430456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376a93fbfdd661b6ba92aa7097c65e646f83c50d150e4227f42141e158b7928b`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 290.6 KB (290632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3bd6226dffa9763d44b0e5688ab7b844b744846e3cc0fa7d8ab6d3c068e466`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9ffbfdd3e888d3f9a94270e0b47ca758645b21ec38f6a203223475052b2802`  
		Last Modified: Thu, 17 Mar 2022 18:19:42 GMT  
		Size: 11.1 MB (11106727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb6dc1be2f2389fa78d2d0002c63575d8d14197e59e0347dbca9ae951a38d4f`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:a4e7a7a9d505b716122bbfb9b41e25b8189dafc8115284279687c2021de7aca1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13751720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a574b32ce3c98bd1848efe2e07ad86e55789b4da7fe02909566fa06a0fdbe6a1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 07:13:27 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 18 Mar 2022 07:13:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 18 Mar 2022 07:13:30 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 18 Mar 2022 07:13:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 18 Mar 2022 07:13:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 18 Mar 2022 07:13:34 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 18 Mar 2022 07:13:35 GMT
ENV XDG_DATA_HOME=/data
# Fri, 18 Mar 2022 07:13:36 GMT
VOLUME [/config]
# Fri, 18 Mar 2022 07:13:37 GMT
VOLUME [/data]
# Fri, 18 Mar 2022 07:13:38 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 18 Mar 2022 07:13:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 18 Mar 2022 07:13:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 18 Mar 2022 07:13:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 18 Mar 2022 07:13:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 18 Mar 2022 07:13:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 18 Mar 2022 07:13:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 18 Mar 2022 07:13:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 18 Mar 2022 07:13:46 GMT
EXPOSE 80
# Fri, 18 Mar 2022 07:13:47 GMT
EXPOSE 443
# Fri, 18 Mar 2022 07:13:48 GMT
EXPOSE 2019
# Fri, 18 Mar 2022 07:13:49 GMT
WORKDIR /srv
# Fri, 18 Mar 2022 07:13:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649e3e65430e0077032ab20dedb081c00e1be3a1f4660b94275f242d1dcd295d`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 291.3 KB (291292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048be0a2d569af2daf2b6cd4728a72f8fecd26611069441023a70b360d3850a0`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 5.8 KB (5751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e382adfd8256a09e2e4bed4c90c8755fc3ee3c58e0679734cd85e4da6ac486`  
		Last Modified: Fri, 18 Mar 2022 07:14:59 GMT  
		Size: 10.7 MB (10738636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d589a4f582ad58b1be3ac310f968793927b5d1629ae84b5c78100265bd825d`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b91b55c6bdcfe17f047217339ace7c264f76e9011d077d7f84cb4852667273e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13419279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0272ad9824009f684ca3ecddd7e61583b5994b0c08a6db63295222a0dbf8a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 18:18:43 GMT
ADD file:bf9c99d8209e0bed9fd3b62cbe691ebf3829d5a35e63e2b066f1f842577a6d24 in / 
# Thu, 17 Mar 2022 18:18:48 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:30:55 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 21:31:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 21:31:03 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 21:31:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 21:31:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 21:31:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 21:31:22 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 21:31:24 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 21:31:27 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 21:31:29 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 21:31:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 21:31:34 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 21:31:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 21:31:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 21:31:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 21:31:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 21:31:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 21:31:49 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:31:55 GMT
EXPOSE 443
# Thu, 17 Mar 2022 21:31:58 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 21:32:01 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 21:32:03 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8b7e8363a93630a772b70e3cf72231f43c62addae0ee8e507c61d43e3781c4e7`  
		Last Modified: Thu, 17 Mar 2022 18:20:01 GMT  
		Size: 2.8 MB (2817281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e91dcc90eb989323abf507cb545731e08fdb7ae99452318650960f3b2bc29b8`  
		Last Modified: Thu, 17 Mar 2022 21:34:38 GMT  
		Size: 293.7 KB (293720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8763c1a56f6f74d41630bbb545d52602505e99c0e311f1ccfc50c001aa5c705c`  
		Last Modified: Thu, 17 Mar 2022 21:34:37 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e19db97ec3aacb5588ff43135ffccf7eef8281b28c0f3e95f8fa4a4c6e9f554`  
		Last Modified: Thu, 17 Mar 2022 21:34:40 GMT  
		Size: 10.3 MB (10302291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5f036cbadaf9e63bb1584d58115f79a3f4f9fdbce665e25642178129efa74b`  
		Last Modified: Thu, 17 Mar 2022 21:34:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:f710373b7c95e8c39a1e57b06884bac2548574d182889812998295c8b120c1ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14226716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced9b4438f1c256b9508d7d3dbf5048aed06c31b8a05cfbda638e5292d0dee83`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:00:36 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 21:00:37 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 21:00:37 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 21:00:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 21:00:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 21:00:40 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 21:00:40 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 21:00:40 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 21:00:41 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 21:00:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 443
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 21:00:42 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 21:00:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c5df2f20a519a7f78f07f63378f86b2481339dccb5001000518f146e1ef5c0`  
		Last Modified: Thu, 17 Mar 2022 21:01:48 GMT  
		Size: 291.8 KB (291797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6179022673cadc5a23974fa435eaa88fbe3c46ae7f0e61e3a80fa34f7cb6c846`  
		Last Modified: Thu, 17 Mar 2022 21:01:47 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a36f8de1aad1bf91018c94013e0cf58d27a1e6c141c8c11cb4beae1b0aaa78`  
		Last Modified: Thu, 17 Mar 2022 21:01:49 GMT  
		Size: 11.3 MB (11323729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f17a5362f8b342e5c3ac44e83b09ad5a9c93dabbea07012c1a32399962536e`  
		Last Modified: Thu, 17 Mar 2022 21:01:48 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:d68bc5f41d6aa3c85abcf9601715ad226a9a29f9e33b7d47c6d963804a3777cd
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
$ docker pull caddy@sha256:2cde19d722eecd94ceaa9bab9a6c4347f74ce5a2fd3a0a48a509e971f13591c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121339146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09d14008da07e14004b96c64f6845c57e0e194ca4de036a13fdf51fe4187d75`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 17:33:52 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 17:47:17 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 17:47:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:49:48 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 17:51:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 17:51:49 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 17:51:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:51:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 17:51:50 GMT
WORKDIR /go
# Wed, 23 Mar 2022 20:57:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 23 Mar 2022 20:57:03 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 23 Mar 2022 20:57:03 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 23 Mar 2022 20:57:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 23 Mar 2022 20:57:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 23 Mar 2022 20:57:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 23 Mar 2022 20:57:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ae170c2a8ceb6dfe7dd52edb58d7be5583518415f0e441c5b7d4f0f8bad244`  
		Last Modified: Wed, 23 Mar 2022 17:34:04 GMT  
		Size: 272.0 KB (271973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb35b180f41941e8ec9af85110ff412f204e4afaf593ac8fc601c07b7449304d`  
		Last Modified: Wed, 23 Mar 2022 17:52:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367011ddbc177b50e507d24a640d8fdbdd64a32a4b0e2a3549ad26a1c0581da5`  
		Last Modified: Wed, 23 Mar 2022 17:53:41 GMT  
		Size: 110.2 MB (110186567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318840287a8912b4d3a5caf13e21932dd668cfa441f84c3f7cb89884f12bc498`  
		Last Modified: Wed, 23 Mar 2022 17:53:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c39dbaf7c7b7fee5c862d4a01ade30b6cc7ab1640f4d9768f164f020ebb0df`  
		Last Modified: Wed, 23 Mar 2022 20:57:42 GMT  
		Size: 6.8 MB (6821487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7c788e131725ef62ff805cf02500b08d59ffe6c17a83e2dfa2c19a5999259e`  
		Last Modified: Wed, 23 Mar 2022 20:57:42 GMT  
		Size: 1.2 MB (1245716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66404f523f94bed92b342dc3d6d751110fe89285e41d3428c8961f4ff8c970ae`  
		Last Modified: Wed, 23 Mar 2022 20:57:41 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f1da3f8fa8aed1df028de4dbfa4512d40b857dae6a2a67f37a3359059c6c8252
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115822199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4371bb88d2b11615cd2bbf5613374b41164d11cf83b1ea4ddc7560961210c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:49:35 GMT
ADD file:fd7f6da4a48df653ae6dd18e6d5959008daf5ce429845c974982dc7d213342d9 in / 
# Wed, 23 Mar 2022 15:49:35 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:19:47 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:19:48 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:19:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:24:07 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:27:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:27:24 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:27:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:27:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:27:26 GMT
WORKDIR /go
# Thu, 24 Mar 2022 02:26:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 02:26:42 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 02:26:43 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 02:26:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 02:26:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 02:26:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 02:26:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4e012d7cd81aa4570d9d209a75131b32f34a3533d5d449d23fd875513922588e`  
		Last Modified: Wed, 23 Mar 2022 15:51:07 GMT  
		Size: 2.6 MB (2624816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b4a951e94c8a6946a91154ab5ace93adbd78d1ebd435a602fb836ac671efd7`  
		Last Modified: Wed, 23 Mar 2022 19:29:03 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63d00ec81dafe9f0ca510122a4959c5a6a1f1c1acf4be47bf25c3cff6cd4be9`  
		Last Modified: Wed, 23 Mar 2022 19:29:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71824796f74f5fbac9812755baf9bc693e67715490b2b7bf6b83484476796f9c`  
		Last Modified: Wed, 23 Mar 2022 19:32:09 GMT  
		Size: 105.1 MB (105068610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5b249d15fb3bdb66c75a0883f0d10c153c767bb066d86c428791a5478ccb1a`  
		Last Modified: Wed, 23 Mar 2022 19:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0daf81a4e5a849bf96c5aea4c17ac34d6b76e6f4d6de637fdc6b71a37fb17aba`  
		Last Modified: Thu, 24 Mar 2022 02:28:34 GMT  
		Size: 6.7 MB (6677403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd152783b4ba077867dc853a8a18f0a188c9416b1df4a65852513c0199c6e68`  
		Last Modified: Thu, 24 Mar 2022 02:28:32 GMT  
		Size: 1.2 MB (1178511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e80b5acad3274c86d1c575b8370883cbc92a0bcf8f69787011ab5e9ad0309d`  
		Last Modified: Thu, 24 Mar 2022 02:28:31 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:02f8b98f2d7f610839150ec7c8b2cb28303ae5b928a3c46827dba569edcd4cc2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114681140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3173e35645f6e2df7cbb70ab3f0caa9e2e9d580c868b7323cbd4daa9fdf36a95`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:43:55 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:43:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:43:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:48:35 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:51:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:51:52 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:51:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:51:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:51:54 GMT
WORKDIR /go
# Thu, 24 Mar 2022 04:35:30 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 04:35:31 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 04:35:31 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 04:35:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 04:35:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 04:35:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 04:35:35 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331b3631dc9d8ace1881c2cb1c28eb266b0ec19c778721faa865e7bb38223ff6`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 271.1 KB (271107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac904122a78116e4100e90af49a2891c00345dbccfae86db8d59e7eb485212d1`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba6f0fdfa168bee61b63cce8a65b54fc5a493c16656abe13d65fb568c83352f`  
		Last Modified: Wed, 23 Mar 2022 21:39:45 GMT  
		Size: 104.9 MB (104853378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137658965282de05bacdac1471373fd69acaae9418ca2169e043327d833e27ca`  
		Last Modified: Wed, 23 Mar 2022 21:38:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52955aeb924042d48cdbb607de289b7457f6a5d6a0e9739931f61fdfe427f344`  
		Last Modified: Thu, 24 Mar 2022 04:37:20 GMT  
		Size: 6.0 MB (5952171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4014b68d35871bfdbe2e53206c7c5d4ced7c200ae0fcd28605f203330c4bfe1`  
		Last Modified: Thu, 24 Mar 2022 04:37:18 GMT  
		Size: 1.2 MB (1176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fba897ff3f805fe40858af1887544e7fa2e99543c8410fbfb002a3a21ddaf8`  
		Last Modified: Thu, 24 Mar 2022 04:37:18 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:ea3dfbed453c77f5f75be7cb81c2ccee9dce3c65b654e8ef309dfe32b33652e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115485391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15729f70afc23409c5069a96dd3a3a35df28d19c5becc3bdc6dacc7c156a3777`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 08:40:42 GMT
RUN apk add --no-cache ca-certificates
# Thu, 24 Mar 2022 09:03:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Mar 2022 09:03:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 09:05:34 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 24 Mar 2022 09:06:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 24 Mar 2022 09:06:52 GMT
ENV GOPATH=/go
# Thu, 24 Mar 2022 09:06:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 09:06:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 24 Mar 2022 09:06:55 GMT
WORKDIR /go
# Thu, 24 Mar 2022 12:06:47 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 12:06:48 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 12:06:49 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 12:06:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 12:06:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 12:06:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 12:06:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b0b4c4587fbfa6f0755490bb53175932c8f0348926efd629b5e26b281aaa57`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 271.8 KB (271767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bc71a7e8dd1d9668121710be981aa07a74660d94ff3bc08a49ec70e7654c7f`  
		Last Modified: Thu, 24 Mar 2022 09:08:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f22eeb6ec86e713b0a2cb7da0cc984bba811a2fd1d3aef57ac8a509969f9a2e`  
		Last Modified: Thu, 24 Mar 2022 09:09:26 GMT  
		Size: 104.4 MB (104423565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1374803ba168889172986189f9d0d20f5b1491771af58ebe714cb84f99fa3a15`  
		Last Modified: Thu, 24 Mar 2022 09:09:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a9f8667a88f626fef41f02488af5fd79509d422aa4e00fe721fd704c067f87`  
		Last Modified: Thu, 24 Mar 2022 12:07:47 GMT  
		Size: 6.9 MB (6925978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b55c23fcf50b7be62fd87f864eb47347cc2bffb823221798cbfcf40d994fdd`  
		Last Modified: Thu, 24 Mar 2022 12:07:46 GMT  
		Size: 1.1 MB (1148676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d38bff84bce7d7ee9ea1a3bfe3473790a3681d0ecec05d0bdd077af8a567ab1`  
		Last Modified: Thu, 24 Mar 2022 12:07:46 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:11649bbf1cf06ebea3bcef630c8601cc35feaa553ade9923fa62f53c282db438
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114315662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc5080a9dc71d919e80a3f561c2b9af0560976209f3535b1c327b1f26650fff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:57:35 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:57:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:57:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 20:14:48 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 20:17:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 20:17:23 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 20:17:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 20:17:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 20:17:52 GMT
WORKDIR /go
# Thu, 24 Mar 2022 03:31:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 03:31:15 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 03:31:18 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 03:31:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 03:31:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 03:31:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 03:31:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1638cef9b912d53eb425be9e028b98f20521ef09b221e120180e69b238a14321`  
		Last Modified: Wed, 23 Mar 2022 20:19:18 GMT  
		Size: 274.2 KB (274168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611046ca672b25224535bd7440ddf58c8b3f23db1f3b3a079dd7411ea06aafa1`  
		Last Modified: Wed, 23 Mar 2022 20:19:17 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5277b684f884438c817309578480b4bbaf44dec0767ea8c51ceb76bb9b9b60`  
		Last Modified: Wed, 23 Mar 2022 20:19:35 GMT  
		Size: 102.8 MB (102784907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb475fbb9abdc19e3bb6e3ce9caedb03b0cfb03f91dffdc01117daa32d36dfa`  
		Last Modified: Wed, 23 Mar 2022 20:19:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53cb43e7adeb1ac72bd05420bc8de466a4b23f7ef2834419cbbe6f04415022f1`  
		Last Modified: Thu, 24 Mar 2022 03:33:11 GMT  
		Size: 7.3 MB (7320988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c822ff2754104c9cdf880adb708e4dec3d253566eb6e2287220bab202d462abc`  
		Last Modified: Thu, 24 Mar 2022 03:33:09 GMT  
		Size: 1.1 MB (1120846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016dbe0d502dc8e63e4f16f1f7936c74e076cbf990aaea69795c2a56b4c137df`  
		Last Modified: Thu, 24 Mar 2022 03:33:09 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:dfcf236ef9b39bb046ee1f48ecd09d1c7fc7a1f577993d7f7853f55eae3d648b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118748542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e7df7a28241422c766fb3b02badc9125abfd33f30709757ca435b65bc47adb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:03:22 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:03:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:03:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:05:28 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:06:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:06:54 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:06:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:06:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:06:55 GMT
WORKDIR /go
# Wed, 23 Mar 2022 22:22:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 23 Mar 2022 22:22:04 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 23 Mar 2022 22:22:04 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 23 Mar 2022 22:22:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 23 Mar 2022 22:22:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 23 Mar 2022 22:22:05 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 23 Mar 2022 22:22:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332d95e018732d014fb48555d26ed3b1acdc693fa15e5e47a76df80ae10a5fb1`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 272.3 KB (272259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f72ff5871bf659daab8a8511372fe2c96cedb9bcf381d83295e789a93f4b07`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80339d6bea83256c3717aaab67711c55ac89a9bc146b9c891fe826e0462b6b5`  
		Last Modified: Wed, 23 Mar 2022 19:09:18 GMT  
		Size: 107.7 MB (107739195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20716e4f8fc56be1943b49531d073a7a30112a97e9c1772dd2d67f495afab1`  
		Last Modified: Wed, 23 Mar 2022 19:09:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cb1e266fa8a15e2d1a81bc572482e40c95b2db376d37a0935415cb96404132`  
		Last Modified: Wed, 23 Mar 2022 22:23:01 GMT  
		Size: 6.9 MB (6930889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b96c8a99cb7674ba09bf70886a1b327bd8dc19b439c6e828dd8fa8de98261d`  
		Last Modified: Wed, 23 Mar 2022 22:23:01 GMT  
		Size: 1.2 MB (1203789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1572768c5198e65924f57fb4f9008d0847a676367109b9e0d0aad64521b498`  
		Last Modified: Wed, 23 Mar 2022 22:23:00 GMT  
		Size: 403.0 B  
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
$ docker pull caddy@sha256:a2ce0b7552206ba989201ea58d325b7c3ddab4ac035b017775e800bf42e224cb
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
$ docker pull caddy@sha256:2cde19d722eecd94ceaa9bab9a6c4347f74ce5a2fd3a0a48a509e971f13591c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121339146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09d14008da07e14004b96c64f6845c57e0e194ca4de036a13fdf51fe4187d75`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 17:33:52 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 17:47:17 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 17:47:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:49:48 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 17:51:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 17:51:49 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 17:51:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 17:51:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 17:51:50 GMT
WORKDIR /go
# Wed, 23 Mar 2022 20:57:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 23 Mar 2022 20:57:03 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 23 Mar 2022 20:57:03 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 23 Mar 2022 20:57:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 23 Mar 2022 20:57:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 23 Mar 2022 20:57:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 23 Mar 2022 20:57:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ae170c2a8ceb6dfe7dd52edb58d7be5583518415f0e441c5b7d4f0f8bad244`  
		Last Modified: Wed, 23 Mar 2022 17:34:04 GMT  
		Size: 272.0 KB (271973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb35b180f41941e8ec9af85110ff412f204e4afaf593ac8fc601c07b7449304d`  
		Last Modified: Wed, 23 Mar 2022 17:52:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367011ddbc177b50e507d24a640d8fdbdd64a32a4b0e2a3549ad26a1c0581da5`  
		Last Modified: Wed, 23 Mar 2022 17:53:41 GMT  
		Size: 110.2 MB (110186567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318840287a8912b4d3a5caf13e21932dd668cfa441f84c3f7cb89884f12bc498`  
		Last Modified: Wed, 23 Mar 2022 17:53:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c39dbaf7c7b7fee5c862d4a01ade30b6cc7ab1640f4d9768f164f020ebb0df`  
		Last Modified: Wed, 23 Mar 2022 20:57:42 GMT  
		Size: 6.8 MB (6821487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7c788e131725ef62ff805cf02500b08d59ffe6c17a83e2dfa2c19a5999259e`  
		Last Modified: Wed, 23 Mar 2022 20:57:42 GMT  
		Size: 1.2 MB (1245716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66404f523f94bed92b342dc3d6d751110fe89285e41d3428c8961f4ff8c970ae`  
		Last Modified: Wed, 23 Mar 2022 20:57:41 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f1da3f8fa8aed1df028de4dbfa4512d40b857dae6a2a67f37a3359059c6c8252
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115822199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4371bb88d2b11615cd2bbf5613374b41164d11cf83b1ea4ddc7560961210c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:49:35 GMT
ADD file:fd7f6da4a48df653ae6dd18e6d5959008daf5ce429845c974982dc7d213342d9 in / 
# Wed, 23 Mar 2022 15:49:35 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:19:47 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:19:48 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:19:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:24:07 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:27:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:27:24 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:27:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:27:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:27:26 GMT
WORKDIR /go
# Thu, 24 Mar 2022 02:26:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 02:26:42 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 02:26:43 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 02:26:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 02:26:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 02:26:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 02:26:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4e012d7cd81aa4570d9d209a75131b32f34a3533d5d449d23fd875513922588e`  
		Last Modified: Wed, 23 Mar 2022 15:51:07 GMT  
		Size: 2.6 MB (2624816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b4a951e94c8a6946a91154ab5ace93adbd78d1ebd435a602fb836ac671efd7`  
		Last Modified: Wed, 23 Mar 2022 19:29:03 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63d00ec81dafe9f0ca510122a4959c5a6a1f1c1acf4be47bf25c3cff6cd4be9`  
		Last Modified: Wed, 23 Mar 2022 19:29:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71824796f74f5fbac9812755baf9bc693e67715490b2b7bf6b83484476796f9c`  
		Last Modified: Wed, 23 Mar 2022 19:32:09 GMT  
		Size: 105.1 MB (105068610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5b249d15fb3bdb66c75a0883f0d10c153c767bb066d86c428791a5478ccb1a`  
		Last Modified: Wed, 23 Mar 2022 19:30:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0daf81a4e5a849bf96c5aea4c17ac34d6b76e6f4d6de637fdc6b71a37fb17aba`  
		Last Modified: Thu, 24 Mar 2022 02:28:34 GMT  
		Size: 6.7 MB (6677403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd152783b4ba077867dc853a8a18f0a188c9416b1df4a65852513c0199c6e68`  
		Last Modified: Thu, 24 Mar 2022 02:28:32 GMT  
		Size: 1.2 MB (1178511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e80b5acad3274c86d1c575b8370883cbc92a0bcf8f69787011ab5e9ad0309d`  
		Last Modified: Thu, 24 Mar 2022 02:28:31 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:02f8b98f2d7f610839150ec7c8b2cb28303ae5b928a3c46827dba569edcd4cc2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114681140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3173e35645f6e2df7cbb70ab3f0caa9e2e9d580c868b7323cbd4daa9fdf36a95`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:57:29 GMT
ADD file:462f633d612f6502dcfa539fcfd8b1fc90da097b08ad6b984e485bc73e57bd41 in / 
# Wed, 23 Mar 2022 15:57:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:43:55 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:43:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:43:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:48:35 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:51:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:51:52 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:51:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:51:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:51:54 GMT
WORKDIR /go
# Thu, 24 Mar 2022 04:35:30 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 04:35:31 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 04:35:31 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 04:35:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 04:35:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 04:35:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 04:35:35 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:dfd6a1b07255bd60715939c7488b4714efdc3519f793d4d8b238b910091c1642`  
		Last Modified: Wed, 23 Mar 2022 15:58:58 GMT  
		Size: 2.4 MB (2427061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331b3631dc9d8ace1881c2cb1c28eb266b0ec19c778721faa865e7bb38223ff6`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 271.1 KB (271107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac904122a78116e4100e90af49a2891c00345dbccfae86db8d59e7eb485212d1`  
		Last Modified: Wed, 23 Mar 2022 19:55:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba6f0fdfa168bee61b63cce8a65b54fc5a493c16656abe13d65fb568c83352f`  
		Last Modified: Wed, 23 Mar 2022 21:39:45 GMT  
		Size: 104.9 MB (104853378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137658965282de05bacdac1471373fd69acaae9418ca2169e043327d833e27ca`  
		Last Modified: Wed, 23 Mar 2022 21:38:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52955aeb924042d48cdbb607de289b7457f6a5d6a0e9739931f61fdfe427f344`  
		Last Modified: Thu, 24 Mar 2022 04:37:20 GMT  
		Size: 6.0 MB (5952171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4014b68d35871bfdbe2e53206c7c5d4ced7c200ae0fcd28605f203330c4bfe1`  
		Last Modified: Thu, 24 Mar 2022 04:37:18 GMT  
		Size: 1.2 MB (1176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fba897ff3f805fe40858af1887544e7fa2e99543c8410fbfb002a3a21ddaf8`  
		Last Modified: Thu, 24 Mar 2022 04:37:18 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:ea3dfbed453c77f5f75be7cb81c2ccee9dce3c65b654e8ef309dfe32b33652e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115485391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15729f70afc23409c5069a96dd3a3a35df28d19c5becc3bdc6dacc7c156a3777`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 24 Mar 2022 00:36:14 GMT
ADD file:30da1868f9f0555fb3e5223cd75cbf3c31760c1b6087f42d78abb08a8c5066ff in / 
# Thu, 24 Mar 2022 00:36:14 GMT
CMD ["/bin/sh"]
# Thu, 24 Mar 2022 08:40:42 GMT
RUN apk add --no-cache ca-certificates
# Thu, 24 Mar 2022 09:03:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 24 Mar 2022 09:03:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 09:05:34 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 24 Mar 2022 09:06:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 24 Mar 2022 09:06:52 GMT
ENV GOPATH=/go
# Thu, 24 Mar 2022 09:06:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Mar 2022 09:06:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 24 Mar 2022 09:06:55 GMT
WORKDIR /go
# Thu, 24 Mar 2022 12:06:47 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 12:06:48 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 12:06:49 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 12:06:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 12:06:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 12:06:54 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 12:06:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a5e44472bb1f0d721d23f82fa10a4c3d25994790238a173c1de950a649eb9a90`  
		Last Modified: Wed, 23 Mar 2022 20:10:33 GMT  
		Size: 2.7 MB (2714720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b0b4c4587fbfa6f0755490bb53175932c8f0348926efd629b5e26b281aaa57`  
		Last Modified: Thu, 24 Mar 2022 08:41:08 GMT  
		Size: 271.8 KB (271767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bc71a7e8dd1d9668121710be981aa07a74660d94ff3bc08a49ec70e7654c7f`  
		Last Modified: Thu, 24 Mar 2022 09:08:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f22eeb6ec86e713b0a2cb7da0cc984bba811a2fd1d3aef57ac8a509969f9a2e`  
		Last Modified: Thu, 24 Mar 2022 09:09:26 GMT  
		Size: 104.4 MB (104423565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1374803ba168889172986189f9d0d20f5b1491771af58ebe714cb84f99fa3a15`  
		Last Modified: Thu, 24 Mar 2022 09:09:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a9f8667a88f626fef41f02488af5fd79509d422aa4e00fe721fd704c067f87`  
		Last Modified: Thu, 24 Mar 2022 12:07:47 GMT  
		Size: 6.9 MB (6925978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b55c23fcf50b7be62fd87f864eb47347cc2bffb823221798cbfcf40d994fdd`  
		Last Modified: Thu, 24 Mar 2022 12:07:46 GMT  
		Size: 1.1 MB (1148676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d38bff84bce7d7ee9ea1a3bfe3473790a3681d0ecec05d0bdd077af8a567ab1`  
		Last Modified: Thu, 24 Mar 2022 12:07:46 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:11649bbf1cf06ebea3bcef630c8601cc35feaa553ade9923fa62f53c282db438
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114315662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc5080a9dc71d919e80a3f561c2b9af0560976209f3535b1c327b1f26650fff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:24:30 GMT
ADD file:3392b3547a6a1366b9a6ada72065830d8886708bbfc70472c607e742dfd07994 in / 
# Wed, 23 Mar 2022 15:24:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:57:35 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:57:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:57:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 20:14:48 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 20:17:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 20:17:23 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 20:17:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 20:17:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 20:17:52 GMT
WORKDIR /go
# Thu, 24 Mar 2022 03:31:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 24 Mar 2022 03:31:15 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 24 Mar 2022 03:31:18 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 24 Mar 2022 03:31:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 24 Mar 2022 03:31:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 24 Mar 2022 03:31:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 24 Mar 2022 03:31:39 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:58323f60457d1c04dce77185ce8c0377ac10135b55fdf4506e87d24e67780d7d`  
		Last Modified: Wed, 23 Mar 2022 15:25:23 GMT  
		Size: 2.8 MB (2814037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1638cef9b912d53eb425be9e028b98f20521ef09b221e120180e69b238a14321`  
		Last Modified: Wed, 23 Mar 2022 20:19:18 GMT  
		Size: 274.2 KB (274168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611046ca672b25224535bd7440ddf58c8b3f23db1f3b3a079dd7411ea06aafa1`  
		Last Modified: Wed, 23 Mar 2022 20:19:17 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5277b684f884438c817309578480b4bbaf44dec0767ea8c51ceb76bb9b9b60`  
		Last Modified: Wed, 23 Mar 2022 20:19:35 GMT  
		Size: 102.8 MB (102784907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb475fbb9abdc19e3bb6e3ce9caedb03b0cfb03f91dffdc01117daa32d36dfa`  
		Last Modified: Wed, 23 Mar 2022 20:19:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53cb43e7adeb1ac72bd05420bc8de466a4b23f7ef2834419cbbe6f04415022f1`  
		Last Modified: Thu, 24 Mar 2022 03:33:11 GMT  
		Size: 7.3 MB (7320988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c822ff2754104c9cdf880adb708e4dec3d253566eb6e2287220bab202d462abc`  
		Last Modified: Thu, 24 Mar 2022 03:33:09 GMT  
		Size: 1.1 MB (1120846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016dbe0d502dc8e63e4f16f1f7936c74e076cbf990aaea69795c2a56b4c137df`  
		Last Modified: Thu, 24 Mar 2022 03:33:09 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:dfcf236ef9b39bb046ee1f48ecd09d1c7fc7a1f577993d7f7853f55eae3d648b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118748542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e7df7a28241422c766fb3b02badc9125abfd33f30709757ca435b65bc47adb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:41:27 GMT
ADD file:c6fe4c8affcc912e0de86d8691aecb959ac828259f09843a569ec4e5714d6c6f in / 
# Wed, 23 Mar 2022 15:41:27 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 19:03:22 GMT
RUN apk add --no-cache ca-certificates
# Wed, 23 Mar 2022 19:03:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 23 Mar 2022 19:03:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:05:28 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 23 Mar 2022 19:06:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 23 Mar 2022 19:06:54 GMT
ENV GOPATH=/go
# Wed, 23 Mar 2022 19:06:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Mar 2022 19:06:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 23 Mar 2022 19:06:55 GMT
WORKDIR /go
# Wed, 23 Mar 2022 22:22:03 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 23 Mar 2022 22:22:04 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 23 Mar 2022 22:22:04 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 23 Mar 2022 22:22:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 23 Mar 2022 22:22:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 23 Mar 2022 22:22:05 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 23 Mar 2022 22:22:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:cf2f18c21a46b2d59a7a34a051c9c289710e89cdef47cc582fdb9d65a1e68e44`  
		Last Modified: Wed, 23 Mar 2022 15:42:18 GMT  
		Size: 2.6 MB (2601698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332d95e018732d014fb48555d26ed3b1acdc693fa15e5e47a76df80ae10a5fb1`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 272.3 KB (272259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f72ff5871bf659daab8a8511372fe2c96cedb9bcf381d83295e789a93f4b07`  
		Last Modified: Wed, 23 Mar 2022 19:08:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80339d6bea83256c3717aaab67711c55ac89a9bc146b9c891fe826e0462b6b5`  
		Last Modified: Wed, 23 Mar 2022 19:09:18 GMT  
		Size: 107.7 MB (107739195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20716e4f8fc56be1943b49531d073a7a30112a97e9c1772dd2d67f495afab1`  
		Last Modified: Wed, 23 Mar 2022 19:09:05 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cb1e266fa8a15e2d1a81bc572482e40c95b2db376d37a0935415cb96404132`  
		Last Modified: Wed, 23 Mar 2022 22:23:01 GMT  
		Size: 6.9 MB (6930889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b96c8a99cb7674ba09bf70886a1b327bd8dc19b439c6e828dd8fa8de98261d`  
		Last Modified: Wed, 23 Mar 2022 22:23:01 GMT  
		Size: 1.2 MB (1203789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1572768c5198e65924f57fb4f9008d0847a676367109b9e0d0aad64521b498`  
		Last Modified: Wed, 23 Mar 2022 22:23:00 GMT  
		Size: 403.0 B  
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
$ docker pull caddy@sha256:ea838cedcb447323d5f2726e8671290a277311b5419859d3244640e8f276eb93
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
$ docker pull caddy@sha256:e9451e07cc2803c7a90963bf251e0b81abcc9967ca49fb7a87c3301fad5e60dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735d6b37a42653d291d2a89384895976357b1437fb674a07614cbd3fb35f00e0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:02:43 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 19 Mar 2022 00:02:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 19 Mar 2022 00:02:45 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 19 Mar 2022 00:02:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 19 Mar 2022 00:02:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 19 Mar 2022 00:02:49 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Mar 2022 00:02:49 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Mar 2022 00:02:49 GMT
VOLUME [/config]
# Sat, 19 Mar 2022 00:02:50 GMT
VOLUME [/data]
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 80
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 443
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 2019
# Sat, 19 Mar 2022 00:02:52 GMT
WORKDIR /srv
# Sat, 19 Mar 2022 00:02:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c225d4ce3a38a8a3e6febdc9bbb81aa1faff22dfdccfc44d557d61621d8c3b3`  
		Last Modified: Sat, 19 Mar 2022 00:03:30 GMT  
		Size: 291.2 KB (291236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b48903a98ce96620ab34d505f9fd3337e46ef729e6b93f4c31442a01c031958`  
		Last Modified: Sat, 19 Mar 2022 00:03:29 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9a49498837c179e70172feedd8b5b1684fda96fc85932d533d15fb395d2d25`  
		Last Modified: Sat, 19 Mar 2022 00:03:32 GMT  
		Size: 11.7 MB (11726453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f986cb0c37bc3e0802acdfcb21bfebfdfadce1af2753530be51de31642dc8db5`  
		Last Modified: Sat, 19 Mar 2022 00:03:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5f09a9314e7bcb6c997fafb0c72623e4fe1333f5ffacf717901b8d71992a6314
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14052796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23651bcdf82f31f580af8bb2a691742988178ec24273cc7d427790fc899b70d2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 14:58:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 14:58:06 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 14:58:07 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 14:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 14:58:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 14:58:13 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 14:58:14 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 14:58:14 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 14:58:15 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 14:58:15 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 14:58:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 14:58:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 14:58:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 14:58:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 14:58:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 14:58:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 14:58:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 14:58:19 GMT
EXPOSE 80
# Thu, 17 Mar 2022 14:58:19 GMT
EXPOSE 443
# Thu, 17 Mar 2022 14:58:20 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 14:58:20 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 14:58:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe387c61070bfe1fbf52bdf2f034ca39f369605473616ebfc4b89287058a395d`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 291.6 KB (291648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bc40a5454d774d40dfddbe6f85673f34aed00cd8e9a3035963763b18376639`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81988b3231106e730dc6c7d0b24ebc84826809dd090bff899495129990559e78`  
		Last Modified: Thu, 17 Mar 2022 15:00:19 GMT  
		Size: 11.1 MB (11125802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd1a3665abdbac555066d2695c45980beba49a104e3a55b2d2cf31f8da4c2da`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5d40c99ca31d7c7cc087a8c0059966c8b9e43f0bafbf525cf4fb1494a45da5b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13833799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde5bec726177426cb4d320b0f016f0a8e4569182c6de303c9c9d042446b6197`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 17:21:06 GMT
ADD file:c25fcf153ea349f64e08a1bd0756ce550f2a081ad56cc40c89027d85d1bc26da in / 
# Thu, 17 Mar 2022 17:21:06 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 18:17:11 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 18:17:12 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 18:17:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 18:17:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 18:17:19 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 18:17:19 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 18:17:20 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 18:17:20 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 18:17:21 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 18:17:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 18:17:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 18:17:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 18:17:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 18:17:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 18:17:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 18:17:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 18:17:25 GMT
EXPOSE 80
# Thu, 17 Mar 2022 18:17:25 GMT
EXPOSE 443
# Thu, 17 Mar 2022 18:17:26 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 18:17:26 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 18:17:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c3a1157c36d8d156f7664fa098212ab2149a64bcb59767cdf4595a86617c17fd`  
		Last Modified: Thu, 17 Mar 2022 17:22:45 GMT  
		Size: 2.4 MB (2430456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376a93fbfdd661b6ba92aa7097c65e646f83c50d150e4227f42141e158b7928b`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 290.6 KB (290632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3bd6226dffa9763d44b0e5688ab7b844b744846e3cc0fa7d8ab6d3c068e466`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9ffbfdd3e888d3f9a94270e0b47ca758645b21ec38f6a203223475052b2802`  
		Last Modified: Thu, 17 Mar 2022 18:19:42 GMT  
		Size: 11.1 MB (11106727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb6dc1be2f2389fa78d2d0002c63575d8d14197e59e0347dbca9ae951a38d4f`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:a4e7a7a9d505b716122bbfb9b41e25b8189dafc8115284279687c2021de7aca1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13751720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a574b32ce3c98bd1848efe2e07ad86e55789b4da7fe02909566fa06a0fdbe6a1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 07:13:27 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 18 Mar 2022 07:13:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 18 Mar 2022 07:13:30 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 18 Mar 2022 07:13:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 18 Mar 2022 07:13:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 18 Mar 2022 07:13:34 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 18 Mar 2022 07:13:35 GMT
ENV XDG_DATA_HOME=/data
# Fri, 18 Mar 2022 07:13:36 GMT
VOLUME [/config]
# Fri, 18 Mar 2022 07:13:37 GMT
VOLUME [/data]
# Fri, 18 Mar 2022 07:13:38 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 18 Mar 2022 07:13:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 18 Mar 2022 07:13:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 18 Mar 2022 07:13:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 18 Mar 2022 07:13:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 18 Mar 2022 07:13:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 18 Mar 2022 07:13:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 18 Mar 2022 07:13:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 18 Mar 2022 07:13:46 GMT
EXPOSE 80
# Fri, 18 Mar 2022 07:13:47 GMT
EXPOSE 443
# Fri, 18 Mar 2022 07:13:48 GMT
EXPOSE 2019
# Fri, 18 Mar 2022 07:13:49 GMT
WORKDIR /srv
# Fri, 18 Mar 2022 07:13:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649e3e65430e0077032ab20dedb081c00e1be3a1f4660b94275f242d1dcd295d`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 291.3 KB (291292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048be0a2d569af2daf2b6cd4728a72f8fecd26611069441023a70b360d3850a0`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 5.8 KB (5751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e382adfd8256a09e2e4bed4c90c8755fc3ee3c58e0679734cd85e4da6ac486`  
		Last Modified: Fri, 18 Mar 2022 07:14:59 GMT  
		Size: 10.7 MB (10738636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d589a4f582ad58b1be3ac310f968793927b5d1629ae84b5c78100265bd825d`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:b91b55c6bdcfe17f047217339ace7c264f76e9011d077d7f84cb4852667273e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13419279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0272ad9824009f684ca3ecddd7e61583b5994b0c08a6db63295222a0dbf8a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 18:18:43 GMT
ADD file:bf9c99d8209e0bed9fd3b62cbe691ebf3829d5a35e63e2b066f1f842577a6d24 in / 
# Thu, 17 Mar 2022 18:18:48 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:30:55 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 21:31:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 21:31:03 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 21:31:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 21:31:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 21:31:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 21:31:22 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 21:31:24 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 21:31:27 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 21:31:29 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 21:31:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 21:31:34 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 21:31:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 21:31:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 21:31:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 21:31:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 21:31:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 21:31:49 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:31:55 GMT
EXPOSE 443
# Thu, 17 Mar 2022 21:31:58 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 21:32:01 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 21:32:03 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8b7e8363a93630a772b70e3cf72231f43c62addae0ee8e507c61d43e3781c4e7`  
		Last Modified: Thu, 17 Mar 2022 18:20:01 GMT  
		Size: 2.8 MB (2817281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e91dcc90eb989323abf507cb545731e08fdb7ae99452318650960f3b2bc29b8`  
		Last Modified: Thu, 17 Mar 2022 21:34:38 GMT  
		Size: 293.7 KB (293720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8763c1a56f6f74d41630bbb545d52602505e99c0e311f1ccfc50c001aa5c705c`  
		Last Modified: Thu, 17 Mar 2022 21:34:37 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e19db97ec3aacb5588ff43135ffccf7eef8281b28c0f3e95f8fa4a4c6e9f554`  
		Last Modified: Thu, 17 Mar 2022 21:34:40 GMT  
		Size: 10.3 MB (10302291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5f036cbadaf9e63bb1584d58115f79a3f4f9fdbce665e25642178129efa74b`  
		Last Modified: Thu, 17 Mar 2022 21:34:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:f710373b7c95e8c39a1e57b06884bac2548574d182889812998295c8b120c1ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14226716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced9b4438f1c256b9508d7d3dbf5048aed06c31b8a05cfbda638e5292d0dee83`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:00:36 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 21:00:37 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 21:00:37 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 21:00:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 21:00:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 21:00:40 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 21:00:40 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 21:00:40 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 21:00:41 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 21:00:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 443
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 21:00:42 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 21:00:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c5df2f20a519a7f78f07f63378f86b2481339dccb5001000518f146e1ef5c0`  
		Last Modified: Thu, 17 Mar 2022 21:01:48 GMT  
		Size: 291.8 KB (291797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6179022673cadc5a23974fa435eaa88fbe3c46ae7f0e61e3a80fa34f7cb6c846`  
		Last Modified: Thu, 17 Mar 2022 21:01:47 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a36f8de1aad1bf91018c94013e0cf58d27a1e6c141c8c11cb4beae1b0aaa78`  
		Last Modified: Thu, 17 Mar 2022 21:01:49 GMT  
		Size: 11.3 MB (11323729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f17a5362f8b342e5c3ac44e83b09ad5a9c93dabbea07012c1a32399962536e`  
		Last Modified: Thu, 17 Mar 2022 21:01:48 GMT  
		Size: 152.0 B  
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
