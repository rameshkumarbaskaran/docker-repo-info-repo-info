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
