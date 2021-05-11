## `caddy:alpine`

```console
$ docker pull caddy@sha256:0a3759d4e95e9af8a79858f7aa565d24ee8c2bf9a884faddcb1fe95d7ac52967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:alpine` - linux; amd64

```console
$ docker pull caddy@sha256:6395c0a4bfcc76ccd72e0c77bd609c3561f941a32321456520357a278dd113f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14566627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c76f8655142c3788bcce68be571bdc12a9eb162cbef12a8b0cd9828e80ae62f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:11:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 11 May 2021 01:04:23 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Tue, 11 May 2021 01:04:24 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:04:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='dd6427ba877d286f5af229e439e59a05afe840283c7674589f46a3bd2bcb25f2162295d55c705f052318a85de23f3661f8322628e952cc1a0f784a8068f68357' ;; 		armhf)   binArch='armv6'; checksum='088f011a1e71fa3312b907bcdcfe545ba69294e3310acdcccf453c7096498dd61bb818cd19e1fca164711e878a662965bcbfd9946574a20403f71711537a76de' ;; 		armv7)   binArch='armv7'; checksum='32fe7ff1544e3845b181fadd394383f31522239476f7df031f048856ec3ae73264f70eb3934e6074b7bba385e1188cacef6b7c941e80b1f9a303711eecae396b' ;; 		aarch64) binArch='arm64'; checksum='2c4fa4ce1465e1dc8e97d669bde9df50a06f4c21a916e59d32d5a4af7be449fc3f0f18303e43ff95655202832898bbdf02148b4aaa1e9e205d487ef14482b31e' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='1ab37dba5fea5e55a403b51d59faa1d4ba74eb3065584fdf585562ae88de6396b5296e5d3c107e5bd2a08cc4e77dce2a8ee29f291a5d4639b4a097b47de9dbf9' ;; 		s390x)   binArch='s390x'; checksum='ec9319f3ade6ead60c2b6c1a8c5649ca6f911efef938970fc1f08a613ecf9d582b507aad178a7c75fdcf502164cbf4f4563553c40be2ced529c6b0844def8341' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 11 May 2021 01:04:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 11 May 2021 01:04:28 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 11 May 2021 01:04:28 GMT
ENV XDG_DATA_HOME=/data
# Tue, 11 May 2021 01:04:28 GMT
VOLUME [/config]
# Tue, 11 May 2021 01:04:28 GMT
VOLUME [/data]
# Tue, 11 May 2021 01:04:28 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 01:04:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 01:04:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 01:04:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 01:04:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 01:04:30 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 01:04:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 01:04:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 01:04:30 GMT
EXPOSE 80
# Tue, 11 May 2021 01:04:31 GMT
EXPOSE 443
# Tue, 11 May 2021 01:04:31 GMT
EXPOSE 2019
# Tue, 11 May 2021 01:04:31 GMT
WORKDIR /srv
# Tue, 11 May 2021 01:04:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8294633c5b5606f8e98aaf81da701b7a7e2018dbf82355d1d73830c677034f19`  
		Last Modified: Wed, 14 Apr 2021 20:12:08 GMT  
		Size: 300.4 KB (300403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16798e0582fce7af9c2ba2c8ee4990d0fd1e58384e170ee9937486253d67bbf1`  
		Last Modified: Tue, 11 May 2021 01:05:00 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7caf536ee3257ee5085ea50b1fdb2342f1ba7cf67dd718c14657bc29c9c1df`  
		Last Modified: Tue, 11 May 2021 01:05:02 GMT  
		Size: 11.4 MB (11448248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55d296ee3d96b0a8ddf81c22c5416bfdfb98b4e987079dea3f1d2a407a0a3d7`  
		Last Modified: Tue, 11 May 2021 01:05:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:accd51f67c4da65e48a62067231d7f279a7414c84f7e3a074ea484a8024e7ddf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13781937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e539d0aea8e90bdb3c7929a807a5300f0e2ad19de1a5eea2b7307a99f573271`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:46:41 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 10 May 2021 23:50:08 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Mon, 10 May 2021 23:50:20 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:50:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='dd6427ba877d286f5af229e439e59a05afe840283c7674589f46a3bd2bcb25f2162295d55c705f052318a85de23f3661f8322628e952cc1a0f784a8068f68357' ;; 		armhf)   binArch='armv6'; checksum='088f011a1e71fa3312b907bcdcfe545ba69294e3310acdcccf453c7096498dd61bb818cd19e1fca164711e878a662965bcbfd9946574a20403f71711537a76de' ;; 		armv7)   binArch='armv7'; checksum='32fe7ff1544e3845b181fadd394383f31522239476f7df031f048856ec3ae73264f70eb3934e6074b7bba385e1188cacef6b7c941e80b1f9a303711eecae396b' ;; 		aarch64) binArch='arm64'; checksum='2c4fa4ce1465e1dc8e97d669bde9df50a06f4c21a916e59d32d5a4af7be449fc3f0f18303e43ff95655202832898bbdf02148b4aaa1e9e205d487ef14482b31e' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='1ab37dba5fea5e55a403b51d59faa1d4ba74eb3065584fdf585562ae88de6396b5296e5d3c107e5bd2a08cc4e77dce2a8ee29f291a5d4639b4a097b47de9dbf9' ;; 		s390x)   binArch='s390x'; checksum='ec9319f3ade6ead60c2b6c1a8c5649ca6f911efef938970fc1f08a613ecf9d582b507aad178a7c75fdcf502164cbf4f4563553c40be2ced529c6b0844def8341' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 10 May 2021 23:50:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 10 May 2021 23:50:33 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 10 May 2021 23:50:34 GMT
