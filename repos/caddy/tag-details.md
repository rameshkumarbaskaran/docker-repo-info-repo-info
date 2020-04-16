<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `caddy`

-	[`caddy:2.0.0-rc.3`](#caddy200-rc3)
-	[`caddy:2.0.0-rc.3-alpine`](#caddy200-rc3-alpine)
-	[`caddy:2.0.0-rc.3-builder`](#caddy200-rc3-builder)
-	[`caddy:alpine`](#caddyalpine)
-	[`caddy:builder`](#caddybuilder)
-	[`caddy:latest`](#caddylatest)

## `caddy:2.0.0-rc.3`

```console
$ docker pull caddy@sha256:f4b3b3ca127d9fcb3bd877e8d29baec0c80e87a83f1151681ee8df2c067bb4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `caddy:2.0.0-rc.3` - linux; amd64

```console
$ docker pull caddy@sha256:fdcbef33519f6b5860c3dfa4a7b5267266cd37dd6288c40a4d3731af092e7a84
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27094620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a14b8af6e7a6b5d59c4ddbaa92e503d72f04f9a1379dcea1c6af1d7d1650699`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2020 00:19:25 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 16 Apr 2020 00:19:25 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 16 Apr 2020 00:19:27 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Thu, 16 Apr 2020 00:19:27 GMT
ENV CADDY_VERSION=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:19:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='32735a963f946bf561ed2a540192c22ad19565be4bce4bc243c61beae9022ca15a54bf5ef8a5f2341bd3af16fd7b0e9f7832697687201a981a2ac52b0c18ca88' ;; 		armhf)   binArch='armv6'; checksum='5f1485c4be4a050dc12a42d9cc6b0a215a27173eca0bd46c09a0e5ac941b863511f695ca1fad211fb7ebb21e516c549aa2b6d7bc7b11ce3f3729a6c632315937' ;; 		armv7)   binArch='armv7'; checksum='f38d32e6c48f6eb889d7f7bca9ef18d953aeafe8f6ae5b37a657318890c806999dbf4161ac3f5ccb7c6b356ffbded61228e24e6b1ad5e76b3d694923c2483984' ;; 		aarch64) binArch='arm64'; checksum='c4786c030121519ea988ad418878f29b90487357bb434f357955a5ac158460192b4da136fd6d08a2507521a2920412ffa294bf2d83c858c3d1e7fb02de1482a2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0-rc.3/caddy_2.0.0-rc.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 16 Apr 2020 00:19:29 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 16 Apr 2020 00:19:29 GMT
ENV XDG_DATA_HOME=/data
# Thu, 16 Apr 2020 00:19:29 GMT
VOLUME [/config]
# Thu, 16 Apr 2020 00:19:29 GMT
VOLUME [/data]
# Thu, 16 Apr 2020 00:19:29 GMT
LABEL org.opencontainers.image.version=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 16 Apr 2020 00:19:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Apr 2020 00:19:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 16 Apr 2020 00:19:31 GMT
EXPOSE 80
# Thu, 16 Apr 2020 00:19:31 GMT
EXPOSE 443
# Thu, 16 Apr 2020 00:19:31 GMT
EXPOSE 2019
# Thu, 16 Apr 2020 00:19:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c895336717654d7bf50758d2fe590a60610eb7d7168d12c6b6bb9887bae481d`  
		Last Modified: Thu, 16 Apr 2020 00:19:44 GMT  
		Size: 318.6 KB (318556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e769246751713852fe7f4107628f489ad3068e3ef3d9180d8f282591fce3ae2`  
		Last Modified: Thu, 16 Apr 2020 00:19:44 GMT  
		Size: 5.8 KB (5764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5921f47d630c9c7f61bf61ef026a407e71ea4620a63c00d5a0690c74799d409`  
		Last Modified: Thu, 16 Apr 2020 00:19:48 GMT  
		Size: 24.0 MB (23967045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-rc.3` - linux; arm variant v6

```console
$ docker pull caddy@sha256:becd2f8eaa2b3fdfa7368eacb199cd455d874ef5d6f400c1f4c0e2d57f1ba7b0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25835631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2487d38bc455e7c92a16a9eeb0454171f2c7498bb4cfde01babb52e239da5bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2020 00:49:57 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 16 Apr 2020 00:49:58 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 16 Apr 2020 00:50:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Thu, 16 Apr 2020 00:50:02 GMT
ENV CADDY_VERSION=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:50:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='32735a963f946bf561ed2a540192c22ad19565be4bce4bc243c61beae9022ca15a54bf5ef8a5f2341bd3af16fd7b0e9f7832697687201a981a2ac52b0c18ca88' ;; 		armhf)   binArch='armv6'; checksum='5f1485c4be4a050dc12a42d9cc6b0a215a27173eca0bd46c09a0e5ac941b863511f695ca1fad211fb7ebb21e516c549aa2b6d7bc7b11ce3f3729a6c632315937' ;; 		armv7)   binArch='armv7'; checksum='f38d32e6c48f6eb889d7f7bca9ef18d953aeafe8f6ae5b37a657318890c806999dbf4161ac3f5ccb7c6b356ffbded61228e24e6b1ad5e76b3d694923c2483984' ;; 		aarch64) binArch='arm64'; checksum='c4786c030121519ea988ad418878f29b90487357bb434f357955a5ac158460192b4da136fd6d08a2507521a2920412ffa294bf2d83c858c3d1e7fb02de1482a2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0-rc.3/caddy_2.0.0-rc.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 16 Apr 2020 00:50:08 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 16 Apr 2020 00:50:08 GMT
ENV XDG_DATA_HOME=/data
# Thu, 16 Apr 2020 00:50:09 GMT
VOLUME [/config]
# Thu, 16 Apr 2020 00:50:11 GMT
VOLUME [/data]
# Thu, 16 Apr 2020 00:50:12 GMT
LABEL org.opencontainers.image.version=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:50:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 16 Apr 2020 00:50:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 16 Apr 2020 00:50:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 16 Apr 2020 00:50:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 16 Apr 2020 00:50:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 16 Apr 2020 00:50:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Apr 2020 00:50:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 16 Apr 2020 00:50:19 GMT
EXPOSE 80
# Thu, 16 Apr 2020 00:50:20 GMT
EXPOSE 443
# Thu, 16 Apr 2020 00:50:21 GMT
EXPOSE 2019
# Thu, 16 Apr 2020 00:50:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4dda4ab56a13a1d8bae586f3c1118bd9d862c2f1245928f3ab1cffbd09b287`  
		Last Modified: Thu, 16 Apr 2020 00:50:50 GMT  
		Size: 319.0 KB (318952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6306a8bbb774718ea961cd8c24fb370aacb34e1268a6868d8964821419f130d7`  
		Last Modified: Thu, 16 Apr 2020 00:50:50 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9edb5046889b030fa7fd4163c6c0bbdf7bbc89cc299e5fbb0c8dfb8cc12ace5`  
		Last Modified: Thu, 16 Apr 2020 00:50:56 GMT  
		Size: 22.9 MB (22892256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-rc.3` - linux; arm variant v7

```console
$ docker pull caddy@sha256:08ff30aa19db485ae78a08aefaaebe799c92065919a763dba28a73b80decdd0d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25590001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f831f3050f23cc577f83227575cdbdb8353e784dcff2a6bdb3e1c4832d8f14e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2020 23:57:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 15 Apr 2020 23:57:32 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Wed, 15 Apr 2020 23:57:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 15 Apr 2020 23:57:35 GMT
ENV CADDY_VERSION=v2.0.0-rc.3
# Wed, 15 Apr 2020 23:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='32735a963f946bf561ed2a540192c22ad19565be4bce4bc243c61beae9022ca15a54bf5ef8a5f2341bd3af16fd7b0e9f7832697687201a981a2ac52b0c18ca88' ;; 		armhf)   binArch='armv6'; checksum='5f1485c4be4a050dc12a42d9cc6b0a215a27173eca0bd46c09a0e5ac941b863511f695ca1fad211fb7ebb21e516c549aa2b6d7bc7b11ce3f3729a6c632315937' ;; 		armv7)   binArch='armv7'; checksum='f38d32e6c48f6eb889d7f7bca9ef18d953aeafe8f6ae5b37a657318890c806999dbf4161ac3f5ccb7c6b356ffbded61228e24e6b1ad5e76b3d694923c2483984' ;; 		aarch64) binArch='arm64'; checksum='c4786c030121519ea988ad418878f29b90487357bb434f357955a5ac158460192b4da136fd6d08a2507521a2920412ffa294bf2d83c858c3d1e7fb02de1482a2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0-rc.3/caddy_2.0.0-rc.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Apr 2020 23:57:40 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Apr 2020 23:57:40 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Apr 2020 23:57:41 GMT
VOLUME [/config]
# Wed, 15 Apr 2020 23:57:41 GMT
VOLUME [/data]
# Wed, 15 Apr 2020 23:57:42 GMT
LABEL org.opencontainers.image.version=v2.0.0-rc.3
# Wed, 15 Apr 2020 23:57:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Apr 2020 23:57:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Apr 2020 23:57:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Apr 2020 23:57:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Apr 2020 23:57:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Apr 2020 23:57:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Apr 2020 23:57:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Apr 2020 23:57:47 GMT
EXPOSE 80
# Wed, 15 Apr 2020 23:57:47 GMT
EXPOSE 443
# Wed, 15 Apr 2020 23:57:48 GMT
EXPOSE 2019
# Wed, 15 Apr 2020 23:57:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befe79730f9213596c0cab32a77e4953596a1ab545ac79f04785bcb1ace48909`  
		Last Modified: Wed, 15 Apr 2020 23:58:08 GMT  
		Size: 317.9 KB (317897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091b38b8a06e74dc8370527ea85371538a5e02941ce9c603152ab6b32c8d61e7`  
		Last Modified: Wed, 15 Apr 2020 23:58:08 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfda26ce91738c36e69d3129c33bb4aac26edc7e7c9af92747178ddfa17d1b4`  
		Last Modified: Wed, 15 Apr 2020 23:58:13 GMT  
		Size: 22.8 MB (22845766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-rc.3` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:e30cf81584606a40e151d611e1dbabc3825c94f3fe9a301ad5b3c57a6c08c983
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25109967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed743ddd2d7af716e9b6ef9cd857b3caed9c902627777847c952518d65b662c3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2020 00:39:33 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 16 Apr 2020 00:39:33 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 16 Apr 2020 00:39:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Thu, 16 Apr 2020 00:39:36 GMT
ENV CADDY_VERSION=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:39:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='32735a963f946bf561ed2a540192c22ad19565be4bce4bc243c61beae9022ca15a54bf5ef8a5f2341bd3af16fd7b0e9f7832697687201a981a2ac52b0c18ca88' ;; 		armhf)   binArch='armv6'; checksum='5f1485c4be4a050dc12a42d9cc6b0a215a27173eca0bd46c09a0e5ac941b863511f695ca1fad211fb7ebb21e516c549aa2b6d7bc7b11ce3f3729a6c632315937' ;; 		armv7)   binArch='armv7'; checksum='f38d32e6c48f6eb889d7f7bca9ef18d953aeafe8f6ae5b37a657318890c806999dbf4161ac3f5ccb7c6b356ffbded61228e24e6b1ad5e76b3d694923c2483984' ;; 		aarch64) binArch='arm64'; checksum='c4786c030121519ea988ad418878f29b90487357bb434f357955a5ac158460192b4da136fd6d08a2507521a2920412ffa294bf2d83c858c3d1e7fb02de1482a2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0-rc.3/caddy_2.0.0-rc.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 16 Apr 2020 00:39:40 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 16 Apr 2020 00:39:41 GMT
ENV XDG_DATA_HOME=/data
# Thu, 16 Apr 2020 00:39:42 GMT
VOLUME [/config]
# Thu, 16 Apr 2020 00:39:42 GMT
VOLUME [/data]
# Thu, 16 Apr 2020 00:39:43 GMT
LABEL org.opencontainers.image.version=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:39:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 16 Apr 2020 00:39:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 16 Apr 2020 00:39:45 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 16 Apr 2020 00:39:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 16 Apr 2020 00:39:46 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 16 Apr 2020 00:39:47 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Apr 2020 00:39:47 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 16 Apr 2020 00:39:48 GMT
EXPOSE 80
# Thu, 16 Apr 2020 00:39:48 GMT
EXPOSE 443
# Thu, 16 Apr 2020 00:39:49 GMT
EXPOSE 2019
# Thu, 16 Apr 2020 00:39:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8769f63ec8b31f05ebb26b0a58d55301ef35d1449a5f401e24fbd8fc966bfd21`  
		Last Modified: Thu, 16 Apr 2020 00:40:10 GMT  
		Size: 319.1 KB (319126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faaac47c6de0ab38444a53999b472ae63772dbb66155e37fc5014ee3f99d596e`  
		Last Modified: Thu, 16 Apr 2020 00:40:10 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4532cc514c5332376487a299a4f52a7863b1aaff5262f88777f86167d2e4bcd`  
		Last Modified: Thu, 16 Apr 2020 00:40:15 GMT  
		Size: 22.1 MB (22061857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.0.0-rc.3-alpine`

```console
$ docker pull caddy@sha256:f4b3b3ca127d9fcb3bd877e8d29baec0c80e87a83f1151681ee8df2c067bb4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `caddy:2.0.0-rc.3-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:fdcbef33519f6b5860c3dfa4a7b5267266cd37dd6288c40a4d3731af092e7a84
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27094620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a14b8af6e7a6b5d59c4ddbaa92e503d72f04f9a1379dcea1c6af1d7d1650699`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2020 00:19:25 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 16 Apr 2020 00:19:25 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 16 Apr 2020 00:19:27 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Thu, 16 Apr 2020 00:19:27 GMT
ENV CADDY_VERSION=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:19:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='32735a963f946bf561ed2a540192c22ad19565be4bce4bc243c61beae9022ca15a54bf5ef8a5f2341bd3af16fd7b0e9f7832697687201a981a2ac52b0c18ca88' ;; 		armhf)   binArch='armv6'; checksum='5f1485c4be4a050dc12a42d9cc6b0a215a27173eca0bd46c09a0e5ac941b863511f695ca1fad211fb7ebb21e516c549aa2b6d7bc7b11ce3f3729a6c632315937' ;; 		armv7)   binArch='armv7'; checksum='f38d32e6c48f6eb889d7f7bca9ef18d953aeafe8f6ae5b37a657318890c806999dbf4161ac3f5ccb7c6b356ffbded61228e24e6b1ad5e76b3d694923c2483984' ;; 		aarch64) binArch='arm64'; checksum='c4786c030121519ea988ad418878f29b90487357bb434f357955a5ac158460192b4da136fd6d08a2507521a2920412ffa294bf2d83c858c3d1e7fb02de1482a2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0-rc.3/caddy_2.0.0-rc.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 16 Apr 2020 00:19:29 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 16 Apr 2020 00:19:29 GMT
ENV XDG_DATA_HOME=/data
# Thu, 16 Apr 2020 00:19:29 GMT
VOLUME [/config]
# Thu, 16 Apr 2020 00:19:29 GMT
VOLUME [/data]
# Thu, 16 Apr 2020 00:19:29 GMT
LABEL org.opencontainers.image.version=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 16 Apr 2020 00:19:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Apr 2020 00:19:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 16 Apr 2020 00:19:31 GMT
EXPOSE 80
# Thu, 16 Apr 2020 00:19:31 GMT
EXPOSE 443
# Thu, 16 Apr 2020 00:19:31 GMT
EXPOSE 2019
# Thu, 16 Apr 2020 00:19:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c895336717654d7bf50758d2fe590a60610eb7d7168d12c6b6bb9887bae481d`  
		Last Modified: Thu, 16 Apr 2020 00:19:44 GMT  
		Size: 318.6 KB (318556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e769246751713852fe7f4107628f489ad3068e3ef3d9180d8f282591fce3ae2`  
		Last Modified: Thu, 16 Apr 2020 00:19:44 GMT  
		Size: 5.8 KB (5764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5921f47d630c9c7f61bf61ef026a407e71ea4620a63c00d5a0690c74799d409`  
		Last Modified: Thu, 16 Apr 2020 00:19:48 GMT  
		Size: 24.0 MB (23967045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-rc.3-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:becd2f8eaa2b3fdfa7368eacb199cd455d874ef5d6f400c1f4c0e2d57f1ba7b0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25835631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2487d38bc455e7c92a16a9eeb0454171f2c7498bb4cfde01babb52e239da5bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2020 00:49:57 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 16 Apr 2020 00:49:58 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 16 Apr 2020 00:50:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Thu, 16 Apr 2020 00:50:02 GMT
ENV CADDY_VERSION=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:50:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='32735a963f946bf561ed2a540192c22ad19565be4bce4bc243c61beae9022ca15a54bf5ef8a5f2341bd3af16fd7b0e9f7832697687201a981a2ac52b0c18ca88' ;; 		armhf)   binArch='armv6'; checksum='5f1485c4be4a050dc12a42d9cc6b0a215a27173eca0bd46c09a0e5ac941b863511f695ca1fad211fb7ebb21e516c549aa2b6d7bc7b11ce3f3729a6c632315937' ;; 		armv7)   binArch='armv7'; checksum='f38d32e6c48f6eb889d7f7bca9ef18d953aeafe8f6ae5b37a657318890c806999dbf4161ac3f5ccb7c6b356ffbded61228e24e6b1ad5e76b3d694923c2483984' ;; 		aarch64) binArch='arm64'; checksum='c4786c030121519ea988ad418878f29b90487357bb434f357955a5ac158460192b4da136fd6d08a2507521a2920412ffa294bf2d83c858c3d1e7fb02de1482a2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0-rc.3/caddy_2.0.0-rc.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 16 Apr 2020 00:50:08 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 16 Apr 2020 00:50:08 GMT
ENV XDG_DATA_HOME=/data
# Thu, 16 Apr 2020 00:50:09 GMT
VOLUME [/config]
# Thu, 16 Apr 2020 00:50:11 GMT
VOLUME [/data]
# Thu, 16 Apr 2020 00:50:12 GMT
LABEL org.opencontainers.image.version=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:50:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 16 Apr 2020 00:50:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 16 Apr 2020 00:50:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 16 Apr 2020 00:50:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 16 Apr 2020 00:50:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 16 Apr 2020 00:50:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Apr 2020 00:50:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 16 Apr 2020 00:50:19 GMT
EXPOSE 80
# Thu, 16 Apr 2020 00:50:20 GMT
EXPOSE 443
# Thu, 16 Apr 2020 00:50:21 GMT
EXPOSE 2019
# Thu, 16 Apr 2020 00:50:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4dda4ab56a13a1d8bae586f3c1118bd9d862c2f1245928f3ab1cffbd09b287`  
		Last Modified: Thu, 16 Apr 2020 00:50:50 GMT  
		Size: 319.0 KB (318952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6306a8bbb774718ea961cd8c24fb370aacb34e1268a6868d8964821419f130d7`  
		Last Modified: Thu, 16 Apr 2020 00:50:50 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9edb5046889b030fa7fd4163c6c0bbdf7bbc89cc299e5fbb0c8dfb8cc12ace5`  
		Last Modified: Thu, 16 Apr 2020 00:50:56 GMT  
		Size: 22.9 MB (22892256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-rc.3-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:08ff30aa19db485ae78a08aefaaebe799c92065919a763dba28a73b80decdd0d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25590001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f831f3050f23cc577f83227575cdbdb8353e784dcff2a6bdb3e1c4832d8f14e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2020 23:57:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 15 Apr 2020 23:57:32 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Wed, 15 Apr 2020 23:57:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 15 Apr 2020 23:57:35 GMT
ENV CADDY_VERSION=v2.0.0-rc.3
# Wed, 15 Apr 2020 23:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='32735a963f946bf561ed2a540192c22ad19565be4bce4bc243c61beae9022ca15a54bf5ef8a5f2341bd3af16fd7b0e9f7832697687201a981a2ac52b0c18ca88' ;; 		armhf)   binArch='armv6'; checksum='5f1485c4be4a050dc12a42d9cc6b0a215a27173eca0bd46c09a0e5ac941b863511f695ca1fad211fb7ebb21e516c549aa2b6d7bc7b11ce3f3729a6c632315937' ;; 		armv7)   binArch='armv7'; checksum='f38d32e6c48f6eb889d7f7bca9ef18d953aeafe8f6ae5b37a657318890c806999dbf4161ac3f5ccb7c6b356ffbded61228e24e6b1ad5e76b3d694923c2483984' ;; 		aarch64) binArch='arm64'; checksum='c4786c030121519ea988ad418878f29b90487357bb434f357955a5ac158460192b4da136fd6d08a2507521a2920412ffa294bf2d83c858c3d1e7fb02de1482a2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0-rc.3/caddy_2.0.0-rc.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Apr 2020 23:57:40 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Apr 2020 23:57:40 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Apr 2020 23:57:41 GMT
VOLUME [/config]
# Wed, 15 Apr 2020 23:57:41 GMT
VOLUME [/data]
# Wed, 15 Apr 2020 23:57:42 GMT
LABEL org.opencontainers.image.version=v2.0.0-rc.3
# Wed, 15 Apr 2020 23:57:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Apr 2020 23:57:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Apr 2020 23:57:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Apr 2020 23:57:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Apr 2020 23:57:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Apr 2020 23:57:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Apr 2020 23:57:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Apr 2020 23:57:47 GMT
EXPOSE 80
# Wed, 15 Apr 2020 23:57:47 GMT
EXPOSE 443
# Wed, 15 Apr 2020 23:57:48 GMT
EXPOSE 2019
# Wed, 15 Apr 2020 23:57:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befe79730f9213596c0cab32a77e4953596a1ab545ac79f04785bcb1ace48909`  
		Last Modified: Wed, 15 Apr 2020 23:58:08 GMT  
		Size: 317.9 KB (317897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091b38b8a06e74dc8370527ea85371538a5e02941ce9c603152ab6b32c8d61e7`  
		Last Modified: Wed, 15 Apr 2020 23:58:08 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfda26ce91738c36e69d3129c33bb4aac26edc7e7c9af92747178ddfa17d1b4`  
		Last Modified: Wed, 15 Apr 2020 23:58:13 GMT  
		Size: 22.8 MB (22845766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-rc.3-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:e30cf81584606a40e151d611e1dbabc3825c94f3fe9a301ad5b3c57a6c08c983
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25109967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed743ddd2d7af716e9b6ef9cd857b3caed9c902627777847c952518d65b662c3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2020 00:39:33 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 16 Apr 2020 00:39:33 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 16 Apr 2020 00:39:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Thu, 16 Apr 2020 00:39:36 GMT
ENV CADDY_VERSION=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:39:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='32735a963f946bf561ed2a540192c22ad19565be4bce4bc243c61beae9022ca15a54bf5ef8a5f2341bd3af16fd7b0e9f7832697687201a981a2ac52b0c18ca88' ;; 		armhf)   binArch='armv6'; checksum='5f1485c4be4a050dc12a42d9cc6b0a215a27173eca0bd46c09a0e5ac941b863511f695ca1fad211fb7ebb21e516c549aa2b6d7bc7b11ce3f3729a6c632315937' ;; 		armv7)   binArch='armv7'; checksum='f38d32e6c48f6eb889d7f7bca9ef18d953aeafe8f6ae5b37a657318890c806999dbf4161ac3f5ccb7c6b356ffbded61228e24e6b1ad5e76b3d694923c2483984' ;; 		aarch64) binArch='arm64'; checksum='c4786c030121519ea988ad418878f29b90487357bb434f357955a5ac158460192b4da136fd6d08a2507521a2920412ffa294bf2d83c858c3d1e7fb02de1482a2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0-rc.3/caddy_2.0.0-rc.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 16 Apr 2020 00:39:40 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 16 Apr 2020 00:39:41 GMT
ENV XDG_DATA_HOME=/data
# Thu, 16 Apr 2020 00:39:42 GMT
VOLUME [/config]
# Thu, 16 Apr 2020 00:39:42 GMT
VOLUME [/data]
# Thu, 16 Apr 2020 00:39:43 GMT
LABEL org.opencontainers.image.version=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:39:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 16 Apr 2020 00:39:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 16 Apr 2020 00:39:45 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 16 Apr 2020 00:39:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 16 Apr 2020 00:39:46 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 16 Apr 2020 00:39:47 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Apr 2020 00:39:47 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 16 Apr 2020 00:39:48 GMT
EXPOSE 80
# Thu, 16 Apr 2020 00:39:48 GMT
EXPOSE 443
# Thu, 16 Apr 2020 00:39:49 GMT
EXPOSE 2019
# Thu, 16 Apr 2020 00:39:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8769f63ec8b31f05ebb26b0a58d55301ef35d1449a5f401e24fbd8fc966bfd21`  
		Last Modified: Thu, 16 Apr 2020 00:40:10 GMT  
		Size: 319.1 KB (319126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faaac47c6de0ab38444a53999b472ae63772dbb66155e37fc5014ee3f99d596e`  
		Last Modified: Thu, 16 Apr 2020 00:40:10 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4532cc514c5332376487a299a4f52a7863b1aaff5262f88777f86167d2e4bcd`  
		Last Modified: Thu, 16 Apr 2020 00:40:15 GMT  
		Size: 22.1 MB (22061857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.0.0-rc.3-builder`

```console
$ docker pull caddy@sha256:7896c2b5e9fa3b33e2c661c68b2541a63474efb08cd204fdf20e48ab7ad89a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `caddy:2.0.0-rc.3-builder` - linux; amd64

```console
$ docker pull caddy@sha256:486d86fe70265203228afb9b9e6e7934019090c6686da9a9fb98579931a05778
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322863984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fd06ca5bdeb1a36375ba63a93a06401045ebb7a6154830e973a6de5949242b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:02:02 GMT
RUN apk add --no-cache 		ca-certificates
# Mon, 23 Mar 2020 23:02:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 08 Apr 2020 23:06:10 GMT
ENV GOLANG_VERSION=1.14.2
# Wed, 08 Apr 2020 23:11:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '98de84e69726a66da7b4e58eac41b99cbe274d7e8906eeb8a5b7eb0aadee7f7c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Wed, 08 Apr 2020 23:11:13 GMT
ENV GOPATH=/go
# Wed, 08 Apr 2020 23:11:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2020 23:11:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 08 Apr 2020 23:11:16 GMT
WORKDIR /go
# Mon, 13 Apr 2020 23:43:21 GMT
WORKDIR /src
# Mon, 13 Apr 2020 23:43:23 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 13 Apr 2020 23:43:24 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0-rc.3
# Mon, 13 Apr 2020 23:43:27 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Mon, 13 Apr 2020 23:43:27 GMT
WORKDIR /src/caddy/cmd/caddy
# Mon, 13 Apr 2020 23:43:57 GMT
RUN go get -d ./...
# Mon, 13 Apr 2020 23:43:59 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Mon, 13 Apr 2020 23:43:59 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c732a2540651eb09faab95b03b3b5928ab23e096fae0006bdc2abf9e0cb5bfb4`  
		Last Modified: Mon, 23 Mar 2020 23:13:03 GMT  
		Size: 301.3 KB (301283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2225181d6bcfb7877529a7257ff207cb14e52831420f770cbc2187031b6228`  
		Last Modified: Mon, 23 Mar 2020 23:13:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdfa13e5b48c976ba308826b27a4978c2ffe6833efcfcfc0bd40dbf25e88455`  
		Last Modified: Wed, 08 Apr 2020 23:26:23 GMT  
		Size: 132.0 MB (132012220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c48a539365d2d572e18de4a42ab11b02d9870a17bf1f65160d7fcbbd0423263`  
		Last Modified: Wed, 08 Apr 2020 23:25:47 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947fdad36c6d1e2fd7b618aa1a49dfabaa1ff9d6fb85a195e2437c2b9ac78142`  
		Last Modified: Mon, 13 Apr 2020 23:44:26 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199e6b2236a218d72efd03fc1fa0971c00c87439722e1a40269b7edfd910b79`  
		Last Modified: Mon, 13 Apr 2020 23:44:28 GMT  
		Size: 8.2 MB (8155831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732862f7439776bbe7cc313ed1e10454506f168429234c0daea17d6c48a9692`  
		Last Modified: Mon, 13 Apr 2020 23:44:26 GMT  
		Size: 2.7 MB (2744273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d54fb1573600e831b250c83cb9dc699bab8aa12040568d9ee542fb8d09c1d99`  
		Last Modified: Mon, 13 Apr 2020 23:45:02 GMT  
		Size: 176.8 MB (176846093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e336ec02e20348f57d1ef8151ecfcd216777f5489f01b29164883ec496bcbb`  
		Last Modified: Mon, 13 Apr 2020 23:44:25 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6f8a2da1c847ae8cd10d1f3e37ad75cc0ba17c5e9b4f7e68fdd3b7cffb5482`  
		Last Modified: Mon, 13 Apr 2020 23:44:25 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-rc.3-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:cd2ad079bba5bd32e34425b4e582e403c8da0794d75cd9532089e397d6a6a6fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318283866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f1e47fec82e99b063b602e73e298a78f88206130b99dc09f5ce6d996c4b546`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:09:39 GMT
RUN apk add --no-cache 		ca-certificates
# Mon, 23 Mar 2020 22:09:41 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 08 Apr 2020 23:05:33 GMT
ENV GOLANG_VERSION=1.14.2
# Wed, 08 Apr 2020 23:08:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '98de84e69726a66da7b4e58eac41b99cbe274d7e8906eeb8a5b7eb0aadee7f7c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Wed, 08 Apr 2020 23:08:51 GMT
ENV GOPATH=/go
# Wed, 08 Apr 2020 23:08:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2020 23:08:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 08 Apr 2020 23:08:54 GMT
WORKDIR /go
# Tue, 14 Apr 2020 19:02:05 GMT
WORKDIR /src
# Tue, 14 Apr 2020 19:02:09 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 14 Apr 2020 19:02:10 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0-rc.3
# Tue, 14 Apr 2020 19:02:14 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 14 Apr 2020 19:02:16 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 14 Apr 2020 19:03:36 GMT
RUN go get -d ./...
# Tue, 14 Apr 2020 19:03:40 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Tue, 14 Apr 2020 19:03:41 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7800bd79b91213697a2858807a07e49702e4e0f15365c4c7ff9d4e4a702a9c41`  
		Last Modified: Mon, 23 Mar 2020 22:57:54 GMT  
		Size: 301.6 KB (301626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd98a07237762fc6acaab52f9eb58cbea968ed7f0830c02e87622d6f777456e`  
		Last Modified: Mon, 23 Mar 2020 22:57:54 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d32447fdb8339cdd3fde9b708d14fff501271a9f8ff970a75bb23454bcfab8`  
		Last Modified: Wed, 08 Apr 2020 23:17:23 GMT  
		Size: 128.1 MB (128149579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351ec32b9e5337dfc6bdd6204b76587028f2cf530e51bb7f0379908cd3a9e3bb`  
		Last Modified: Wed, 08 Apr 2020 23:15:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a743cd83ba00508dd353a743708e6e434e2f56a1abdc6f2156d953839d646a1`  
		Last Modified: Tue, 14 Apr 2020 19:04:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04790f6bc405f18e7cedfbf754285f13c69997c89558c211e920c8b1e99e99fb`  
		Last Modified: Tue, 14 Apr 2020 19:04:14 GMT  
		Size: 7.8 MB (7777224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7916ea4abf152652f304cc659eb5f49cdeb18bcfa4b08da8121c7cb926618d5f`  
		Last Modified: Tue, 14 Apr 2020 19:04:08 GMT  
		Size: 2.6 MB (2583942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017e0a0855a5b5caab47f0cf399468d8ddee95fcc2a96bb1dba8ef9de6490f41`  
		Last Modified: Tue, 14 Apr 2020 19:04:53 GMT  
		Size: 176.9 MB (176851792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd412eceac3544008060ba63d1877dfa7e7652e3495fa90d754dcf0a515480d`  
		Last Modified: Tue, 14 Apr 2020 19:04:07 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fcea70e4e7db2fed8fb230f66d27fc46446054a0cdc6f6a342235480e7a248`  
		Last Modified: Tue, 14 Apr 2020 19:04:07 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-rc.3-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c6b2f1f5d52cfbabf244af757effe7b6ddc142acdb15ef5d8dc7452a9659b795
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.9 MB (316942094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516ec248376a670b87153cbe61efb69b30615826ae2ec1ee48034a951a771e92`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:47:15 GMT
RUN apk add --no-cache 		ca-certificates
# Mon, 23 Mar 2020 23:47:17 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 08 Apr 2020 23:11:43 GMT
ENV GOLANG_VERSION=1.14.2
# Wed, 08 Apr 2020 23:14:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '98de84e69726a66da7b4e58eac41b99cbe274d7e8906eeb8a5b7eb0aadee7f7c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Wed, 08 Apr 2020 23:14:23 GMT
ENV GOPATH=/go
# Wed, 08 Apr 2020 23:14:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2020 23:14:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 08 Apr 2020 23:14:31 GMT
WORKDIR /go
# Tue, 14 Apr 2020 19:02:05 GMT
WORKDIR /src
# Tue, 14 Apr 2020 19:02:09 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 14 Apr 2020 19:02:10 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0-rc.3
# Tue, 14 Apr 2020 19:02:15 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 14 Apr 2020 19:02:17 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 14 Apr 2020 19:03:31 GMT
RUN go get -d ./...
# Tue, 14 Apr 2020 19:03:39 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Tue, 14 Apr 2020 19:03:41 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0c66f8509bb56e1ead748baf3433dcad3c1fa170146d5d7d06506b9a80f367`  
		Last Modified: Mon, 23 Mar 2020 23:53:18 GMT  
		Size: 300.6 KB (300602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf5f16b98b20e6e4f07e24e93de1018e88310a49963dc147c370d360a02fdbb`  
		Last Modified: Mon, 23 Mar 2020 23:53:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a38fd97575c34aedd91676d7643f6dbf66a1bca83f7d010e631807b96dae74`  
		Last Modified: Wed, 08 Apr 2020 23:25:03 GMT  
		Size: 127.8 MB (127774109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61bd435de55167e1a5a8cbdd73838375b819c98df2c23be5991140c00cbfd9a`  
		Last Modified: Wed, 08 Apr 2020 23:24:26 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a743cd83ba00508dd353a743708e6e434e2f56a1abdc6f2156d953839d646a1`  
		Last Modified: Tue, 14 Apr 2020 19:04:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8928c849f33d759a505e159745da8960d19460b8735d7a08631ee817549c57d5`  
		Last Modified: Tue, 14 Apr 2020 19:04:11 GMT  
		Size: 7.0 MB (7010480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fe4dbb3884a7fa0c551818da659e9c4d3f97f13eb6d53634655e97f9bd2f0d`  
		Last Modified: Tue, 14 Apr 2020 19:04:10 GMT  
		Size: 2.6 MB (2584042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb4bc7d74da5ae926bd30beea4c4abe59b6c0bb76705fb4f6b83391b591ecd7`  
		Last Modified: Tue, 14 Apr 2020 19:04:53 GMT  
		Size: 176.9 MB (176851243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fb3f4c0251d63ed371fb8a24333c2d9f9dada8830bad6af323550a4276f828`  
		Last Modified: Tue, 14 Apr 2020 19:04:09 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fcea70e4e7db2fed8fb230f66d27fc46446054a0cdc6f6a342235480e7a248`  
		Last Modified: Tue, 14 Apr 2020 19:04:07 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.0.0-rc.3-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:75a990032363651bf7b39167b9e44e70cb8e6d4ae814545a2274a74005ce8660
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.2 MB (317221628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb140d2ac2499d88e26b91f2219f57edca78ae1597261d9799cb9519bf9f2e24`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:58:12 GMT
RUN apk add --no-cache 		ca-certificates
# Mon, 23 Mar 2020 22:58:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 08 Apr 2020 23:11:00 GMT
ENV GOLANG_VERSION=1.14.2
# Wed, 08 Apr 2020 23:13:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '98de84e69726a66da7b4e58eac41b99cbe274d7e8906eeb8a5b7eb0aadee7f7c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Wed, 08 Apr 2020 23:13:19 GMT
ENV GOPATH=/go
# Wed, 08 Apr 2020 23:13:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2020 23:13:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 08 Apr 2020 23:13:22 GMT
WORKDIR /go
# Tue, 14 Apr 2020 19:02:03 GMT
WORKDIR /src
# Tue, 14 Apr 2020 19:02:07 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 14 Apr 2020 19:02:08 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0-rc.3
# Tue, 14 Apr 2020 19:02:12 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 14 Apr 2020 19:02:13 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 14 Apr 2020 19:03:13 GMT
RUN go get -d ./...
# Tue, 14 Apr 2020 19:03:15 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Tue, 14 Apr 2020 19:03:21 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42d4106c43952870e20bfb808275012c22e6244af6eff1e916f446f7d338d0d`  
		Last Modified: Mon, 23 Mar 2020 23:03:34 GMT  
		Size: 301.8 KB (301778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f0a4e33d457336c22ac08eaec4609be330959ccdfefdb342be1045df4d26f0`  
		Last Modified: Mon, 23 Mar 2020 23:03:34 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44acbbdbf71f1d00fa6d0011bb10b82bef26b421a579bcf3a3491dced9f8233e`  
		Last Modified: Wed, 08 Apr 2020 23:21:31 GMT  
		Size: 126.4 MB (126405787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d054599df8f57e1578fdc2c554a9ac6124bf04f808dc623ef7f6548230fa3b5f`  
		Last Modified: Wed, 08 Apr 2020 23:20:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcee4e573bebbed33479e125fd8abf1f3debd0a7aee2137f55b67d9c38a79be`  
		Last Modified: Tue, 14 Apr 2020 19:03:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968260b321a071a55eb891faac5f738bc2c3340a7843fc9ebd092902475f6fb3`  
		Last Modified: Tue, 14 Apr 2020 19:03:59 GMT  
		Size: 8.4 MB (8353090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f7e47a5a4e440d1d8c40f1b42638e70ea0fbf9b5635f0145f58768993763d6`  
		Last Modified: Tue, 14 Apr 2020 19:03:57 GMT  
		Size: 2.6 MB (2584029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e682841e5eb376ed223cc26d628878cb76d53d943e6f205310f7294f212717`  
		Last Modified: Tue, 14 Apr 2020 19:04:33 GMT  
		Size: 176.9 MB (176852681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffdb1a37f36e66ea176ba211db0396ddcf52e5c11bc8c335ad3814c1f091f33`  
		Last Modified: Tue, 14 Apr 2020 19:03:58 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d540e0414cc6a26d9aed38f141af756f0c60e88bb278d4807bda8d6b5939314`  
		Last Modified: Tue, 14 Apr 2020 19:03:57 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:alpine`

```console
$ docker pull caddy@sha256:f4b3b3ca127d9fcb3bd877e8d29baec0c80e87a83f1151681ee8df2c067bb4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `caddy:alpine` - linux; amd64

```console
$ docker pull caddy@sha256:fdcbef33519f6b5860c3dfa4a7b5267266cd37dd6288c40a4d3731af092e7a84
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27094620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a14b8af6e7a6b5d59c4ddbaa92e503d72f04f9a1379dcea1c6af1d7d1650699`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2020 00:19:25 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 16 Apr 2020 00:19:25 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 16 Apr 2020 00:19:27 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Thu, 16 Apr 2020 00:19:27 GMT
ENV CADDY_VERSION=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:19:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='32735a963f946bf561ed2a540192c22ad19565be4bce4bc243c61beae9022ca15a54bf5ef8a5f2341bd3af16fd7b0e9f7832697687201a981a2ac52b0c18ca88' ;; 		armhf)   binArch='armv6'; checksum='5f1485c4be4a050dc12a42d9cc6b0a215a27173eca0bd46c09a0e5ac941b863511f695ca1fad211fb7ebb21e516c549aa2b6d7bc7b11ce3f3729a6c632315937' ;; 		armv7)   binArch='armv7'; checksum='f38d32e6c48f6eb889d7f7bca9ef18d953aeafe8f6ae5b37a657318890c806999dbf4161ac3f5ccb7c6b356ffbded61228e24e6b1ad5e76b3d694923c2483984' ;; 		aarch64) binArch='arm64'; checksum='c4786c030121519ea988ad418878f29b90487357bb434f357955a5ac158460192b4da136fd6d08a2507521a2920412ffa294bf2d83c858c3d1e7fb02de1482a2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0-rc.3/caddy_2.0.0-rc.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 16 Apr 2020 00:19:29 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 16 Apr 2020 00:19:29 GMT
ENV XDG_DATA_HOME=/data
# Thu, 16 Apr 2020 00:19:29 GMT
VOLUME [/config]
# Thu, 16 Apr 2020 00:19:29 GMT
VOLUME [/data]
# Thu, 16 Apr 2020 00:19:29 GMT
LABEL org.opencontainers.image.version=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 16 Apr 2020 00:19:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Apr 2020 00:19:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 16 Apr 2020 00:19:31 GMT
EXPOSE 80
# Thu, 16 Apr 2020 00:19:31 GMT
EXPOSE 443
# Thu, 16 Apr 2020 00:19:31 GMT
EXPOSE 2019
# Thu, 16 Apr 2020 00:19:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c895336717654d7bf50758d2fe590a60610eb7d7168d12c6b6bb9887bae481d`  
		Last Modified: Thu, 16 Apr 2020 00:19:44 GMT  
		Size: 318.6 KB (318556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e769246751713852fe7f4107628f489ad3068e3ef3d9180d8f282591fce3ae2`  
		Last Modified: Thu, 16 Apr 2020 00:19:44 GMT  
		Size: 5.8 KB (5764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5921f47d630c9c7f61bf61ef026a407e71ea4620a63c00d5a0690c74799d409`  
		Last Modified: Thu, 16 Apr 2020 00:19:48 GMT  
		Size: 24.0 MB (23967045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:becd2f8eaa2b3fdfa7368eacb199cd455d874ef5d6f400c1f4c0e2d57f1ba7b0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25835631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2487d38bc455e7c92a16a9eeb0454171f2c7498bb4cfde01babb52e239da5bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2020 00:49:57 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 16 Apr 2020 00:49:58 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 16 Apr 2020 00:50:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Thu, 16 Apr 2020 00:50:02 GMT
ENV CADDY_VERSION=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:50:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='32735a963f946bf561ed2a540192c22ad19565be4bce4bc243c61beae9022ca15a54bf5ef8a5f2341bd3af16fd7b0e9f7832697687201a981a2ac52b0c18ca88' ;; 		armhf)   binArch='armv6'; checksum='5f1485c4be4a050dc12a42d9cc6b0a215a27173eca0bd46c09a0e5ac941b863511f695ca1fad211fb7ebb21e516c549aa2b6d7bc7b11ce3f3729a6c632315937' ;; 		armv7)   binArch='armv7'; checksum='f38d32e6c48f6eb889d7f7bca9ef18d953aeafe8f6ae5b37a657318890c806999dbf4161ac3f5ccb7c6b356ffbded61228e24e6b1ad5e76b3d694923c2483984' ;; 		aarch64) binArch='arm64'; checksum='c4786c030121519ea988ad418878f29b90487357bb434f357955a5ac158460192b4da136fd6d08a2507521a2920412ffa294bf2d83c858c3d1e7fb02de1482a2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0-rc.3/caddy_2.0.0-rc.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 16 Apr 2020 00:50:08 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 16 Apr 2020 00:50:08 GMT
ENV XDG_DATA_HOME=/data
# Thu, 16 Apr 2020 00:50:09 GMT
VOLUME [/config]
# Thu, 16 Apr 2020 00:50:11 GMT
VOLUME [/data]
# Thu, 16 Apr 2020 00:50:12 GMT
LABEL org.opencontainers.image.version=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:50:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 16 Apr 2020 00:50:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 16 Apr 2020 00:50:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 16 Apr 2020 00:50:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 16 Apr 2020 00:50:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 16 Apr 2020 00:50:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Apr 2020 00:50:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 16 Apr 2020 00:50:19 GMT
EXPOSE 80
# Thu, 16 Apr 2020 00:50:20 GMT
EXPOSE 443
# Thu, 16 Apr 2020 00:50:21 GMT
EXPOSE 2019
# Thu, 16 Apr 2020 00:50:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4dda4ab56a13a1d8bae586f3c1118bd9d862c2f1245928f3ab1cffbd09b287`  
		Last Modified: Thu, 16 Apr 2020 00:50:50 GMT  
		Size: 319.0 KB (318952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6306a8bbb774718ea961cd8c24fb370aacb34e1268a6868d8964821419f130d7`  
		Last Modified: Thu, 16 Apr 2020 00:50:50 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9edb5046889b030fa7fd4163c6c0bbdf7bbc89cc299e5fbb0c8dfb8cc12ace5`  
		Last Modified: Thu, 16 Apr 2020 00:50:56 GMT  
		Size: 22.9 MB (22892256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:08ff30aa19db485ae78a08aefaaebe799c92065919a763dba28a73b80decdd0d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25590001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f831f3050f23cc577f83227575cdbdb8353e784dcff2a6bdb3e1c4832d8f14e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2020 23:57:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 15 Apr 2020 23:57:32 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Wed, 15 Apr 2020 23:57:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 15 Apr 2020 23:57:35 GMT
ENV CADDY_VERSION=v2.0.0-rc.3
# Wed, 15 Apr 2020 23:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='32735a963f946bf561ed2a540192c22ad19565be4bce4bc243c61beae9022ca15a54bf5ef8a5f2341bd3af16fd7b0e9f7832697687201a981a2ac52b0c18ca88' ;; 		armhf)   binArch='armv6'; checksum='5f1485c4be4a050dc12a42d9cc6b0a215a27173eca0bd46c09a0e5ac941b863511f695ca1fad211fb7ebb21e516c549aa2b6d7bc7b11ce3f3729a6c632315937' ;; 		armv7)   binArch='armv7'; checksum='f38d32e6c48f6eb889d7f7bca9ef18d953aeafe8f6ae5b37a657318890c806999dbf4161ac3f5ccb7c6b356ffbded61228e24e6b1ad5e76b3d694923c2483984' ;; 		aarch64) binArch='arm64'; checksum='c4786c030121519ea988ad418878f29b90487357bb434f357955a5ac158460192b4da136fd6d08a2507521a2920412ffa294bf2d83c858c3d1e7fb02de1482a2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0-rc.3/caddy_2.0.0-rc.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Apr 2020 23:57:40 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Apr 2020 23:57:40 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Apr 2020 23:57:41 GMT
VOLUME [/config]
# Wed, 15 Apr 2020 23:57:41 GMT
VOLUME [/data]
# Wed, 15 Apr 2020 23:57:42 GMT
LABEL org.opencontainers.image.version=v2.0.0-rc.3
# Wed, 15 Apr 2020 23:57:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Apr 2020 23:57:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Apr 2020 23:57:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Apr 2020 23:57:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Apr 2020 23:57:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Apr 2020 23:57:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Apr 2020 23:57:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Apr 2020 23:57:47 GMT
EXPOSE 80
# Wed, 15 Apr 2020 23:57:47 GMT
EXPOSE 443
# Wed, 15 Apr 2020 23:57:48 GMT
EXPOSE 2019
# Wed, 15 Apr 2020 23:57:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befe79730f9213596c0cab32a77e4953596a1ab545ac79f04785bcb1ace48909`  
		Last Modified: Wed, 15 Apr 2020 23:58:08 GMT  
		Size: 317.9 KB (317897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091b38b8a06e74dc8370527ea85371538a5e02941ce9c603152ab6b32c8d61e7`  
		Last Modified: Wed, 15 Apr 2020 23:58:08 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfda26ce91738c36e69d3129c33bb4aac26edc7e7c9af92747178ddfa17d1b4`  
		Last Modified: Wed, 15 Apr 2020 23:58:13 GMT  
		Size: 22.8 MB (22845766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:e30cf81584606a40e151d611e1dbabc3825c94f3fe9a301ad5b3c57a6c08c983
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25109967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed743ddd2d7af716e9b6ef9cd857b3caed9c902627777847c952518d65b662c3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2020 00:39:33 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 16 Apr 2020 00:39:33 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 16 Apr 2020 00:39:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Thu, 16 Apr 2020 00:39:36 GMT
ENV CADDY_VERSION=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:39:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='32735a963f946bf561ed2a540192c22ad19565be4bce4bc243c61beae9022ca15a54bf5ef8a5f2341bd3af16fd7b0e9f7832697687201a981a2ac52b0c18ca88' ;; 		armhf)   binArch='armv6'; checksum='5f1485c4be4a050dc12a42d9cc6b0a215a27173eca0bd46c09a0e5ac941b863511f695ca1fad211fb7ebb21e516c549aa2b6d7bc7b11ce3f3729a6c632315937' ;; 		armv7)   binArch='armv7'; checksum='f38d32e6c48f6eb889d7f7bca9ef18d953aeafe8f6ae5b37a657318890c806999dbf4161ac3f5ccb7c6b356ffbded61228e24e6b1ad5e76b3d694923c2483984' ;; 		aarch64) binArch='arm64'; checksum='c4786c030121519ea988ad418878f29b90487357bb434f357955a5ac158460192b4da136fd6d08a2507521a2920412ffa294bf2d83c858c3d1e7fb02de1482a2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0-rc.3/caddy_2.0.0-rc.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 16 Apr 2020 00:39:40 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 16 Apr 2020 00:39:41 GMT
ENV XDG_DATA_HOME=/data
# Thu, 16 Apr 2020 00:39:42 GMT
VOLUME [/config]
# Thu, 16 Apr 2020 00:39:42 GMT
VOLUME [/data]
# Thu, 16 Apr 2020 00:39:43 GMT
LABEL org.opencontainers.image.version=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:39:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 16 Apr 2020 00:39:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 16 Apr 2020 00:39:45 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 16 Apr 2020 00:39:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 16 Apr 2020 00:39:46 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 16 Apr 2020 00:39:47 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Apr 2020 00:39:47 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 16 Apr 2020 00:39:48 GMT
EXPOSE 80
# Thu, 16 Apr 2020 00:39:48 GMT
EXPOSE 443
# Thu, 16 Apr 2020 00:39:49 GMT
EXPOSE 2019
# Thu, 16 Apr 2020 00:39:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8769f63ec8b31f05ebb26b0a58d55301ef35d1449a5f401e24fbd8fc966bfd21`  
		Last Modified: Thu, 16 Apr 2020 00:40:10 GMT  
		Size: 319.1 KB (319126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faaac47c6de0ab38444a53999b472ae63772dbb66155e37fc5014ee3f99d596e`  
		Last Modified: Thu, 16 Apr 2020 00:40:10 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4532cc514c5332376487a299a4f52a7863b1aaff5262f88777f86167d2e4bcd`  
		Last Modified: Thu, 16 Apr 2020 00:40:15 GMT  
		Size: 22.1 MB (22061857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:7896c2b5e9fa3b33e2c661c68b2541a63474efb08cd204fdf20e48ab7ad89a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:486d86fe70265203228afb9b9e6e7934019090c6686da9a9fb98579931a05778
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322863984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fd06ca5bdeb1a36375ba63a93a06401045ebb7a6154830e973a6de5949242b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:02:02 GMT
RUN apk add --no-cache 		ca-certificates
# Mon, 23 Mar 2020 23:02:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 08 Apr 2020 23:06:10 GMT
ENV GOLANG_VERSION=1.14.2
# Wed, 08 Apr 2020 23:11:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '98de84e69726a66da7b4e58eac41b99cbe274d7e8906eeb8a5b7eb0aadee7f7c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Wed, 08 Apr 2020 23:11:13 GMT
ENV GOPATH=/go
# Wed, 08 Apr 2020 23:11:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2020 23:11:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 08 Apr 2020 23:11:16 GMT
WORKDIR /go
# Mon, 13 Apr 2020 23:43:21 GMT
WORKDIR /src
# Mon, 13 Apr 2020 23:43:23 GMT
RUN apk add --no-cache     git     ca-certificates
# Mon, 13 Apr 2020 23:43:24 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0-rc.3
# Mon, 13 Apr 2020 23:43:27 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Mon, 13 Apr 2020 23:43:27 GMT
WORKDIR /src/caddy/cmd/caddy
# Mon, 13 Apr 2020 23:43:57 GMT
RUN go get -d ./...
# Mon, 13 Apr 2020 23:43:59 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Mon, 13 Apr 2020 23:43:59 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c732a2540651eb09faab95b03b3b5928ab23e096fae0006bdc2abf9e0cb5bfb4`  
		Last Modified: Mon, 23 Mar 2020 23:13:03 GMT  
		Size: 301.3 KB (301283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2225181d6bcfb7877529a7257ff207cb14e52831420f770cbc2187031b6228`  
		Last Modified: Mon, 23 Mar 2020 23:13:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdfa13e5b48c976ba308826b27a4978c2ffe6833efcfcfc0bd40dbf25e88455`  
		Last Modified: Wed, 08 Apr 2020 23:26:23 GMT  
		Size: 132.0 MB (132012220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c48a539365d2d572e18de4a42ab11b02d9870a17bf1f65160d7fcbbd0423263`  
		Last Modified: Wed, 08 Apr 2020 23:25:47 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947fdad36c6d1e2fd7b618aa1a49dfabaa1ff9d6fb85a195e2437c2b9ac78142`  
		Last Modified: Mon, 13 Apr 2020 23:44:26 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199e6b2236a218d72efd03fc1fa0971c00c87439722e1a40269b7edfd910b79`  
		Last Modified: Mon, 13 Apr 2020 23:44:28 GMT  
		Size: 8.2 MB (8155831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732862f7439776bbe7cc313ed1e10454506f168429234c0daea17d6c48a9692`  
		Last Modified: Mon, 13 Apr 2020 23:44:26 GMT  
		Size: 2.7 MB (2744273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d54fb1573600e831b250c83cb9dc699bab8aa12040568d9ee542fb8d09c1d99`  
		Last Modified: Mon, 13 Apr 2020 23:45:02 GMT  
		Size: 176.8 MB (176846093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e336ec02e20348f57d1ef8151ecfcd216777f5489f01b29164883ec496bcbb`  
		Last Modified: Mon, 13 Apr 2020 23:44:25 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6f8a2da1c847ae8cd10d1f3e37ad75cc0ba17c5e9b4f7e68fdd3b7cffb5482`  
		Last Modified: Mon, 13 Apr 2020 23:44:25 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:cd2ad079bba5bd32e34425b4e582e403c8da0794d75cd9532089e397d6a6a6fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318283866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f1e47fec82e99b063b602e73e298a78f88206130b99dc09f5ce6d996c4b546`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:09:39 GMT
RUN apk add --no-cache 		ca-certificates
# Mon, 23 Mar 2020 22:09:41 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 08 Apr 2020 23:05:33 GMT
ENV GOLANG_VERSION=1.14.2
# Wed, 08 Apr 2020 23:08:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '98de84e69726a66da7b4e58eac41b99cbe274d7e8906eeb8a5b7eb0aadee7f7c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Wed, 08 Apr 2020 23:08:51 GMT
ENV GOPATH=/go
# Wed, 08 Apr 2020 23:08:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2020 23:08:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 08 Apr 2020 23:08:54 GMT
WORKDIR /go
# Tue, 14 Apr 2020 19:02:05 GMT
WORKDIR /src
# Tue, 14 Apr 2020 19:02:09 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 14 Apr 2020 19:02:10 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0-rc.3
# Tue, 14 Apr 2020 19:02:14 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 14 Apr 2020 19:02:16 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 14 Apr 2020 19:03:36 GMT
RUN go get -d ./...
# Tue, 14 Apr 2020 19:03:40 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Tue, 14 Apr 2020 19:03:41 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7800bd79b91213697a2858807a07e49702e4e0f15365c4c7ff9d4e4a702a9c41`  
		Last Modified: Mon, 23 Mar 2020 22:57:54 GMT  
		Size: 301.6 KB (301626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd98a07237762fc6acaab52f9eb58cbea968ed7f0830c02e87622d6f777456e`  
		Last Modified: Mon, 23 Mar 2020 22:57:54 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d32447fdb8339cdd3fde9b708d14fff501271a9f8ff970a75bb23454bcfab8`  
		Last Modified: Wed, 08 Apr 2020 23:17:23 GMT  
		Size: 128.1 MB (128149579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351ec32b9e5337dfc6bdd6204b76587028f2cf530e51bb7f0379908cd3a9e3bb`  
		Last Modified: Wed, 08 Apr 2020 23:15:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a743cd83ba00508dd353a743708e6e434e2f56a1abdc6f2156d953839d646a1`  
		Last Modified: Tue, 14 Apr 2020 19:04:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04790f6bc405f18e7cedfbf754285f13c69997c89558c211e920c8b1e99e99fb`  
		Last Modified: Tue, 14 Apr 2020 19:04:14 GMT  
		Size: 7.8 MB (7777224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7916ea4abf152652f304cc659eb5f49cdeb18bcfa4b08da8121c7cb926618d5f`  
		Last Modified: Tue, 14 Apr 2020 19:04:08 GMT  
		Size: 2.6 MB (2583942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017e0a0855a5b5caab47f0cf399468d8ddee95fcc2a96bb1dba8ef9de6490f41`  
		Last Modified: Tue, 14 Apr 2020 19:04:53 GMT  
		Size: 176.9 MB (176851792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd412eceac3544008060ba63d1877dfa7e7652e3495fa90d754dcf0a515480d`  
		Last Modified: Tue, 14 Apr 2020 19:04:07 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fcea70e4e7db2fed8fb230f66d27fc46446054a0cdc6f6a342235480e7a248`  
		Last Modified: Tue, 14 Apr 2020 19:04:07 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c6b2f1f5d52cfbabf244af757effe7b6ddc142acdb15ef5d8dc7452a9659b795
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.9 MB (316942094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516ec248376a670b87153cbe61efb69b30615826ae2ec1ee48034a951a771e92`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 23:47:15 GMT
RUN apk add --no-cache 		ca-certificates
# Mon, 23 Mar 2020 23:47:17 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 08 Apr 2020 23:11:43 GMT
ENV GOLANG_VERSION=1.14.2
# Wed, 08 Apr 2020 23:14:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '98de84e69726a66da7b4e58eac41b99cbe274d7e8906eeb8a5b7eb0aadee7f7c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Wed, 08 Apr 2020 23:14:23 GMT
ENV GOPATH=/go
# Wed, 08 Apr 2020 23:14:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2020 23:14:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 08 Apr 2020 23:14:31 GMT
WORKDIR /go
# Tue, 14 Apr 2020 19:02:05 GMT
WORKDIR /src
# Tue, 14 Apr 2020 19:02:09 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 14 Apr 2020 19:02:10 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0-rc.3
# Tue, 14 Apr 2020 19:02:15 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 14 Apr 2020 19:02:17 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 14 Apr 2020 19:03:31 GMT
RUN go get -d ./...
# Tue, 14 Apr 2020 19:03:39 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Tue, 14 Apr 2020 19:03:41 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0c66f8509bb56e1ead748baf3433dcad3c1fa170146d5d7d06506b9a80f367`  
		Last Modified: Mon, 23 Mar 2020 23:53:18 GMT  
		Size: 300.6 KB (300602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf5f16b98b20e6e4f07e24e93de1018e88310a49963dc147c370d360a02fdbb`  
		Last Modified: Mon, 23 Mar 2020 23:53:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a38fd97575c34aedd91676d7643f6dbf66a1bca83f7d010e631807b96dae74`  
		Last Modified: Wed, 08 Apr 2020 23:25:03 GMT  
		Size: 127.8 MB (127774109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61bd435de55167e1a5a8cbdd73838375b819c98df2c23be5991140c00cbfd9a`  
		Last Modified: Wed, 08 Apr 2020 23:24:26 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a743cd83ba00508dd353a743708e6e434e2f56a1abdc6f2156d953839d646a1`  
		Last Modified: Tue, 14 Apr 2020 19:04:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8928c849f33d759a505e159745da8960d19460b8735d7a08631ee817549c57d5`  
		Last Modified: Tue, 14 Apr 2020 19:04:11 GMT  
		Size: 7.0 MB (7010480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fe4dbb3884a7fa0c551818da659e9c4d3f97f13eb6d53634655e97f9bd2f0d`  
		Last Modified: Tue, 14 Apr 2020 19:04:10 GMT  
		Size: 2.6 MB (2584042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb4bc7d74da5ae926bd30beea4c4abe59b6c0bb76705fb4f6b83391b591ecd7`  
		Last Modified: Tue, 14 Apr 2020 19:04:53 GMT  
		Size: 176.9 MB (176851243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fb3f4c0251d63ed371fb8a24333c2d9f9dada8830bad6af323550a4276f828`  
		Last Modified: Tue, 14 Apr 2020 19:04:09 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fcea70e4e7db2fed8fb230f66d27fc46446054a0cdc6f6a342235480e7a248`  
		Last Modified: Tue, 14 Apr 2020 19:04:07 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:75a990032363651bf7b39167b9e44e70cb8e6d4ae814545a2274a74005ce8660
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.2 MB (317221628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb140d2ac2499d88e26b91f2219f57edca78ae1597261d9799cb9519bf9f2e24`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 22:58:12 GMT
RUN apk add --no-cache 		ca-certificates
# Mon, 23 Mar 2020 22:58:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 08 Apr 2020 23:11:00 GMT
ENV GOLANG_VERSION=1.14.2
# Wed, 08 Apr 2020 23:13:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '98de84e69726a66da7b4e58eac41b99cbe274d7e8906eeb8a5b7eb0aadee7f7c *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Wed, 08 Apr 2020 23:13:19 GMT
ENV GOPATH=/go
# Wed, 08 Apr 2020 23:13:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2020 23:13:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 08 Apr 2020 23:13:22 GMT
WORKDIR /go
# Tue, 14 Apr 2020 19:02:03 GMT
WORKDIR /src
# Tue, 14 Apr 2020 19:02:07 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 14 Apr 2020 19:02:08 GMT
ENV CADDY_SOURCE_VERSION=v2.0.0-rc.3
# Tue, 14 Apr 2020 19:02:12 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Tue, 14 Apr 2020 19:02:13 GMT
WORKDIR /src/caddy/cmd/caddy
# Tue, 14 Apr 2020 19:03:13 GMT
RUN go get -d ./...
# Tue, 14 Apr 2020 19:03:15 GMT
COPY file:83b813b69aee8796ce6cdf324efd1e9890d70da3ae40d917ee2f320c487134c6 in /usr/bin/caddy-builder 
# Tue, 14 Apr 2020 19:03:21 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42d4106c43952870e20bfb808275012c22e6244af6eff1e916f446f7d338d0d`  
		Last Modified: Mon, 23 Mar 2020 23:03:34 GMT  
		Size: 301.8 KB (301778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f0a4e33d457336c22ac08eaec4609be330959ccdfefdb342be1045df4d26f0`  
		Last Modified: Mon, 23 Mar 2020 23:03:34 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44acbbdbf71f1d00fa6d0011bb10b82bef26b421a579bcf3a3491dced9f8233e`  
		Last Modified: Wed, 08 Apr 2020 23:21:31 GMT  
		Size: 126.4 MB (126405787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d054599df8f57e1578fdc2c554a9ac6124bf04f808dc623ef7f6548230fa3b5f`  
		Last Modified: Wed, 08 Apr 2020 23:20:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcee4e573bebbed33479e125fd8abf1f3debd0a7aee2137f55b67d9c38a79be`  
		Last Modified: Tue, 14 Apr 2020 19:03:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968260b321a071a55eb891faac5f738bc2c3340a7843fc9ebd092902475f6fb3`  
		Last Modified: Tue, 14 Apr 2020 19:03:59 GMT  
		Size: 8.4 MB (8353090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f7e47a5a4e440d1d8c40f1b42638e70ea0fbf9b5635f0145f58768993763d6`  
		Last Modified: Tue, 14 Apr 2020 19:03:57 GMT  
		Size: 2.6 MB (2584029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e682841e5eb376ed223cc26d628878cb76d53d943e6f205310f7294f212717`  
		Last Modified: Tue, 14 Apr 2020 19:04:33 GMT  
		Size: 176.9 MB (176852681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffdb1a37f36e66ea176ba211db0396ddcf52e5c11bc8c335ad3814c1f091f33`  
		Last Modified: Tue, 14 Apr 2020 19:03:58 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d540e0414cc6a26d9aed38f141af756f0c60e88bb278d4807bda8d6b5939314`  
		Last Modified: Tue, 14 Apr 2020 19:03:57 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:f4b3b3ca127d9fcb3bd877e8d29baec0c80e87a83f1151681ee8df2c067bb4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:fdcbef33519f6b5860c3dfa4a7b5267266cd37dd6288c40a4d3731af092e7a84
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27094620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a14b8af6e7a6b5d59c4ddbaa92e503d72f04f9a1379dcea1c6af1d7d1650699`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2020 00:19:25 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 16 Apr 2020 00:19:25 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 16 Apr 2020 00:19:27 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Thu, 16 Apr 2020 00:19:27 GMT
ENV CADDY_VERSION=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:19:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='32735a963f946bf561ed2a540192c22ad19565be4bce4bc243c61beae9022ca15a54bf5ef8a5f2341bd3af16fd7b0e9f7832697687201a981a2ac52b0c18ca88' ;; 		armhf)   binArch='armv6'; checksum='5f1485c4be4a050dc12a42d9cc6b0a215a27173eca0bd46c09a0e5ac941b863511f695ca1fad211fb7ebb21e516c549aa2b6d7bc7b11ce3f3729a6c632315937' ;; 		armv7)   binArch='armv7'; checksum='f38d32e6c48f6eb889d7f7bca9ef18d953aeafe8f6ae5b37a657318890c806999dbf4161ac3f5ccb7c6b356ffbded61228e24e6b1ad5e76b3d694923c2483984' ;; 		aarch64) binArch='arm64'; checksum='c4786c030121519ea988ad418878f29b90487357bb434f357955a5ac158460192b4da136fd6d08a2507521a2920412ffa294bf2d83c858c3d1e7fb02de1482a2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0-rc.3/caddy_2.0.0-rc.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 16 Apr 2020 00:19:29 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 16 Apr 2020 00:19:29 GMT
ENV XDG_DATA_HOME=/data
# Thu, 16 Apr 2020 00:19:29 GMT
VOLUME [/config]
# Thu, 16 Apr 2020 00:19:29 GMT
VOLUME [/data]
# Thu, 16 Apr 2020 00:19:29 GMT
LABEL org.opencontainers.image.version=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 16 Apr 2020 00:19:30 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 16 Apr 2020 00:19:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Apr 2020 00:19:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 16 Apr 2020 00:19:31 GMT
EXPOSE 80
# Thu, 16 Apr 2020 00:19:31 GMT
EXPOSE 443
# Thu, 16 Apr 2020 00:19:31 GMT
EXPOSE 2019
# Thu, 16 Apr 2020 00:19:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c895336717654d7bf50758d2fe590a60610eb7d7168d12c6b6bb9887bae481d`  
		Last Modified: Thu, 16 Apr 2020 00:19:44 GMT  
		Size: 318.6 KB (318556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e769246751713852fe7f4107628f489ad3068e3ef3d9180d8f282591fce3ae2`  
		Last Modified: Thu, 16 Apr 2020 00:19:44 GMT  
		Size: 5.8 KB (5764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5921f47d630c9c7f61bf61ef026a407e71ea4620a63c00d5a0690c74799d409`  
		Last Modified: Thu, 16 Apr 2020 00:19:48 GMT  
		Size: 24.0 MB (23967045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:becd2f8eaa2b3fdfa7368eacb199cd455d874ef5d6f400c1f4c0e2d57f1ba7b0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25835631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2487d38bc455e7c92a16a9eeb0454171f2c7498bb4cfde01babb52e239da5bd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 Mar 2020 21:49:26 GMT
ADD file:e2fdfc637b534345942caf4097883508a5ed23be97d85ccc3357b8277aaa5430 in / 
# Mon, 23 Mar 2020 21:49:27 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2020 00:49:57 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 16 Apr 2020 00:49:58 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 16 Apr 2020 00:50:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Thu, 16 Apr 2020 00:50:02 GMT
ENV CADDY_VERSION=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:50:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='32735a963f946bf561ed2a540192c22ad19565be4bce4bc243c61beae9022ca15a54bf5ef8a5f2341bd3af16fd7b0e9f7832697687201a981a2ac52b0c18ca88' ;; 		armhf)   binArch='armv6'; checksum='5f1485c4be4a050dc12a42d9cc6b0a215a27173eca0bd46c09a0e5ac941b863511f695ca1fad211fb7ebb21e516c549aa2b6d7bc7b11ce3f3729a6c632315937' ;; 		armv7)   binArch='armv7'; checksum='f38d32e6c48f6eb889d7f7bca9ef18d953aeafe8f6ae5b37a657318890c806999dbf4161ac3f5ccb7c6b356ffbded61228e24e6b1ad5e76b3d694923c2483984' ;; 		aarch64) binArch='arm64'; checksum='c4786c030121519ea988ad418878f29b90487357bb434f357955a5ac158460192b4da136fd6d08a2507521a2920412ffa294bf2d83c858c3d1e7fb02de1482a2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0-rc.3/caddy_2.0.0-rc.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 16 Apr 2020 00:50:08 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 16 Apr 2020 00:50:08 GMT
ENV XDG_DATA_HOME=/data
# Thu, 16 Apr 2020 00:50:09 GMT
VOLUME [/config]
# Thu, 16 Apr 2020 00:50:11 GMT
VOLUME [/data]
# Thu, 16 Apr 2020 00:50:12 GMT
LABEL org.opencontainers.image.version=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:50:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 16 Apr 2020 00:50:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 16 Apr 2020 00:50:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 16 Apr 2020 00:50:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 16 Apr 2020 00:50:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 16 Apr 2020 00:50:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Apr 2020 00:50:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 16 Apr 2020 00:50:19 GMT
EXPOSE 80
# Thu, 16 Apr 2020 00:50:20 GMT
EXPOSE 443
# Thu, 16 Apr 2020 00:50:21 GMT
EXPOSE 2019
# Thu, 16 Apr 2020 00:50:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:0776aeec3430c5a5ba3f43937f0ee6a7770a1fe81a318c9d94cc76512e5375e9`  
		Last Modified: Mon, 23 Mar 2020 21:49:50 GMT  
		Size: 2.6 MB (2618579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4dda4ab56a13a1d8bae586f3c1118bd9d862c2f1245928f3ab1cffbd09b287`  
		Last Modified: Thu, 16 Apr 2020 00:50:50 GMT  
		Size: 319.0 KB (318952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6306a8bbb774718ea961cd8c24fb370aacb34e1268a6868d8964821419f130d7`  
		Last Modified: Thu, 16 Apr 2020 00:50:50 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9edb5046889b030fa7fd4163c6c0bbdf7bbc89cc299e5fbb0c8dfb8cc12ace5`  
		Last Modified: Thu, 16 Apr 2020 00:50:56 GMT  
		Size: 22.9 MB (22892256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:08ff30aa19db485ae78a08aefaaebe799c92065919a763dba28a73b80decdd0d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25590001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f831f3050f23cc577f83227575cdbdb8353e784dcff2a6bdb3e1c4832d8f14e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 Mar 2020 21:57:55 GMT
ADD file:3bde6b6fd06efbf24e66446c6d32f72294fc749ae9ee6191776242e92b2f8ab4 in / 
# Mon, 23 Mar 2020 21:57:56 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2020 23:57:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 15 Apr 2020 23:57:32 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Wed, 15 Apr 2020 23:57:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Wed, 15 Apr 2020 23:57:35 GMT
ENV CADDY_VERSION=v2.0.0-rc.3
# Wed, 15 Apr 2020 23:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='32735a963f946bf561ed2a540192c22ad19565be4bce4bc243c61beae9022ca15a54bf5ef8a5f2341bd3af16fd7b0e9f7832697687201a981a2ac52b0c18ca88' ;; 		armhf)   binArch='armv6'; checksum='5f1485c4be4a050dc12a42d9cc6b0a215a27173eca0bd46c09a0e5ac941b863511f695ca1fad211fb7ebb21e516c549aa2b6d7bc7b11ce3f3729a6c632315937' ;; 		armv7)   binArch='armv7'; checksum='f38d32e6c48f6eb889d7f7bca9ef18d953aeafe8f6ae5b37a657318890c806999dbf4161ac3f5ccb7c6b356ffbded61228e24e6b1ad5e76b3d694923c2483984' ;; 		aarch64) binArch='arm64'; checksum='c4786c030121519ea988ad418878f29b90487357bb434f357955a5ac158460192b4da136fd6d08a2507521a2920412ffa294bf2d83c858c3d1e7fb02de1482a2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0-rc.3/caddy_2.0.0-rc.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 15 Apr 2020 23:57:40 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 15 Apr 2020 23:57:40 GMT
ENV XDG_DATA_HOME=/data
# Wed, 15 Apr 2020 23:57:41 GMT
VOLUME [/config]
# Wed, 15 Apr 2020 23:57:41 GMT
VOLUME [/data]
# Wed, 15 Apr 2020 23:57:42 GMT
LABEL org.opencontainers.image.version=v2.0.0-rc.3
# Wed, 15 Apr 2020 23:57:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 15 Apr 2020 23:57:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 15 Apr 2020 23:57:44 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 15 Apr 2020 23:57:44 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 15 Apr 2020 23:57:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 15 Apr 2020 23:57:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 15 Apr 2020 23:57:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 15 Apr 2020 23:57:47 GMT
EXPOSE 80
# Wed, 15 Apr 2020 23:57:47 GMT
EXPOSE 443
# Wed, 15 Apr 2020 23:57:48 GMT
EXPOSE 2019
# Wed, 15 Apr 2020 23:57:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d9bf605ce3d4449f4b90035c3e21d691806324781d43a5287b1da25a01779d6b`  
		Last Modified: Mon, 23 Mar 2020 21:58:16 GMT  
		Size: 2.4 MB (2420493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befe79730f9213596c0cab32a77e4953596a1ab545ac79f04785bcb1ace48909`  
		Last Modified: Wed, 15 Apr 2020 23:58:08 GMT  
		Size: 317.9 KB (317897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091b38b8a06e74dc8370527ea85371538a5e02941ce9c603152ab6b32c8d61e7`  
		Last Modified: Wed, 15 Apr 2020 23:58:08 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfda26ce91738c36e69d3129c33bb4aac26edc7e7c9af92747178ddfa17d1b4`  
		Last Modified: Wed, 15 Apr 2020 23:58:13 GMT  
		Size: 22.8 MB (22845766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:e30cf81584606a40e151d611e1dbabc3825c94f3fe9a301ad5b3c57a6c08c983
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25109967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed743ddd2d7af716e9b6ef9cd857b3caed9c902627777847c952518d65b662c3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2020 00:39:33 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 16 Apr 2020 00:39:33 GMT
ENV CADDY_DIST_COMMIT=80870b227ded910971ecace4a0c136bf0ef46342
# Thu, 16 Apr 2020 00:39:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/$CADDY_DIST_COMMIT/welcome/index.html"
# Thu, 16 Apr 2020 00:39:36 GMT
ENV CADDY_VERSION=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:39:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='32735a963f946bf561ed2a540192c22ad19565be4bce4bc243c61beae9022ca15a54bf5ef8a5f2341bd3af16fd7b0e9f7832697687201a981a2ac52b0c18ca88' ;; 		armhf)   binArch='armv6'; checksum='5f1485c4be4a050dc12a42d9cc6b0a215a27173eca0bd46c09a0e5ac941b863511f695ca1fad211fb7ebb21e516c549aa2b6d7bc7b11ce3f3729a6c632315937' ;; 		armv7)   binArch='armv7'; checksum='f38d32e6c48f6eb889d7f7bca9ef18d953aeafe8f6ae5b37a657318890c806999dbf4161ac3f5ccb7c6b356ffbded61228e24e6b1ad5e76b3d694923c2483984' ;; 		aarch64) binArch='arm64'; checksum='c4786c030121519ea988ad418878f29b90487357bb434f357955a5ac158460192b4da136fd6d08a2507521a2920412ffa294bf2d83c858c3d1e7fb02de1482a2' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.0.0-rc.3/caddy_2.0.0-rc.3_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 16 Apr 2020 00:39:40 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 16 Apr 2020 00:39:41 GMT
ENV XDG_DATA_HOME=/data
# Thu, 16 Apr 2020 00:39:42 GMT
VOLUME [/config]
# Thu, 16 Apr 2020 00:39:42 GMT
VOLUME [/data]
# Thu, 16 Apr 2020 00:39:43 GMT
LABEL org.opencontainers.image.version=v2.0.0-rc.3
# Thu, 16 Apr 2020 00:39:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 16 Apr 2020 00:39:44 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 16 Apr 2020 00:39:45 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 16 Apr 2020 00:39:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 16 Apr 2020 00:39:46 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 16 Apr 2020 00:39:47 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Apr 2020 00:39:47 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 16 Apr 2020 00:39:48 GMT
EXPOSE 80
# Thu, 16 Apr 2020 00:39:48 GMT
EXPOSE 443
# Thu, 16 Apr 2020 00:39:49 GMT
EXPOSE 2019
# Thu, 16 Apr 2020 00:39:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8769f63ec8b31f05ebb26b0a58d55301ef35d1449a5f401e24fbd8fc966bfd21`  
		Last Modified: Thu, 16 Apr 2020 00:40:10 GMT  
		Size: 319.1 KB (319126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faaac47c6de0ab38444a53999b472ae63772dbb66155e37fc5014ee3f99d596e`  
		Last Modified: Thu, 16 Apr 2020 00:40:10 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4532cc514c5332376487a299a4f52a7863b1aaff5262f88777f86167d2e4bcd`  
		Last Modified: Thu, 16 Apr 2020 00:40:15 GMT  
		Size: 22.1 MB (22061857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