ENV XDG_DATA_HOME=/data
# Mon, 10 May 2021 23:50:35 GMT
VOLUME [/config]
# Mon, 10 May 2021 23:50:37 GMT
VOLUME [/data]
# Mon, 10 May 2021 23:50:38 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Mon, 10 May 2021 23:50:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 10 May 2021 23:50:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 10 May 2021 23:50:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 10 May 2021 23:50:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 10 May 2021 23:50:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 10 May 2021 23:50:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 10 May 2021 23:50:47 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 10 May 2021 23:50:49 GMT
EXPOSE 80
# Mon, 10 May 2021 23:50:50 GMT
EXPOSE 443
# Mon, 10 May 2021 23:50:52 GMT
EXPOSE 2019
# Mon, 10 May 2021 23:50:54 GMT
WORKDIR /srv
# Mon, 10 May 2021 23:50:55 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf1089ae45174c5bef4f470e0e4c2337f99090005f19e104781d0b048ea9c3b`  
		Last Modified: Wed, 14 Apr 2021 19:48:05 GMT  
		Size: 300.5 KB (300511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c14f76d7a7af16ae081f310cdc4fedb50982a53c62946c7880f5333bd47c28`  
		Last Modified: Mon, 10 May 2021 23:51:39 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f575ba8a69ca1a5904bf22dad27c7546342af53febbc35ccb5dd267e8feab97c`  
		Last Modified: Mon, 10 May 2021 23:51:43 GMT  
		Size: 10.9 MB (10853292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c324d5c3633091e7997d13f43fe84f9ac2bf7794d197fa229113ad4c902faf2f`  
		Last Modified: Mon, 10 May 2021 23:51:39 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:159edc693b6f3d45e04ab7307ea31bfa442d06231b69e5f42bff5eb2125ab1fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13559369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfb4539c52fe67844a8b90b8d3a0bf118a6896f043571a3a8d6218cdb32f69b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:40:17 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 11 May 2021 01:15:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Tue, 11 May 2021 01:15:43 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:16:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='dd6427ba877d286f5af229e439e59a05afe840283c7674589f46a3bd2bcb25f2162295d55c705f052318a85de23f3661f8322628e952cc1a0f784a8068f68357' ;; 		armhf)   binArch='armv6'; checksum='088f011a1e71fa3312b907bcdcfe545ba69294e3310acdcccf453c7096498dd61bb818cd19e1fca164711e878a662965bcbfd9946574a20403f71711537a76de' ;; 		armv7)   binArch='armv7'; checksum='32fe7ff1544e3845b181fadd394383f31522239476f7df031f048856ec3ae73264f70eb3934e6074b7bba385e1188cacef6b7c941e80b1f9a303711eecae396b' ;; 		aarch64) binArch='arm64'; checksum='2c4fa4ce1465e1dc8e97d669bde9df50a06f4c21a916e59d32d5a4af7be449fc3f0f18303e43ff95655202832898bbdf02148b4aaa1e9e205d487ef14482b31e' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='1ab37dba5fea5e55a403b51d59faa1d4ba74eb3065584fdf585562ae88de6396b5296e5d3c107e5bd2a08cc4e77dce2a8ee29f291a5d4639b4a097b47de9dbf9' ;; 		s390x)   binArch='s390x'; checksum='ec9319f3ade6ead60c2b6c1a8c5649ca6f911efef938970fc1f08a613ecf9d582b507aad178a7c75fdcf502164cbf4f4563553c40be2ced529c6b0844def8341' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 11 May 2021 01:16:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 11 May 2021 01:16:51 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 11 May 2021 01:16:52 GMT
ENV XDG_DATA_HOME=/data
# Tue, 11 May 2021 01:16:54 GMT
VOLUME [/config]
# Tue, 11 May 2021 01:16:55 GMT
VOLUME [/data]
# Tue, 11 May 2021 01:16:57 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 01:16:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 01:17:00 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 01:17:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 01:17:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 01:17:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 01:17:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 01:17:09 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 01:17:12 GMT
EXPOSE 80
# Tue, 11 May 2021 01:17:13 GMT
EXPOSE 443
# Tue, 11 May 2021 01:17:16 GMT
EXPOSE 2019
# Tue, 11 May 2021 01:17:19 GMT
WORKDIR /srv
# Tue, 11 May 2021 01:17:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f77b739097bd5400613d0daa0adde01d99993ce236a374da6748f11f866bf0`  
		Last Modified: Wed, 14 Apr 2021 19:41:38 GMT  
		Size: 299.7 KB (299662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5d4f3a32ad0ee5557140984ec66d8aec7518580e0b4f25075abc467852f5c9`  
		Last Modified: Tue, 11 May 2021 01:19:04 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c575185c831e1739dc7ab125ed53c9c9eeb2d30e22cf98463c504b37032eaa50`  
		Last Modified: Tue, 11 May 2021 01:19:08 GMT  
		Size: 10.8 MB (10829560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaaca182d4fd03b56b6b3a42f2291ff209334224c854363a79e5ebab993f3230`  
		Last Modified: Tue, 11 May 2021 01:19:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:a7b0a04a662cf260a34977b125179056a62db0b2e1851c1dd7d8ebc9f8cfc759
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13415216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f513d5a7342c2d3b29180971441798c54e90a4bae8566531b9ad22ed40df6212`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:00:47 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 10 May 2021 23:39:51 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Mon, 10 May 2021 23:39:52 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:39:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='dd6427ba877d286f5af229e439e59a05afe840283c7674589f46a3bd2bcb25f2162295d55c705f052318a85de23f3661f8322628e952cc1a0f784a8068f68357' ;; 		armhf)   binArch='armv6'; checksum='088f011a1e71fa3312b907bcdcfe545ba69294e3310acdcccf453c7096498dd61bb818cd19e1fca164711e878a662965bcbfd9946574a20403f71711537a76de' ;; 		armv7)   binArch='armv7'; checksum='32fe7ff1544e3845b181fadd394383f31522239476f7df031f048856ec3ae73264f70eb3934e6074b7bba385e1188cacef6b7c941e80b1f9a303711eecae396b' ;; 		aarch64) binArch='arm64'; checksum='2c4fa4ce1465e1dc8e97d669bde9df50a06f4c21a916e59d32d5a4af7be449fc3f0f18303e43ff95655202832898bbdf02148b4aaa1e9e205d487ef14482b31e' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='1ab37dba5fea5e55a403b51d59faa1d4ba74eb3065584fdf585562ae88de6396b5296e5d3c107e5bd2a08cc4e77dce2a8ee29f291a5d4639b4a097b47de9dbf9' ;; 		s390x)   binArch='s390x'; checksum='ec9319f3ade6ead60c2b6c1a8c5649ca6f911efef938970fc1f08a613ecf9d582b507aad178a7c75fdcf502164cbf4f4563553c40be2ced529c6b0844def8341' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 10 May 2021 23:39:58 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 10 May 2021 23:39:59 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 10 May 2021 23:40:00 GMT
ENV XDG_DATA_HOME=/data
# Mon, 10 May 2021 23:40:01 GMT
VOLUME [/config]
# Mon, 10 May 2021 23:40:02 GMT
VOLUME [/data]
# Mon, 10 May 2021 23:40:02 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Mon, 10 May 2021 23:40:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 10 May 2021 23:40:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 10 May 2021 23:40:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 10 May 2021 23:40:06 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 10 May 2021 23:40:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 10 May 2021 23:40:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 10 May 2021 23:40:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 10 May 2021 23:40:09 GMT
EXPOSE 80
# Mon, 10 May 2021 23:40:10 GMT
EXPOSE 443
# Mon, 10 May 2021 23:40:11 GMT
EXPOSE 2019
# Mon, 10 May 2021 23:40:12 GMT
WORKDIR /srv
# Mon, 10 May 2021 23:40:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0e0200fa31a158cd37e4584ab7ca30d0663376cf38fe7f1b73ff5a9a59fa12`  
		Last Modified: Wed, 14 Apr 2021 19:02:06 GMT  
		Size: 300.6 KB (300628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a226e39f1950acc413ed3ac67a7b336554ce3e8b6f18944919ead2f26fc64b`  
		Last Modified: Mon, 10 May 2021 23:40:48 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4960f1f64846804fc30f5058d85051d76e307a619fc59284272e71e7499c3a38`  
		Last Modified: Mon, 10 May 2021 23:40:51 GMT  
		Size: 10.4 MB (10396556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f958efe8814c77472d3cc7966c7cd904e5d478ebb7a6bc55787ec52ed29cc6`  
		Last Modified: Mon, 10 May 2021 23:40:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:d211f951fe7f23617be7c14d71ed0cd4119eaab14cbf966986edc416f0c0be82
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13116860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd138e3e0b764e1303127c59ea74d320008abb27509713e2e0cdd44a2354978f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:12:15 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 11 May 2021 01:17:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Tue, 11 May 2021 01:17:09 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:17:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='dd6427ba877d286f5af229e439e59a05afe840283c7674589f46a3bd2bcb25f2162295d55c705f052318a85de23f3661f8322628e952cc1a0f784a8068f68357' ;; 		armhf)   binArch='armv6'; checksum='088f011a1e71fa3312b907bcdcfe545ba69294e3310acdcccf453c7096498dd61bb818cd19e1fca164711e878a662965bcbfd9946574a20403f71711537a76de' ;; 		armv7)   binArch='armv7'; checksum='32fe7ff1544e3845b181fadd394383f31522239476f7df031f048856ec3ae73264f70eb3934e6074b7bba385e1188cacef6b7c941e80b1f9a303711eecae396b' ;; 		aarch64) binArch='arm64'; checksum='2c4fa4ce1465e1dc8e97d669bde9df50a06f4c21a916e59d32d5a4af7be449fc3f0f18303e43ff95655202832898bbdf02148b4aaa1e9e205d487ef14482b31e' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='1ab37dba5fea5e55a403b51d59faa1d4ba74eb3065584fdf585562ae88de6396b5296e5d3c107e5bd2a08cc4e77dce2a8ee29f291a5d4639b4a097b47de9dbf9' ;; 		s390x)   binArch='s390x'; checksum='ec9319f3ade6ead60c2b6c1a8c5649ca6f911efef938970fc1f08a613ecf9d582b507aad178a7c75fdcf502164cbf4f4563553c40be2ced529c6b0844def8341' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 11 May 2021 01:17:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 11 May 2021 01:17:48 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 11 May 2021 01:17:55 GMT
ENV XDG_DATA_HOME=/data
# Tue, 11 May 2021 01:17:59 GMT
VOLUME [/config]
# Tue, 11 May 2021 01:18:03 GMT
VOLUME [/data]
# Tue, 11 May 2021 01:18:09 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 01:18:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 01:18:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 01:18:20 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 01:18:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 01:18:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 01:18:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 01:18:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 01:18:46 GMT
EXPOSE 80
# Tue, 11 May 2021 01:18:49 GMT
EXPOSE 443
# Tue, 11 May 2021 01:18:52 GMT
EXPOSE 2019
# Tue, 11 May 2021 01:18:56 GMT
WORKDIR /srv
# Tue, 11 May 2021 01:19:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25908330df11bb7bc2ed71aa9b4de279db5492df2b03ced3f6650b25821c4584`  
		Last Modified: Wed, 14 Apr 2021 22:16:00 GMT  
		Size: 302.6 KB (302554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a224581e3ba4733f37686f5a5d5375019f9126a0ded6ed20f13e09e898dc735e`  
		Last Modified: Tue, 11 May 2021 01:20:08 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1dd74ee5b1b1729043f41d60aef4d52f55ec9f64d89cd625caaf037ae0c7be6`  
		Last Modified: Tue, 11 May 2021 01:20:11 GMT  
		Size: 10.0 MB (9995159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0bfaf16f0b56abead39bc99d52694122454078fb2e2e9e29f4209f4daf0a8e`  
		Last Modified: Tue, 11 May 2021 01:20:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9e5a00e41c90ba5e0300a6397166cc06dcfac524c3221fa520a9ded1ce6c163b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13937005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc589ef8ecca20bb3a9cd3b06f370d0f4c74397fc459cf6cf14588d7d0c64c9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:07:40 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 10 May 2021 23:41:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"
# Mon, 10 May 2021 23:41:39 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:41:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='dd6427ba877d286f5af229e439e59a05afe840283c7674589f46a3bd2bcb25f2162295d55c705f052318a85de23f3661f8322628e952cc1a0f784a8068f68357' ;; 		armhf)   binArch='armv6'; checksum='088f011a1e71fa3312b907bcdcfe545ba69294e3310acdcccf453c7096498dd61bb818cd19e1fca164711e878a662965bcbfd9946574a20403f71711537a76de' ;; 		armv7)   binArch='armv7'; checksum='32fe7ff1544e3845b181fadd394383f31522239476f7df031f048856ec3ae73264f70eb3934e6074b7bba385e1188cacef6b7c941e80b1f9a303711eecae396b' ;; 		aarch64) binArch='arm64'; checksum='2c4fa4ce1465e1dc8e97d669bde9df50a06f4c21a916e59d32d5a4af7be449fc3f0f18303e43ff95655202832898bbdf02148b4aaa1e9e205d487ef14482b31e' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='1ab37dba5fea5e55a403b51d59faa1d4ba74eb3065584fdf585562ae88de6396b5296e5d3c107e5bd2a08cc4e77dce2a8ee29f291a5d4639b4a097b47de9dbf9' ;; 		s390x)   binArch='s390x'; checksum='ec9319f3ade6ead60c2b6c1a8c5649ca6f911efef938970fc1f08a613ecf9d582b507aad178a7c75fdcf502164cbf4f4563553c40be2ced529c6b0844def8341' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 10 May 2021 23:41:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 10 May 2021 23:41:46 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 10 May 2021 23:41:46 GMT
ENV XDG_DATA_HOME=/data
# Mon, 10 May 2021 23:41:47 GMT
VOLUME [/config]
# Mon, 10 May 2021 23:41:48 GMT
VOLUME [/data]
# Mon, 10 May 2021 23:41:48 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Mon, 10 May 2021 23:41:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 10 May 2021 23:41:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 10 May 2021 23:41:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 10 May 2021 23:41:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 10 May 2021 23:41:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 10 May 2021 23:41:52 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 10 May 2021 23:41:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 10 May 2021 23:41:54 GMT
EXPOSE 80
# Mon, 10 May 2021 23:41:55 GMT
EXPOSE 443
# Mon, 10 May 2021 23:41:55 GMT
EXPOSE 2019
# Mon, 10 May 2021 23:41:55 GMT
WORKDIR /srv
# Mon, 10 May 2021 23:41:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db3c8b812fcb0d1bfd42c16c2e9ac68f4f3006382c5362e969d1c9eb3a9fab5`  
		Last Modified: Wed, 14 Apr 2021 20:08:26 GMT  
		Size: 300.8 KB (300847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eba030675d7bb5bc251d93896d2c81ed8a2f4f4ef2e8e84ad7dfdce9886387c`  
		Last Modified: Mon, 10 May 2021 23:42:29 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645cac8e572aad7be24e99df8012056e9752654f6923bf19b08171139a76793d`  
		Last Modified: Mon, 10 May 2021 23:42:31 GMT  
		Size: 11.0 MB (11027506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d6ae883db75a7ce02c9b38976d8aa73fe94d35701ce4f589302e33cc88710d`  
		Last Modified: Mon, 10 May 2021 23:42:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
