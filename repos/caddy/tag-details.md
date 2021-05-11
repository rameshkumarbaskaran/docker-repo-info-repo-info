<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `caddy`

-	[`caddy:2`](#caddy2)
-	[`caddy:2-alpine`](#caddy2-alpine)
-	[`caddy:2-builder`](#caddy2-builder)
-	[`caddy:2-builder-alpine`](#caddy2-builder-alpine)
-	[`caddy:2-builder-windowsservercore-1809`](#caddy2-builder-windowsservercore-1809)
-	[`caddy:2-builder-windowsservercore-ltsc2016`](#caddy2-builder-windowsservercore-ltsc2016)
-	[`caddy:2-windowsservercore`](#caddy2-windowsservercore)
-	[`caddy:2-windowsservercore-1809`](#caddy2-windowsservercore-1809)
-	[`caddy:2-windowsservercore-ltsc2016`](#caddy2-windowsservercore-ltsc2016)
-	[`caddy:2.3.0`](#caddy230)
-	[`caddy:2.3.0-alpine`](#caddy230-alpine)
-	[`caddy:2.3.0-builder`](#caddy230-builder)
-	[`caddy:2.3.0-builder-alpine`](#caddy230-builder-alpine)
-	[`caddy:2.3.0-builder-windowsservercore-1809`](#caddy230-builder-windowsservercore-1809)
-	[`caddy:2.3.0-builder-windowsservercore-ltsc2016`](#caddy230-builder-windowsservercore-ltsc2016)
-	[`caddy:2.3.0-windowsservercore`](#caddy230-windowsservercore)
-	[`caddy:2.3.0-windowsservercore-1809`](#caddy230-windowsservercore-1809)
-	[`caddy:2.3.0-windowsservercore-ltsc2016`](#caddy230-windowsservercore-ltsc2016)
-	[`caddy:2.4.0`](#caddy240)
-	[`caddy:2.4.0-alpine`](#caddy240-alpine)
-	[`caddy:2.4.0-builder`](#caddy240-builder)
-	[`caddy:2.4.0-builder-alpine`](#caddy240-builder-alpine)
-	[`caddy:2.4.0-builder-windowsservercore-1809`](#caddy240-builder-windowsservercore-1809)
-	[`caddy:2.4.0-builder-windowsservercore-ltsc2016`](#caddy240-builder-windowsservercore-ltsc2016)
-	[`caddy:2.4.0-windowsservercore`](#caddy240-windowsservercore)
-	[`caddy:2.4.0-windowsservercore-1809`](#caddy240-windowsservercore-1809)
-	[`caddy:2.4.0-windowsservercore-ltsc2016`](#caddy240-windowsservercore-ltsc2016)
-	[`caddy:alpine`](#caddyalpine)
-	[`caddy:builder`](#caddybuilder)
-	[`caddy:builder-alpine`](#caddybuilder-alpine)
-	[`caddy:builder-windowsservercore-1809`](#caddybuilder-windowsservercore-1809)
-	[`caddy:builder-windowsservercore-ltsc2016`](#caddybuilder-windowsservercore-ltsc2016)
-	[`caddy:latest`](#caddylatest)
-	[`caddy:windowsservercore`](#caddywindowsservercore)
-	[`caddy:windowsservercore-1809`](#caddywindowsservercore-1809)
-	[`caddy:windowsservercore-ltsc2016`](#caddywindowsservercore-ltsc2016)

## `caddy:2`

```console
$ docker pull caddy@sha256:73c4d6412b5e64794e37feeb50d2defc434fb792be2378b35339db162ba52533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:6fbf52298c46c55c572670b5395ecaee5d399338003c9bb4e4abed875c542f4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14728953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7395cc3713b2ca5574a9b4aafc468a1533d16582efe47dcab74ed547540d698a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:10:47 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:10:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:10:49 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:10:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:10:53 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:10:53 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:10:54 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:10:55 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:56 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:10:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7a0cd9cca5be9b30bbc70611052d1456502e1f338ce4b14946233b21cd6a9a`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 300.0 KB (300016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5666523658a43fbbdff6b8fca498a988f4dcecc3ce027f1701414658c21d4ea`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b097228407f13a161f68b188b0a4f255855b64d84e7b076745a744d5aa7ed8cf`  
		Last Modified: Wed, 14 Apr 2021 20:11:49 GMT  
		Size: 11.6 MB (11622383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40682d93cc09b4592a1b9c08d48d0a956b5eef4f123d80d1a12942482edb6aab`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

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

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a41623f53d582c8b503ae859f6ae98c7c0695eddb11bdbf8514b9b914955c3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13639723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4b837694902a1a259a4915444feda59d895ed37ffbef66b8518b9a884f029c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:39:25 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:39:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:39:34 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:39:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:39:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:39:43 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:39:45 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:39:46 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:39:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:39:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:39:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:39:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:39:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:39:56 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:39:57 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:39:58 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:39:59 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:40:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b239ad5e698454501b0de011bffea35a660806a0b85a6141776581e3a98bc467`  
		Last Modified: Wed, 14 Apr 2021 19:41:24 GMT  
		Size: 299.2 KB (299210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0460b038be93717158ad9cdb6f83768b7129eaf4fcaef8620adc7509d0e5fe`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0905d1ca8c4f74966ae8a7b5ebe8fdb33854c4a759d543d767dd9a0add81f155`  
		Last Modified: Wed, 14 Apr 2021 19:41:29 GMT  
		Size: 10.9 MB (10925348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02da274f552e184a7fa5527990e666d77c70e3715a0d96b7588e7433b3022a`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

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

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:f551e1db7910e2d5235d303760aff5b514fc6e8b49d8d67d434bb23c40ac25db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13356454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982bd235f46e537404cdab42c3dfb3d0058f97ed5d7984f2e71ad8734adcc6a8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:22 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Wed, 14 Apr 2021 19:31:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:09:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 22:09:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 22:09:24 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 22:09:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 22:09:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:09:56 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 22:10:01 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 22:10:06 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 22:10:15 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 22:10:22 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 22:10:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 22:10:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 22:10:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 22:10:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 22:10:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 22:11:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 22:11:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 22:11:14 GMT
EXPOSE 80
# Wed, 14 Apr 2021 22:11:20 GMT
EXPOSE 443
# Wed, 14 Apr 2021 22:11:27 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 22:11:35 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 22:11:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93dd31358a6e859a05bb506b946720f02c7ec7969776d811b20eaaa84508cd7`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 302.3 KB (302339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8077b8c9cca163d9a34281a866cf5fe991ff8c160ebd1ab1b617c6b722ec690`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55884816b8eca8150db9473989410e372c69c5431deb51a6cacd029895cf3dd6`  
		Last Modified: Wed, 14 Apr 2021 22:15:43 GMT  
		Size: 10.2 MB (10241380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51efee06e0a650ff5f146fc54a695d4bf2b44e19da18120fdc494982d52cdd62`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; s390x

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

### `caddy:2` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:dee876a8acfe0ad66efe5790b51e5ce47ee105518205c16c1e515107022ee466
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487145585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab04d82b7c1bbab4a4556a4ab389e58cf942f64806603d16b32d02b85377ddc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:15:27 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:15:28 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:16:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:16:04 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:16:06 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:16:07 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:16:08 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:16:10 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:16:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:16:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:16:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:16:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:16:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:16:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:16:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:16:21 GMT
EXPOSE 80
# Tue, 11 May 2021 00:16:22 GMT
EXPOSE 443
# Tue, 11 May 2021 00:16:24 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:16:51 GMT
RUN caddy version
# Tue, 11 May 2021 00:16:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a805066d9e28c5afaf71144648d2270f86d9d1dfbaa0da9a239607694e9315b6`  
		Last Modified: Tue, 11 May 2021 00:26:29 GMT  
		Size: 5.1 MB (5104734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbd0ec6de6085e7571da80b4408f11fada63d710eaf20b44c1ce63847f6455c`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1c04d9585e13e14d3ba056c3a17a8a23821f402c55d603f719fde9885fcc74`  
		Last Modified: Tue, 11 May 2021 00:26:31 GMT  
		Size: 11.9 MB (11930099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27b6dfe0db5cd7aad46afe881c42348361a2c19752cf5629eacb67967b8520`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41902606f9afaae6014164471bda32934d7f0304b3aaa65e2d7480497d85b0bc`  
		Last Modified: Tue, 11 May 2021 00:26:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9ff94e742183a75d4199b58723e286d55ecdd255b03a81ad9ec2b222c85fe1`  
		Last Modified: Tue, 11 May 2021 00:26:25 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1edf08b568698061ffae34580ddf83acab5de417993a30b8a209c919461e6a`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2873cb5c59a087bae99202d1b5f8e424378796848bf9f9f0576cb9e75da8011`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11858529cacdcdc2b7ff911a5df669b21b0efaa8c2fcbde324ccaf0a4a2d4d6`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b96fffb3765e29e3c670d5e14eb09f96a25c0222143cfac7d62c9fa6224896`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b40f5b20f6588f423dc4ba00206ef0b74da9619e96c8c26af206ea104cf85`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9116ab8bdbdeb3f51018f29b3c57d96ed1ebdff8866b0a503c7cb682741e5d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec28519386c9082afe64bc68c2e073b32a2287131bba90c6f56cc9315a638b04`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7649cdb04974c2bf32fa747aadcf57f6402a9c418e9e8f78ada74eae7aec3029`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9652bcbd02b47c702e6f2e8c374f7304cb91ba0186aede9c423104440004857d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33145d7abff94087dd683fd05403939e5aa91276d2693f6c5e8ca28641acd8e1`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a096c1bcb735f9b2cd6bf77eb582dd89b09a6cc75199dd35d65bd5cf6ad50e`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dde82b55b25477fe6eb7381cfdb3e48aa439cbd3f6352e033a85d124cecae7a`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67426815598f918caebff919df817435078c051338bebd944aafb6b25ef593f6`  
		Last Modified: Tue, 11 May 2021 00:26:20 GMT  
		Size: 331.3 KB (331282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf87ebb9031675a0e4407a36e79f274666df2a06d20c2452c1e0acec70fc60a6`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:b61efb630c29dfd10f857eed823207497fd9c94176f47243f48c641119c663d3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818059080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3940d8ab2b2d69a458bd9951c005b3703a5ac35754896cbfd380305f8dfe27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:18:49 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:18:50 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:20:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:20:40 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:20:42 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:20:43 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:20:45 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:20:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:20:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:20:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:20:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:20:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:20:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:20:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:20:56 GMT
EXPOSE 80
# Tue, 11 May 2021 00:20:58 GMT
EXPOSE 443
# Tue, 11 May 2021 00:20:59 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:22:14 GMT
RUN caddy version
# Tue, 11 May 2021 00:22:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc088e7513f9bd5e2261035715cd5f39aff459f086737be39631a5c03dd0bc9`  
		Last Modified: Tue, 11 May 2021 00:27:00 GMT  
		Size: 5.7 MB (5678806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a94477e69ebd7355bfc6230d3309aa20d4fda7d504dc34bd3b2adae7f5f2b4`  
		Last Modified: Tue, 11 May 2021 00:26:57 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db416be1d5a7c97652523c359440855c0ef2127ac11cb08595aa068d99d8a5`  
		Last Modified: Tue, 11 May 2021 00:27:03 GMT  
		Size: 17.2 MB (17201492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e500af558c7988b44d7fae2a1a8c1d4498cb130d1de721a37712c33f09147a`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87b8476ce7fba27f66c08050c4a692f8a19ec0c84e9d42537b4b4b8bbb5f56e`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2d6240d48682965790d983fc3f6b5404aeb7f3f023b517ab83b6e47c20af5c`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757d21ff239a36a372b7fb98d22d42afd8f3c779c7b342605186d6b2a14925e7`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5e64a8fa017a3b5df9f60508bc7b3f72fe2835f00c086648f26235c9358b14`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac63d4edb89dc9920755d7e04e444610a75ac1268b103c178ebff146f490d73`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fbb5cca77bbd06aabe9371bf1fe894938b82367a0ef11be873b231a43b64ab`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b0ecb05ae3d1fffc947acf96dea7fe481fd9a745d4fcf79bff9f4b21a28817`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f292068b665f33bccf70f8100aa252145e0f63abb2283fa29d36cadcc6291c52`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1995472761eea00392fa2ce2d1566a7233a89a019e939892cbb0aeb4a8a3a07a`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e8f37215e61d4f10f002f5ad82c4acadf4a56b559cf036050f33242bfe1e35`  
		Last Modified: Tue, 11 May 2021 00:26:49 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2f6fb7cf636418bada10647c66ee3b92246da967ebb611d58aad6725f5e2b`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271eda8ea06432cb0dae8fd93e8a85314e86201450cdbebf3efcbba2dbd4331`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a4da75f19907c0ee148b5369a63863a2752457cc31b02fe68779d83d56c1`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7013990e537c69857c80a4d6fb386f6d0f04e5a0a5ee5b12ed57c0e458fc8e`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b661b1f2a589a6717a5599a78cb0f3ef950c1a36bd411039dfd39afb20e901b`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 269.3 KB (269349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e686f1164cdcf35434a7d997c0c9ff058302aaade06ace7c5f8a2e4a718aa`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:a7e19bfcf2ead129c692fa915cf6c98dc51d625757e6344da706cf896b6846d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:6fbf52298c46c55c572670b5395ecaee5d399338003c9bb4e4abed875c542f4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14728953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7395cc3713b2ca5574a9b4aafc468a1533d16582efe47dcab74ed547540d698a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:10:47 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:10:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:10:49 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:10:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:10:53 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:10:53 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:10:54 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:10:55 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:56 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:10:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7a0cd9cca5be9b30bbc70611052d1456502e1f338ce4b14946233b21cd6a9a`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 300.0 KB (300016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5666523658a43fbbdff6b8fca498a988f4dcecc3ce027f1701414658c21d4ea`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b097228407f13a161f68b188b0a4f255855b64d84e7b076745a744d5aa7ed8cf`  
		Last Modified: Wed, 14 Apr 2021 20:11:49 GMT  
		Size: 11.6 MB (11622383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40682d93cc09b4592a1b9c08d48d0a956b5eef4f123d80d1a12942482edb6aab`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

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

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a41623f53d582c8b503ae859f6ae98c7c0695eddb11bdbf8514b9b914955c3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13639723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4b837694902a1a259a4915444feda59d895ed37ffbef66b8518b9a884f029c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:39:25 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:39:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:39:34 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:39:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:39:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:39:43 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:39:45 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:39:46 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:39:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:39:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:39:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:39:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:39:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:39:56 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:39:57 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:39:58 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:39:59 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:40:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b239ad5e698454501b0de011bffea35a660806a0b85a6141776581e3a98bc467`  
		Last Modified: Wed, 14 Apr 2021 19:41:24 GMT  
		Size: 299.2 KB (299210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0460b038be93717158ad9cdb6f83768b7129eaf4fcaef8620adc7509d0e5fe`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0905d1ca8c4f74966ae8a7b5ebe8fdb33854c4a759d543d767dd9a0add81f155`  
		Last Modified: Wed, 14 Apr 2021 19:41:29 GMT  
		Size: 10.9 MB (10925348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02da274f552e184a7fa5527990e666d77c70e3715a0d96b7588e7433b3022a`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

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

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:f551e1db7910e2d5235d303760aff5b514fc6e8b49d8d67d434bb23c40ac25db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13356454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982bd235f46e537404cdab42c3dfb3d0058f97ed5d7984f2e71ad8734adcc6a8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:22 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Wed, 14 Apr 2021 19:31:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:09:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 22:09:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 22:09:24 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 22:09:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 22:09:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:09:56 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 22:10:01 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 22:10:06 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 22:10:15 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 22:10:22 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 22:10:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 22:10:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 22:10:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 22:10:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 22:10:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 22:11:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 22:11:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 22:11:14 GMT
EXPOSE 80
# Wed, 14 Apr 2021 22:11:20 GMT
EXPOSE 443
# Wed, 14 Apr 2021 22:11:27 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 22:11:35 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 22:11:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93dd31358a6e859a05bb506b946720f02c7ec7969776d811b20eaaa84508cd7`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 302.3 KB (302339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8077b8c9cca163d9a34281a866cf5fe991ff8c160ebd1ab1b617c6b722ec690`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55884816b8eca8150db9473989410e372c69c5431deb51a6cacd029895cf3dd6`  
		Last Modified: Wed, 14 Apr 2021 22:15:43 GMT  
		Size: 10.2 MB (10241380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51efee06e0a650ff5f146fc54a695d4bf2b44e19da18120fdc494982d52cdd62`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

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

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:8fed7c7421721ba021fff2b52f695efe1adafa0e1557f0d60d0b952047edf9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:6740d877ef515ceac8a37a496899fea4d7607bd9831a4a6c990949964ccf3536
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119554161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48e0382f0f224a95381e7fdb346fe40e28931bdec03923e00db3699d75eec90`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:29:08 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:29:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:29:09 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:25:19 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 23:27:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:27:21 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:27:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:27:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:27:22 GMT
WORKDIR /go
# Fri, 07 May 2021 01:56:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:56:04 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 07 May 2021 01:56:04 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 07 May 2021 01:56:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 07 May 2021 01:56:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 07 May 2021 01:56:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 07 May 2021 01:56:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22b54d2d4342f88201f48db57cae1f7edbacae870ee13d7962f999edd7529a9`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5898d3d0f1f95fd666f764bf918c1656be6169868335cb63bc428a5ef47cf32`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7bf786162598b899ee14cad74bdc1c8a634091a242e88aecef7426389cc2c4`  
		Last Modified: Thu, 06 May 2021 23:32:32 GMT  
		Size: 106.8 MB (106834379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6e1c1f19605c012184b2d0a8839483fcd208ac6cec2f7960703fdd1175dfcf`  
		Last Modified: Thu, 06 May 2021 23:32:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271517dcb3cc152671658ffe8a14ad9d506a93ecdf782757e9ae05c710b62b5`  
		Last Modified: Fri, 07 May 2021 01:56:41 GMT  
		Size: 8.3 MB (8326465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9f2fd9dcaaae8f453297e27e74f09fe28520c7c7c8665bc59870f9fabee0f7`  
		Last Modified: Fri, 07 May 2021 01:56:40 GMT  
		Size: 1.3 MB (1311156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e523069c0450345d7a7e25d5d975f68003c2311e50b473eaa1ea30f0586fdc2a`  
		Last Modified: Fri, 07 May 2021 01:56:40 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:124237c870217e836b67b4697d7cddad2c3c58d50878dc51654db3605712c336
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112278566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bef88e43f4622abd673fe82f110eb193559dd1abb2d8550178eb66032b4b5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:00:55 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:01:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:01:02 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:24:09 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 21:27:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 21:27:32 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 21:27:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:27:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 21:27:35 GMT
WORKDIR /go
# Thu, 06 May 2021 22:10:19 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 06 May 2021 22:10:20 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:51:04 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:51:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:51:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:51:14 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:51:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4dea9fd179326b36ea137aad07e06571ffe7ad849e2a13a32354dcfd5d858d`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 281.4 KB (281379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abeb04d84d23abf8470fc95982483a9117a87e55b13c591f5332a460a5233bb`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a3721aaa7ffedbec829a557c2d5f99c4661695a51f82632ece4df509b71bc1`  
		Last Modified: Thu, 06 May 2021 21:38:30 GMT  
		Size: 101.9 MB (101925593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298c78bc6b40a671a2f9a64d2cecf253acd10da30924ff687012e02b0307a1a8`  
		Last Modified: Thu, 06 May 2021 21:37:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3d237d41fc2805c9d9a047d4bb2618233c7093cc31d682b5231e0261a8c201`  
		Last Modified: Thu, 06 May 2021 22:11:03 GMT  
		Size: 6.2 MB (6227066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ffbb7f2dd65c638ffd56b2ab5964193545041922501d15451a2b6f4b0b0edb`  
		Last Modified: Mon, 10 May 2021 23:51:50 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d30db79a4a633e8984befac9884a645ed6f3bd581f677daa8a26f2cbda65a4`  
		Last Modified: Mon, 10 May 2021 23:51:50 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:6a27d36624d8ceafd50f9caf199d8583315839b6e47617242194192b6443fad3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113547980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc13dd897b9d3a097309d0364885377e102cd91c4dcec23ffd64375520f0029b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:28:16 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:28:21 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:28:26 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:22:53 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 23:25:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:25:38 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:25:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:25:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:25:46 GMT
WORKDIR /go
# Fri, 07 May 2021 02:33:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:33:55 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 07 May 2021 02:33:56 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 07 May 2021 02:33:56 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 07 May 2021 02:33:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 07 May 2021 02:33:59 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 07 May 2021 02:34:00 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a884c3a8500725e0f08f924091ec61ae3e3acee3b0ffe5839b06f874ee63dc08`  
		Last Modified: Wed, 14 Apr 2021 22:45:08 GMT  
		Size: 280.1 KB (280078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f87f08a98de1e7cb636267b626d4e644775ff7962ea1ff9b4813f740b89e67`  
		Last Modified: Wed, 14 Apr 2021 22:45:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73018330efc261efdcdccd072ee7b6ea3dc05bab6b4760a1ec828924d12acf96`  
		Last Modified: Thu, 06 May 2021 23:31:44 GMT  
		Size: 102.5 MB (102483682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12ff58945623ccdd317243b312562a87a60534d35bb0a88f1e2bdd4b800450a`  
		Last Modified: Thu, 06 May 2021 23:31:14 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada1f2ae57155d23410debd2de0fed3f494ac4cedb2d716f10ac64aa8f49350c`  
		Last Modified: Fri, 07 May 2021 02:34:45 GMT  
		Size: 7.2 MB (7154830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6132f297784ed0d2a64f3581da395b458a6ad21b2a884c3dbabf79410415362c`  
		Last Modified: Fri, 07 May 2021 02:34:44 GMT  
		Size: 1.2 MB (1219497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dd68f4d45c90ed4b3be4d5335c923e68cdd3317597b2575fabbdacf45f38fc`  
		Last Modified: Fri, 07 May 2021 02:34:44 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:a8418ff913feb35632b8e2e0e2dde138632b289047de19713b0c24fe65c6eecc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111763060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68622e818b4c271dd7faf093081a9641f809d407eb6dc67bb6afe822393b4b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:40:18 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:40:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:40:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:31:41 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 22:33:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 22:33:53 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 22:33:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:33:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 22:33:57 GMT
WORKDIR /go
# Fri, 07 May 2021 01:17:18 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:17:19 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:40:20 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:40:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:40:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:40:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:40:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7186ed65a4f7bb0e9cd4b00f43359b47a4f19749dbd48e704fc578a4f43d7c96`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 281.5 KB (281488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316046926c0ae5f42710c1197ed3de9fc374986179c18611f523cf4521adeef1`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a969ea94b7c2e3938ec670b72c32f58ece636bb7ec6526d0efab40e760bce`  
		Last Modified: Thu, 06 May 2021 22:44:20 GMT  
		Size: 101.1 MB (101090590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff4d3f41a5567d10cda7e4f3c4267dbb9181eb63bb52c950c3dce3327a9a36e`  
		Last Modified: Thu, 06 May 2021 22:43:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ec12dccc6ac2c5238a0e958e58c89d37f56cf2e181ba8a4f291b176a2a20fa`  
		Last Modified: Fri, 07 May 2021 01:18:00 GMT  
		Size: 6.5 MB (6476691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803dba8659a2ec5c5a177383797832eca7c7d301ec4253e47ee42527aa617bac`  
		Last Modified: Mon, 10 May 2021 23:40:59 GMT  
		Size: 1.2 MB (1201547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e70f326991067a04529de021321ce20d6920e81d14aaef93afb92136c976508`  
		Last Modified: Mon, 10 May 2021 23:40:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:91017bdca5b5a6e529ba9dbbf8b4cc0f1abad484dd2a19ff8162e5a20f1b7470
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114013692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c636d928211d0eebf80ad41447aae081460c4d3673fbb846379e0f71a65c581c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:22 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Wed, 14 Apr 2021 19:31:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:57:05 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 22:57:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:57:16 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:35:58 GMT
ENV GOLANG_VERSION=1.15.12
# Fri, 07 May 2021 00:38:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 07 May 2021 00:38:24 GMT
ENV GOPATH=/go
# Fri, 07 May 2021 00:38:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:38:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 07 May 2021 00:38:53 GMT
WORKDIR /go
# Fri, 07 May 2021 08:18:14 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 08:18:28 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 07 May 2021 08:18:33 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 07 May 2021 08:18:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 07 May 2021 08:19:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 07 May 2021 08:19:05 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 07 May 2021 08:19:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dca7bf08f7e7ef8f1c651b5ba53ba748e66f5a75400b38f67596867bfae4e2`  
		Last Modified: Wed, 14 Apr 2021 23:06:16 GMT  
		Size: 283.2 KB (283201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d495ca184c89fdc74ec1ec1cc670ff41be844b29174141c4602ac1400b0645`  
		Last Modified: Wed, 14 Apr 2021 23:06:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6d75cc8304f9250be10afcbb80447f234d1f01911e86274118bb6fdc34ed48`  
		Last Modified: Fri, 07 May 2021 00:44:07 GMT  
		Size: 100.8 MB (100812628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0997c196aa13c6e561f3432b7239d95ee90562c507e5a8c4f21acfcf1e17f5e3`  
		Last Modified: Fri, 07 May 2021 00:43:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb6e06aa8363e1138fed17e9f2a879be30ac49ebdee6931f49ea76200a4cab3`  
		Last Modified: Fri, 07 May 2021 08:22:00 GMT  
		Size: 8.9 MB (8939878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedccec34d2dc5617dde35e772984f1c60c1cf730c13faeef29d2ecf217b24df`  
		Last Modified: Fri, 07 May 2021 08:21:58 GMT  
		Size: 1.2 MB (1170522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b959e44e74065aea1788a48f30813a54b7121ff398a293ed94b2d6d370f57d8`  
		Last Modified: Fri, 07 May 2021 08:21:58 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:e72252e76203d04b2ed847e26d71ca0de7ed89c2d76990ac177fb80755d88617
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115474412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08b1e73df9c564bfdb9249c0d32c47642dd69cd88bfa280b4682767ef8fe671`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:45:11 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:45:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:45:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:16:38 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:20:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:20:18 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:20:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:20:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:20:21 GMT
WORKDIR /go
# Fri, 07 May 2021 02:02:34 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:02:35 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:42:03 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:42:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:42:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:42:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:42:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc746875ae346ee6ec3c9080f8a7a50bef3899ea9d5ae9dac45a81bfe861c9d`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 281.7 KB (281708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0242688236000dd8f33d16f89f36da3ef1bb2a7a32bb59a7eb97a18ed3d5158`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37dab17b6808078a43afd3d62f1a202857192406e914c33d5ceb5eec1eb05eeb`  
		Last Modified: Thu, 06 May 2021 23:34:08 GMT  
		Size: 104.8 MB (104849388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6059cb089a1bd1108012ddff056f297d814995f95d29d57b15c13d11baede00d`  
		Last Modified: Thu, 06 May 2021 23:33:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84919c1c43955cfb518f179d4f6b541cdfa94579f6f6ef10fdc6e6b3ca4d51a3`  
		Last Modified: Fri, 07 May 2021 02:03:18 GMT  
		Size: 6.5 MB (6475416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3025f5e46ec68c9ef05a49a22ca89718a0d154f401122b0505a18d1c9217fc`  
		Last Modified: Mon, 10 May 2021 23:42:38 GMT  
		Size: 1.3 MB (1264531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bb5d9c7e67f1492e82b3f7c19e6900095d43b1f65fa5496f752a95169cd953`  
		Last Modified: Mon, 10 May 2021 23:42:38 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:bc783b828c95b331d7fad4be39c04af02ab0b76ff396546a2d118771441f398e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2641373061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed813a8f2c9cd1366b5455eb1fd1c585aa4ab0f42e380f58cb6a58f23c27eead`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:30:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:30:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:30:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:30:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:31:57 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:32:38 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:16:07 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 20:18:44 GMT
RUN $url = 'https://dl.google.com/go/go1.16.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'd40139b7ade8a3008e3240a6f86fe8f899a9c465c917e11dac8758af216f5eb0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:18:46 GMT
WORKDIR C:\gopath
# Thu, 06 May 2021 21:02:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:02:30 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 00:22:36 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:22:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 00:23:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 May 2021 00:23:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac56922ba0ee0ac19bcae98f5fb4b7427d31ef3c709f27cfb2c785fd13a611c4`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1723430d5101a2d617d3dbf4bc2a121b3f4b4432105aa2941e1afab8f130b9`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f4dc6e9a77d69a3d172368f4ae471b31c588d6201c2386e4ac62fd83faa16`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea47861a9221a4f1e5750db237c619796c612756a5e75e2cb443b1731ae8a8`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4be4ebd8eabefdb01f27dafad85e65289b95ca15591c14304c7792db99b54b`  
		Last Modified: Wed, 14 Apr 2021 12:58:35 GMT  
		Size: 30.2 MB (30155601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f66ae3738a83ea41b428b49261d4522d57df1617fbd1aa362d93f1e2802643`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2108b314c24064a0c250f72017cc64b3bf68915655327728a267c98985a5ff7`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 324.6 KB (324649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa51985154dd0edd95ef4cc022400dc16b657c4a75cb3ade3675c58d316d0101`  
		Last Modified: Thu, 06 May 2021 20:34:43 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26942e7cec550ceca0e7b0ef319dc3f732731719adfc676869678adce06d1193`  
		Last Modified: Thu, 06 May 2021 20:35:15 GMT  
		Size: 139.4 MB (139382398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e6b3adacda0d1c5092f48a23fa73f5bb807876cf3dcf7fd71632b48d8b1987`  
		Last Modified: Thu, 06 May 2021 20:34:43 GMT  
		Size: 1.6 KB (1598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6d89568ee8ac19213ae2e66b14601f80c6dd3c4a1205da5fa55da7003cd3a0`  
		Last Modified: Thu, 06 May 2021 21:06:02 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0aa20834bcdb38f731b9f6528281005b29ae951a02ef46190bf1be1cab5946`  
		Last Modified: Thu, 06 May 2021 21:06:00 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada218f8f73674eea11444ee4fa8048f2cfd6e2bfc8f8c2bb4cc40954436b6b0`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815ac3cbadfa3d6463be2a02130f663d74e486df33a07b582def59fe66dd48b0`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da0a5d30891cb84455c6b13f7a6b778a19b3a271813ef7066eb0ba908192ee7`  
		Last Modified: Tue, 11 May 2021 00:27:20 GMT  
		Size: 1.7 MB (1738012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e2cb2540135f046b5adb4957a0f75118aeb15e30d46af750522a16e6f0cc2`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:1b2ba73c8dc7fce225f65c457524b3830589cf0fa3e9c62faa0c88b15c73c74f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5987368241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd19fd51f0fc365a83899a16ab9d8fb86585a512ff6cc33bd07e7af1bc5d89d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:35:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:35:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:35:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:35:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:38:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:39:34 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:19:05 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 20:22:32 GMT
RUN $url = 'https://dl.google.com/go/go1.16.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'd40139b7ade8a3008e3240a6f86fe8f899a9c465c917e11dac8758af216f5eb0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:22:34 GMT
WORKDIR C:\gopath
# Thu, 06 May 2021 21:03:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:03:07 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 00:23:23 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:23:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 00:25:06 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 May 2021 00:25:08 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3360763b706a564d93471b21a342ebbda7e047567cf1cbee82dd592ad33e0c`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0f653700ac9b57cf3d694cc90107e3220fc678581d1e985219677733ce242`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59d82702c225a2ca8cd2a5476122f55d8619eae959c9cb8323b68d70a2ed19`  
		Last Modified: Wed, 14 Apr 2021 12:59:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62435cd2b7652fc97ef3dc1a8968446f3f6e95f0ff1d6dcb176a3f0c2b14c2f8`  
		Last Modified: Wed, 14 Apr 2021 12:59:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d78a3a3d6cb25f55dc9d9947f7449a14717e6b787e49571a837e72b79334cf`  
		Last Modified: Wed, 14 Apr 2021 12:59:41 GMT  
		Size: 30.8 MB (30752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b774a32e346c00e004abbbd7290530d0a3f3dfb11915be2b2fa73c402da6bdd`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d153061f2f0d8ef33f71c4b9afd90899e21556e320d7103a8a9fb544c1cb521`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 5.6 MB (5608025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c85bf3447935a123c186c94d58b02a7e89b566366ab0c7a20b57fbc9e453e1`  
		Last Modified: Thu, 06 May 2021 20:35:33 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7558c3fc6da1f41d9317a885b7d1d896986e9e4a81b6487a543b93ca372649cd`  
		Last Modified: Thu, 06 May 2021 20:36:08 GMT  
		Size: 149.1 MB (149112181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d97cea35310e2e19e356bf67efe44136adb4df53f744e6497511765af70f7e`  
		Last Modified: Thu, 06 May 2021 20:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5214a4bbf455290910bf5850bebdd3fdde0c4bf2616c2975a8a91b62cfe7a`  
		Last Modified: Thu, 06 May 2021 21:06:13 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f9311ef107812e0fc28e80ff17843a7d95e33d9b4311d0ff921022f5d199c3`  
		Last Modified: Thu, 06 May 2021 21:06:10 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b921e314d8bdd24486247a7d82137f437b1572bec858ea76813dc27e580670`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8450625dd9bbf2232b7a3d1cbce4d8795d03b140b1fb962bb6042b82a073633`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394074991c1e1b9a6750cf551fb9f7fe9eaffa1a25889bebcf0f35682cb69afe`  
		Last Modified: Tue, 11 May 2021 00:27:37 GMT  
		Size: 7.0 MB (6993409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5f2fa898b0d7f2684b17b889c9c68aa767c0a1f408e2e4eceb3374cdf48393`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:73a6c2dbab08011b02984c25ad70c202a5676ed597f58e9f79a2ad75e75fd91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:6740d877ef515ceac8a37a496899fea4d7607bd9831a4a6c990949964ccf3536
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119554161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48e0382f0f224a95381e7fdb346fe40e28931bdec03923e00db3699d75eec90`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:29:08 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:29:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:29:09 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:25:19 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 23:27:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:27:21 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:27:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:27:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:27:22 GMT
WORKDIR /go
# Fri, 07 May 2021 01:56:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:56:04 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 07 May 2021 01:56:04 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 07 May 2021 01:56:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 07 May 2021 01:56:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 07 May 2021 01:56:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 07 May 2021 01:56:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22b54d2d4342f88201f48db57cae1f7edbacae870ee13d7962f999edd7529a9`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5898d3d0f1f95fd666f764bf918c1656be6169868335cb63bc428a5ef47cf32`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7bf786162598b899ee14cad74bdc1c8a634091a242e88aecef7426389cc2c4`  
		Last Modified: Thu, 06 May 2021 23:32:32 GMT  
		Size: 106.8 MB (106834379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6e1c1f19605c012184b2d0a8839483fcd208ac6cec2f7960703fdd1175dfcf`  
		Last Modified: Thu, 06 May 2021 23:32:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271517dcb3cc152671658ffe8a14ad9d506a93ecdf782757e9ae05c710b62b5`  
		Last Modified: Fri, 07 May 2021 01:56:41 GMT  
		Size: 8.3 MB (8326465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9f2fd9dcaaae8f453297e27e74f09fe28520c7c7c8665bc59870f9fabee0f7`  
		Last Modified: Fri, 07 May 2021 01:56:40 GMT  
		Size: 1.3 MB (1311156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e523069c0450345d7a7e25d5d975f68003c2311e50b473eaa1ea30f0586fdc2a`  
		Last Modified: Fri, 07 May 2021 01:56:40 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:124237c870217e836b67b4697d7cddad2c3c58d50878dc51654db3605712c336
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112278566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bef88e43f4622abd673fe82f110eb193559dd1abb2d8550178eb66032b4b5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:00:55 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:01:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:01:02 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:24:09 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 21:27:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 21:27:32 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 21:27:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:27:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 21:27:35 GMT
WORKDIR /go
# Thu, 06 May 2021 22:10:19 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 06 May 2021 22:10:20 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:51:04 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:51:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:51:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:51:14 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:51:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4dea9fd179326b36ea137aad07e06571ffe7ad849e2a13a32354dcfd5d858d`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 281.4 KB (281379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abeb04d84d23abf8470fc95982483a9117a87e55b13c591f5332a460a5233bb`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a3721aaa7ffedbec829a557c2d5f99c4661695a51f82632ece4df509b71bc1`  
		Last Modified: Thu, 06 May 2021 21:38:30 GMT  
		Size: 101.9 MB (101925593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298c78bc6b40a671a2f9a64d2cecf253acd10da30924ff687012e02b0307a1a8`  
		Last Modified: Thu, 06 May 2021 21:37:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3d237d41fc2805c9d9a047d4bb2618233c7093cc31d682b5231e0261a8c201`  
		Last Modified: Thu, 06 May 2021 22:11:03 GMT  
		Size: 6.2 MB (6227066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ffbb7f2dd65c638ffd56b2ab5964193545041922501d15451a2b6f4b0b0edb`  
		Last Modified: Mon, 10 May 2021 23:51:50 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d30db79a4a633e8984befac9884a645ed6f3bd581f677daa8a26f2cbda65a4`  
		Last Modified: Mon, 10 May 2021 23:51:50 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:6a27d36624d8ceafd50f9caf199d8583315839b6e47617242194192b6443fad3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113547980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc13dd897b9d3a097309d0364885377e102cd91c4dcec23ffd64375520f0029b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:28:16 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:28:21 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:28:26 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:22:53 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 23:25:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:25:38 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:25:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:25:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:25:46 GMT
WORKDIR /go
# Fri, 07 May 2021 02:33:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:33:55 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 07 May 2021 02:33:56 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 07 May 2021 02:33:56 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 07 May 2021 02:33:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 07 May 2021 02:33:59 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 07 May 2021 02:34:00 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a884c3a8500725e0f08f924091ec61ae3e3acee3b0ffe5839b06f874ee63dc08`  
		Last Modified: Wed, 14 Apr 2021 22:45:08 GMT  
		Size: 280.1 KB (280078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f87f08a98de1e7cb636267b626d4e644775ff7962ea1ff9b4813f740b89e67`  
		Last Modified: Wed, 14 Apr 2021 22:45:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73018330efc261efdcdccd072ee7b6ea3dc05bab6b4760a1ec828924d12acf96`  
		Last Modified: Thu, 06 May 2021 23:31:44 GMT  
		Size: 102.5 MB (102483682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12ff58945623ccdd317243b312562a87a60534d35bb0a88f1e2bdd4b800450a`  
		Last Modified: Thu, 06 May 2021 23:31:14 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada1f2ae57155d23410debd2de0fed3f494ac4cedb2d716f10ac64aa8f49350c`  
		Last Modified: Fri, 07 May 2021 02:34:45 GMT  
		Size: 7.2 MB (7154830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6132f297784ed0d2a64f3581da395b458a6ad21b2a884c3dbabf79410415362c`  
		Last Modified: Fri, 07 May 2021 02:34:44 GMT  
		Size: 1.2 MB (1219497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dd68f4d45c90ed4b3be4d5335c923e68cdd3317597b2575fabbdacf45f38fc`  
		Last Modified: Fri, 07 May 2021 02:34:44 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:a8418ff913feb35632b8e2e0e2dde138632b289047de19713b0c24fe65c6eecc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111763060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68622e818b4c271dd7faf093081a9641f809d407eb6dc67bb6afe822393b4b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:40:18 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:40:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:40:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:31:41 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 22:33:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 22:33:53 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 22:33:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:33:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 22:33:57 GMT
WORKDIR /go
# Fri, 07 May 2021 01:17:18 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:17:19 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:40:20 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:40:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:40:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:40:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:40:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7186ed65a4f7bb0e9cd4b00f43359b47a4f19749dbd48e704fc578a4f43d7c96`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 281.5 KB (281488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316046926c0ae5f42710c1197ed3de9fc374986179c18611f523cf4521adeef1`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a969ea94b7c2e3938ec670b72c32f58ece636bb7ec6526d0efab40e760bce`  
		Last Modified: Thu, 06 May 2021 22:44:20 GMT  
		Size: 101.1 MB (101090590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff4d3f41a5567d10cda7e4f3c4267dbb9181eb63bb52c950c3dce3327a9a36e`  
		Last Modified: Thu, 06 May 2021 22:43:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ec12dccc6ac2c5238a0e958e58c89d37f56cf2e181ba8a4f291b176a2a20fa`  
		Last Modified: Fri, 07 May 2021 01:18:00 GMT  
		Size: 6.5 MB (6476691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803dba8659a2ec5c5a177383797832eca7c7d301ec4253e47ee42527aa617bac`  
		Last Modified: Mon, 10 May 2021 23:40:59 GMT  
		Size: 1.2 MB (1201547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e70f326991067a04529de021321ce20d6920e81d14aaef93afb92136c976508`  
		Last Modified: Mon, 10 May 2021 23:40:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:91017bdca5b5a6e529ba9dbbf8b4cc0f1abad484dd2a19ff8162e5a20f1b7470
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114013692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c636d928211d0eebf80ad41447aae081460c4d3673fbb846379e0f71a65c581c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:22 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Wed, 14 Apr 2021 19:31:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:57:05 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 22:57:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:57:16 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:35:58 GMT
ENV GOLANG_VERSION=1.15.12
# Fri, 07 May 2021 00:38:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 07 May 2021 00:38:24 GMT
ENV GOPATH=/go
# Fri, 07 May 2021 00:38:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:38:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 07 May 2021 00:38:53 GMT
WORKDIR /go
# Fri, 07 May 2021 08:18:14 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 08:18:28 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 07 May 2021 08:18:33 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 07 May 2021 08:18:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 07 May 2021 08:19:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 07 May 2021 08:19:05 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 07 May 2021 08:19:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dca7bf08f7e7ef8f1c651b5ba53ba748e66f5a75400b38f67596867bfae4e2`  
		Last Modified: Wed, 14 Apr 2021 23:06:16 GMT  
		Size: 283.2 KB (283201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d495ca184c89fdc74ec1ec1cc670ff41be844b29174141c4602ac1400b0645`  
		Last Modified: Wed, 14 Apr 2021 23:06:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6d75cc8304f9250be10afcbb80447f234d1f01911e86274118bb6fdc34ed48`  
		Last Modified: Fri, 07 May 2021 00:44:07 GMT  
		Size: 100.8 MB (100812628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0997c196aa13c6e561f3432b7239d95ee90562c507e5a8c4f21acfcf1e17f5e3`  
		Last Modified: Fri, 07 May 2021 00:43:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb6e06aa8363e1138fed17e9f2a879be30ac49ebdee6931f49ea76200a4cab3`  
		Last Modified: Fri, 07 May 2021 08:22:00 GMT  
		Size: 8.9 MB (8939878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedccec34d2dc5617dde35e772984f1c60c1cf730c13faeef29d2ecf217b24df`  
		Last Modified: Fri, 07 May 2021 08:21:58 GMT  
		Size: 1.2 MB (1170522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b959e44e74065aea1788a48f30813a54b7121ff398a293ed94b2d6d370f57d8`  
		Last Modified: Fri, 07 May 2021 08:21:58 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:e72252e76203d04b2ed847e26d71ca0de7ed89c2d76990ac177fb80755d88617
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115474412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08b1e73df9c564bfdb9249c0d32c47642dd69cd88bfa280b4682767ef8fe671`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:45:11 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:45:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:45:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:16:38 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:20:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:20:18 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:20:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:20:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:20:21 GMT
WORKDIR /go
# Fri, 07 May 2021 02:02:34 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:02:35 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:42:03 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:42:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:42:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:42:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:42:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc746875ae346ee6ec3c9080f8a7a50bef3899ea9d5ae9dac45a81bfe861c9d`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 281.7 KB (281708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0242688236000dd8f33d16f89f36da3ef1bb2a7a32bb59a7eb97a18ed3d5158`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37dab17b6808078a43afd3d62f1a202857192406e914c33d5ceb5eec1eb05eeb`  
		Last Modified: Thu, 06 May 2021 23:34:08 GMT  
		Size: 104.8 MB (104849388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6059cb089a1bd1108012ddff056f297d814995f95d29d57b15c13d11baede00d`  
		Last Modified: Thu, 06 May 2021 23:33:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84919c1c43955cfb518f179d4f6b541cdfa94579f6f6ef10fdc6e6b3ca4d51a3`  
		Last Modified: Fri, 07 May 2021 02:03:18 GMT  
		Size: 6.5 MB (6475416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3025f5e46ec68c9ef05a49a22ca89718a0d154f401122b0505a18d1c9217fc`  
		Last Modified: Mon, 10 May 2021 23:42:38 GMT  
		Size: 1.3 MB (1264531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bb5d9c7e67f1492e82b3f7c19e6900095d43b1f65fa5496f752a95169cd953`  
		Last Modified: Mon, 10 May 2021 23:42:38 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:a6cb45df3913c41d877ad5dea68ac399f038d58e244fc5f2637971201ece8f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:bc783b828c95b331d7fad4be39c04af02ab0b76ff396546a2d118771441f398e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2641373061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed813a8f2c9cd1366b5455eb1fd1c585aa4ab0f42e380f58cb6a58f23c27eead`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:30:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:30:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:30:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:30:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:31:57 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:32:38 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:16:07 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 20:18:44 GMT
RUN $url = 'https://dl.google.com/go/go1.16.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'd40139b7ade8a3008e3240a6f86fe8f899a9c465c917e11dac8758af216f5eb0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:18:46 GMT
WORKDIR C:\gopath
# Thu, 06 May 2021 21:02:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:02:30 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 00:22:36 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:22:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 00:23:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 May 2021 00:23:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac56922ba0ee0ac19bcae98f5fb4b7427d31ef3c709f27cfb2c785fd13a611c4`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1723430d5101a2d617d3dbf4bc2a121b3f4b4432105aa2941e1afab8f130b9`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f4dc6e9a77d69a3d172368f4ae471b31c588d6201c2386e4ac62fd83faa16`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea47861a9221a4f1e5750db237c619796c612756a5e75e2cb443b1731ae8a8`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4be4ebd8eabefdb01f27dafad85e65289b95ca15591c14304c7792db99b54b`  
		Last Modified: Wed, 14 Apr 2021 12:58:35 GMT  
		Size: 30.2 MB (30155601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f66ae3738a83ea41b428b49261d4522d57df1617fbd1aa362d93f1e2802643`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2108b314c24064a0c250f72017cc64b3bf68915655327728a267c98985a5ff7`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 324.6 KB (324649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa51985154dd0edd95ef4cc022400dc16b657c4a75cb3ade3675c58d316d0101`  
		Last Modified: Thu, 06 May 2021 20:34:43 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26942e7cec550ceca0e7b0ef319dc3f732731719adfc676869678adce06d1193`  
		Last Modified: Thu, 06 May 2021 20:35:15 GMT  
		Size: 139.4 MB (139382398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e6b3adacda0d1c5092f48a23fa73f5bb807876cf3dcf7fd71632b48d8b1987`  
		Last Modified: Thu, 06 May 2021 20:34:43 GMT  
		Size: 1.6 KB (1598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6d89568ee8ac19213ae2e66b14601f80c6dd3c4a1205da5fa55da7003cd3a0`  
		Last Modified: Thu, 06 May 2021 21:06:02 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0aa20834bcdb38f731b9f6528281005b29ae951a02ef46190bf1be1cab5946`  
		Last Modified: Thu, 06 May 2021 21:06:00 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada218f8f73674eea11444ee4fa8048f2cfd6e2bfc8f8c2bb4cc40954436b6b0`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815ac3cbadfa3d6463be2a02130f663d74e486df33a07b582def59fe66dd48b0`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da0a5d30891cb84455c6b13f7a6b778a19b3a271813ef7066eb0ba908192ee7`  
		Last Modified: Tue, 11 May 2021 00:27:20 GMT  
		Size: 1.7 MB (1738012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e2cb2540135f046b5adb4957a0f75118aeb15e30d46af750522a16e6f0cc2`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:78645def8ffaedba4067a39b9ea2318211900b0a00230c004ab61982f9d41958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `caddy:2-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:1b2ba73c8dc7fce225f65c457524b3830589cf0fa3e9c62faa0c88b15c73c74f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5987368241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd19fd51f0fc365a83899a16ab9d8fb86585a512ff6cc33bd07e7af1bc5d89d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:35:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:35:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:35:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:35:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:38:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:39:34 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:19:05 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 20:22:32 GMT
RUN $url = 'https://dl.google.com/go/go1.16.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'd40139b7ade8a3008e3240a6f86fe8f899a9c465c917e11dac8758af216f5eb0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:22:34 GMT
WORKDIR C:\gopath
# Thu, 06 May 2021 21:03:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:03:07 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 00:23:23 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:23:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 00:25:06 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 May 2021 00:25:08 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3360763b706a564d93471b21a342ebbda7e047567cf1cbee82dd592ad33e0c`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0f653700ac9b57cf3d694cc90107e3220fc678581d1e985219677733ce242`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59d82702c225a2ca8cd2a5476122f55d8619eae959c9cb8323b68d70a2ed19`  
		Last Modified: Wed, 14 Apr 2021 12:59:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62435cd2b7652fc97ef3dc1a8968446f3f6e95f0ff1d6dcb176a3f0c2b14c2f8`  
		Last Modified: Wed, 14 Apr 2021 12:59:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d78a3a3d6cb25f55dc9d9947f7449a14717e6b787e49571a837e72b79334cf`  
		Last Modified: Wed, 14 Apr 2021 12:59:41 GMT  
		Size: 30.8 MB (30752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b774a32e346c00e004abbbd7290530d0a3f3dfb11915be2b2fa73c402da6bdd`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d153061f2f0d8ef33f71c4b9afd90899e21556e320d7103a8a9fb544c1cb521`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 5.6 MB (5608025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c85bf3447935a123c186c94d58b02a7e89b566366ab0c7a20b57fbc9e453e1`  
		Last Modified: Thu, 06 May 2021 20:35:33 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7558c3fc6da1f41d9317a885b7d1d896986e9e4a81b6487a543b93ca372649cd`  
		Last Modified: Thu, 06 May 2021 20:36:08 GMT  
		Size: 149.1 MB (149112181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d97cea35310e2e19e356bf67efe44136adb4df53f744e6497511765af70f7e`  
		Last Modified: Thu, 06 May 2021 20:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5214a4bbf455290910bf5850bebdd3fdde0c4bf2616c2975a8a91b62cfe7a`  
		Last Modified: Thu, 06 May 2021 21:06:13 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f9311ef107812e0fc28e80ff17843a7d95e33d9b4311d0ff921022f5d199c3`  
		Last Modified: Thu, 06 May 2021 21:06:10 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b921e314d8bdd24486247a7d82137f437b1572bec858ea76813dc27e580670`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8450625dd9bbf2232b7a3d1cbce4d8795d03b140b1fb962bb6042b82a073633`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394074991c1e1b9a6750cf551fb9f7fe9eaffa1a25889bebcf0f35682cb69afe`  
		Last Modified: Tue, 11 May 2021 00:27:37 GMT  
		Size: 7.0 MB (6993409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5f2fa898b0d7f2684b17b889c9c68aa767c0a1f408e2e4eceb3374cdf48393`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:817273f476c97d5eb6805ecb4f1d622dd1d1eb3fcf0b537151eec68e01df8fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:dee876a8acfe0ad66efe5790b51e5ce47ee105518205c16c1e515107022ee466
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487145585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab04d82b7c1bbab4a4556a4ab389e58cf942f64806603d16b32d02b85377ddc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:15:27 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:15:28 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:16:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:16:04 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:16:06 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:16:07 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:16:08 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:16:10 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:16:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:16:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:16:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:16:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:16:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:16:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:16:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:16:21 GMT
EXPOSE 80
# Tue, 11 May 2021 00:16:22 GMT
EXPOSE 443
# Tue, 11 May 2021 00:16:24 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:16:51 GMT
RUN caddy version
# Tue, 11 May 2021 00:16:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a805066d9e28c5afaf71144648d2270f86d9d1dfbaa0da9a239607694e9315b6`  
		Last Modified: Tue, 11 May 2021 00:26:29 GMT  
		Size: 5.1 MB (5104734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbd0ec6de6085e7571da80b4408f11fada63d710eaf20b44c1ce63847f6455c`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1c04d9585e13e14d3ba056c3a17a8a23821f402c55d603f719fde9885fcc74`  
		Last Modified: Tue, 11 May 2021 00:26:31 GMT  
		Size: 11.9 MB (11930099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27b6dfe0db5cd7aad46afe881c42348361a2c19752cf5629eacb67967b8520`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41902606f9afaae6014164471bda32934d7f0304b3aaa65e2d7480497d85b0bc`  
		Last Modified: Tue, 11 May 2021 00:26:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9ff94e742183a75d4199b58723e286d55ecdd255b03a81ad9ec2b222c85fe1`  
		Last Modified: Tue, 11 May 2021 00:26:25 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1edf08b568698061ffae34580ddf83acab5de417993a30b8a209c919461e6a`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2873cb5c59a087bae99202d1b5f8e424378796848bf9f9f0576cb9e75da8011`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11858529cacdcdc2b7ff911a5df669b21b0efaa8c2fcbde324ccaf0a4a2d4d6`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b96fffb3765e29e3c670d5e14eb09f96a25c0222143cfac7d62c9fa6224896`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b40f5b20f6588f423dc4ba00206ef0b74da9619e96c8c26af206ea104cf85`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9116ab8bdbdeb3f51018f29b3c57d96ed1ebdff8866b0a503c7cb682741e5d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec28519386c9082afe64bc68c2e073b32a2287131bba90c6f56cc9315a638b04`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7649cdb04974c2bf32fa747aadcf57f6402a9c418e9e8f78ada74eae7aec3029`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9652bcbd02b47c702e6f2e8c374f7304cb91ba0186aede9c423104440004857d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33145d7abff94087dd683fd05403939e5aa91276d2693f6c5e8ca28641acd8e1`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a096c1bcb735f9b2cd6bf77eb582dd89b09a6cc75199dd35d65bd5cf6ad50e`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dde82b55b25477fe6eb7381cfdb3e48aa439cbd3f6352e033a85d124cecae7a`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67426815598f918caebff919df817435078c051338bebd944aafb6b25ef593f6`  
		Last Modified: Tue, 11 May 2021 00:26:20 GMT  
		Size: 331.3 KB (331282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf87ebb9031675a0e4407a36e79f274666df2a06d20c2452c1e0acec70fc60a6`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:b61efb630c29dfd10f857eed823207497fd9c94176f47243f48c641119c663d3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818059080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3940d8ab2b2d69a458bd9951c005b3703a5ac35754896cbfd380305f8dfe27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:18:49 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:18:50 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:20:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:20:40 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:20:42 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:20:43 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:20:45 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:20:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:20:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:20:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:20:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:20:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:20:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:20:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:20:56 GMT
EXPOSE 80
# Tue, 11 May 2021 00:20:58 GMT
EXPOSE 443
# Tue, 11 May 2021 00:20:59 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:22:14 GMT
RUN caddy version
# Tue, 11 May 2021 00:22:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc088e7513f9bd5e2261035715cd5f39aff459f086737be39631a5c03dd0bc9`  
		Last Modified: Tue, 11 May 2021 00:27:00 GMT  
		Size: 5.7 MB (5678806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a94477e69ebd7355bfc6230d3309aa20d4fda7d504dc34bd3b2adae7f5f2b4`  
		Last Modified: Tue, 11 May 2021 00:26:57 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db416be1d5a7c97652523c359440855c0ef2127ac11cb08595aa068d99d8a5`  
		Last Modified: Tue, 11 May 2021 00:27:03 GMT  
		Size: 17.2 MB (17201492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e500af558c7988b44d7fae2a1a8c1d4498cb130d1de721a37712c33f09147a`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87b8476ce7fba27f66c08050c4a692f8a19ec0c84e9d42537b4b4b8bbb5f56e`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2d6240d48682965790d983fc3f6b5404aeb7f3f023b517ab83b6e47c20af5c`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757d21ff239a36a372b7fb98d22d42afd8f3c779c7b342605186d6b2a14925e7`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5e64a8fa017a3b5df9f60508bc7b3f72fe2835f00c086648f26235c9358b14`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac63d4edb89dc9920755d7e04e444610a75ac1268b103c178ebff146f490d73`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fbb5cca77bbd06aabe9371bf1fe894938b82367a0ef11be873b231a43b64ab`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b0ecb05ae3d1fffc947acf96dea7fe481fd9a745d4fcf79bff9f4b21a28817`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f292068b665f33bccf70f8100aa252145e0f63abb2283fa29d36cadcc6291c52`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1995472761eea00392fa2ce2d1566a7233a89a019e939892cbb0aeb4a8a3a07a`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e8f37215e61d4f10f002f5ad82c4acadf4a56b559cf036050f33242bfe1e35`  
		Last Modified: Tue, 11 May 2021 00:26:49 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2f6fb7cf636418bada10647c66ee3b92246da967ebb611d58aad6725f5e2b`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271eda8ea06432cb0dae8fd93e8a85314e86201450cdbebf3efcbba2dbd4331`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a4da75f19907c0ee148b5369a63863a2752457cc31b02fe68779d83d56c1`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7013990e537c69857c80a4d6fb386f6d0f04e5a0a5ee5b12ed57c0e458fc8e`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b661b1f2a589a6717a5599a78cb0f3ef950c1a36bd411039dfd39afb20e901b`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 269.3 KB (269349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e686f1164cdcf35434a7d997c0c9ff058302aaade06ace7c5f8a2e4a718aa`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:a72b70da0fa644b846c169807c236cbe93c8103aa45a3e172d7c9247d5ebc445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:dee876a8acfe0ad66efe5790b51e5ce47ee105518205c16c1e515107022ee466
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487145585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab04d82b7c1bbab4a4556a4ab389e58cf942f64806603d16b32d02b85377ddc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:15:27 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:15:28 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:16:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:16:04 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:16:06 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:16:07 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:16:08 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:16:10 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:16:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:16:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:16:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:16:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:16:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:16:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:16:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:16:21 GMT
EXPOSE 80
# Tue, 11 May 2021 00:16:22 GMT
EXPOSE 443
# Tue, 11 May 2021 00:16:24 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:16:51 GMT
RUN caddy version
# Tue, 11 May 2021 00:16:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a805066d9e28c5afaf71144648d2270f86d9d1dfbaa0da9a239607694e9315b6`  
		Last Modified: Tue, 11 May 2021 00:26:29 GMT  
		Size: 5.1 MB (5104734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbd0ec6de6085e7571da80b4408f11fada63d710eaf20b44c1ce63847f6455c`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1c04d9585e13e14d3ba056c3a17a8a23821f402c55d603f719fde9885fcc74`  
		Last Modified: Tue, 11 May 2021 00:26:31 GMT  
		Size: 11.9 MB (11930099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27b6dfe0db5cd7aad46afe881c42348361a2c19752cf5629eacb67967b8520`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41902606f9afaae6014164471bda32934d7f0304b3aaa65e2d7480497d85b0bc`  
		Last Modified: Tue, 11 May 2021 00:26:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9ff94e742183a75d4199b58723e286d55ecdd255b03a81ad9ec2b222c85fe1`  
		Last Modified: Tue, 11 May 2021 00:26:25 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1edf08b568698061ffae34580ddf83acab5de417993a30b8a209c919461e6a`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2873cb5c59a087bae99202d1b5f8e424378796848bf9f9f0576cb9e75da8011`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11858529cacdcdc2b7ff911a5df669b21b0efaa8c2fcbde324ccaf0a4a2d4d6`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b96fffb3765e29e3c670d5e14eb09f96a25c0222143cfac7d62c9fa6224896`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b40f5b20f6588f423dc4ba00206ef0b74da9619e96c8c26af206ea104cf85`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9116ab8bdbdeb3f51018f29b3c57d96ed1ebdff8866b0a503c7cb682741e5d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec28519386c9082afe64bc68c2e073b32a2287131bba90c6f56cc9315a638b04`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7649cdb04974c2bf32fa747aadcf57f6402a9c418e9e8f78ada74eae7aec3029`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9652bcbd02b47c702e6f2e8c374f7304cb91ba0186aede9c423104440004857d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33145d7abff94087dd683fd05403939e5aa91276d2693f6c5e8ca28641acd8e1`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a096c1bcb735f9b2cd6bf77eb582dd89b09a6cc75199dd35d65bd5cf6ad50e`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dde82b55b25477fe6eb7381cfdb3e48aa439cbd3f6352e033a85d124cecae7a`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67426815598f918caebff919df817435078c051338bebd944aafb6b25ef593f6`  
		Last Modified: Tue, 11 May 2021 00:26:20 GMT  
		Size: 331.3 KB (331282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf87ebb9031675a0e4407a36e79f274666df2a06d20c2452c1e0acec70fc60a6`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:54f2ce6cefa5785e781847e6fe0fbe6ce716fb6c5bc0de5a49b4cb71cc8f1cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `caddy:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:b61efb630c29dfd10f857eed823207497fd9c94176f47243f48c641119c663d3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818059080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3940d8ab2b2d69a458bd9951c005b3703a5ac35754896cbfd380305f8dfe27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:18:49 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:18:50 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:20:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:20:40 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:20:42 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:20:43 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:20:45 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:20:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:20:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:20:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:20:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:20:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:20:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:20:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:20:56 GMT
EXPOSE 80
# Tue, 11 May 2021 00:20:58 GMT
EXPOSE 443
# Tue, 11 May 2021 00:20:59 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:22:14 GMT
RUN caddy version
# Tue, 11 May 2021 00:22:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc088e7513f9bd5e2261035715cd5f39aff459f086737be39631a5c03dd0bc9`  
		Last Modified: Tue, 11 May 2021 00:27:00 GMT  
		Size: 5.7 MB (5678806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a94477e69ebd7355bfc6230d3309aa20d4fda7d504dc34bd3b2adae7f5f2b4`  
		Last Modified: Tue, 11 May 2021 00:26:57 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db416be1d5a7c97652523c359440855c0ef2127ac11cb08595aa068d99d8a5`  
		Last Modified: Tue, 11 May 2021 00:27:03 GMT  
		Size: 17.2 MB (17201492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e500af558c7988b44d7fae2a1a8c1d4498cb130d1de721a37712c33f09147a`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87b8476ce7fba27f66c08050c4a692f8a19ec0c84e9d42537b4b4b8bbb5f56e`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2d6240d48682965790d983fc3f6b5404aeb7f3f023b517ab83b6e47c20af5c`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757d21ff239a36a372b7fb98d22d42afd8f3c779c7b342605186d6b2a14925e7`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5e64a8fa017a3b5df9f60508bc7b3f72fe2835f00c086648f26235c9358b14`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac63d4edb89dc9920755d7e04e444610a75ac1268b103c178ebff146f490d73`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fbb5cca77bbd06aabe9371bf1fe894938b82367a0ef11be873b231a43b64ab`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b0ecb05ae3d1fffc947acf96dea7fe481fd9a745d4fcf79bff9f4b21a28817`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f292068b665f33bccf70f8100aa252145e0f63abb2283fa29d36cadcc6291c52`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1995472761eea00392fa2ce2d1566a7233a89a019e939892cbb0aeb4a8a3a07a`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e8f37215e61d4f10f002f5ad82c4acadf4a56b559cf036050f33242bfe1e35`  
		Last Modified: Tue, 11 May 2021 00:26:49 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2f6fb7cf636418bada10647c66ee3b92246da967ebb611d58aad6725f5e2b`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271eda8ea06432cb0dae8fd93e8a85314e86201450cdbebf3efcbba2dbd4331`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a4da75f19907c0ee148b5369a63863a2752457cc31b02fe68779d83d56c1`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7013990e537c69857c80a4d6fb386f6d0f04e5a0a5ee5b12ed57c0e458fc8e`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b661b1f2a589a6717a5599a78cb0f3ef950c1a36bd411039dfd39afb20e901b`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 269.3 KB (269349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e686f1164cdcf35434a7d997c0c9ff058302aaade06ace7c5f8a2e4a718aa`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0`

```console
$ docker pull caddy@sha256:88fc125055b8c4dafe67a48219fd3a89c0a472aa254d2835b2e298b93493b28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.3.0` - linux; amd64

```console
$ docker pull caddy@sha256:6fbf52298c46c55c572670b5395ecaee5d399338003c9bb4e4abed875c542f4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14728953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7395cc3713b2ca5574a9b4aafc468a1533d16582efe47dcab74ed547540d698a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:10:47 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:10:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:10:49 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:10:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:10:53 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:10:53 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:10:54 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:10:55 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:56 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:10:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7a0cd9cca5be9b30bbc70611052d1456502e1f338ce4b14946233b21cd6a9a`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 300.0 KB (300016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5666523658a43fbbdff6b8fca498a988f4dcecc3ce027f1701414658c21d4ea`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b097228407f13a161f68b188b0a4f255855b64d84e7b076745a744d5aa7ed8cf`  
		Last Modified: Wed, 14 Apr 2021 20:11:49 GMT  
		Size: 11.6 MB (11622383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40682d93cc09b4592a1b9c08d48d0a956b5eef4f123d80d1a12942482edb6aab`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0` - linux; arm variant v6

```console
$ docker pull caddy@sha256:0df9df9725cab39fe073887c98b54bf7bf1c96b3ed0e23916737c7c4877576c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13856181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce1c33ce4509195edc1c67d2dcd15c6c5fc0b35cec2e90714ec3007739600eb`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:45:19 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:45:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:45:36 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:45:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:46:03 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:46:04 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:46:05 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:46:07 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:46:08 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:46:10 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:46:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:46:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:46:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:46:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:46:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:46:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:46:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:46:21 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:46:21 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:46:22 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:46:23 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:46:24 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b83e8a6ea044be2a9e3c87c5fdc047ce9a52d1a64e48f8330d9a19002ecffe1`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 300.1 KB (300117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9949bdfbb1d296dd158f8c2bb959f96c8da162a0d579f68fa3f5a4af58bed5b`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c5cc316af29a89f9a1d4e279b5d1bb964095a15795647d013f40921bc808c3`  
		Last Modified: Wed, 14 Apr 2021 19:47:54 GMT  
		Size: 10.9 MB (10944831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6670cc680ce5e5d9a0adfc380fe4a89ac2a2dcef5a7adeb874967a356e6742`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a41623f53d582c8b503ae859f6ae98c7c0695eddb11bdbf8514b9b914955c3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13639723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4b837694902a1a259a4915444feda59d895ed37ffbef66b8518b9a884f029c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:39:25 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:39:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:39:34 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:39:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:39:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:39:43 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:39:45 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:39:46 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:39:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:39:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:39:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:39:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:39:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:39:56 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:39:57 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:39:58 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:39:59 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:40:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b239ad5e698454501b0de011bffea35a660806a0b85a6141776581e3a98bc467`  
		Last Modified: Wed, 14 Apr 2021 19:41:24 GMT  
		Size: 299.2 KB (299210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0460b038be93717158ad9cdb6f83768b7129eaf4fcaef8620adc7509d0e5fe`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0905d1ca8c4f74966ae8a7b5ebe8fdb33854c4a759d543d767dd9a0add81f155`  
		Last Modified: Wed, 14 Apr 2021 19:41:29 GMT  
		Size: 10.9 MB (10925348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02da274f552e184a7fa5527990e666d77c70e3715a0d96b7588e7433b3022a`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:789a609d1ac52d0bed8718bab07beff0633df8333c8f88a4a54ccc6fa14bfb1b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13616003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fab65bcfd86f1922cd2ec38aa336d5c219f99ed0d0878dede9732c770b2113`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:59:52 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 18:59:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 18:59:56 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:00:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:00:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:00:06 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:00:07 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:00:08 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:00:09 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:00:10 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:00:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:00:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:00:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:00:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:00:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:00:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:00:22 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:00:23 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:00:25 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:00:26 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:00:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96638d6a34d0588d1723cae433a6176b83e4bec10cb3a37ffac1891313dd144`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 300.4 KB (300352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27e448c61e8710f135f93f0f19db0e1e20005299e4e28dfcbba2fc048075b11`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955bb49759c02742bb3fe501b864201c3b2a349f8253b73d7114ba39a816ac02`  
		Last Modified: Wed, 14 Apr 2021 19:01:54 GMT  
		Size: 10.6 MB (10598977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639f923159f69301bb290369ef4804ec8ef52d3d159d531976474f8d34d3dc54`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0` - linux; ppc64le

```console
$ docker pull caddy@sha256:f551e1db7910e2d5235d303760aff5b514fc6e8b49d8d67d434bb23c40ac25db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13356454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982bd235f46e537404cdab42c3dfb3d0058f97ed5d7984f2e71ad8734adcc6a8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:22 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Wed, 14 Apr 2021 19:31:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:09:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 22:09:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 22:09:24 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 22:09:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 22:09:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:09:56 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 22:10:01 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 22:10:06 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 22:10:15 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 22:10:22 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 22:10:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 22:10:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 22:10:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 22:10:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 22:10:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 22:11:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 22:11:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 22:11:14 GMT
EXPOSE 80
# Wed, 14 Apr 2021 22:11:20 GMT
EXPOSE 443
# Wed, 14 Apr 2021 22:11:27 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 22:11:35 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 22:11:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93dd31358a6e859a05bb506b946720f02c7ec7969776d811b20eaaa84508cd7`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 302.3 KB (302339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8077b8c9cca163d9a34281a866cf5fe991ff8c160ebd1ab1b617c6b722ec690`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55884816b8eca8150db9473989410e372c69c5431deb51a6cacd029895cf3dd6`  
		Last Modified: Wed, 14 Apr 2021 22:15:43 GMT  
		Size: 10.2 MB (10241380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51efee06e0a650ff5f146fc54a695d4bf2b44e19da18120fdc494982d52cdd62`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0` - linux; s390x

```console
$ docker pull caddy@sha256:68aaf625a22bff4e71edf895129baa2d562765c24ac81a5c68aff2995ebf89c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14146947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfd454f0dfa64ee1a952f9ed74a3f3bda3688a9565f062c3ea37e48b54eb210`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:07:21 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:07:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:07:22 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:07:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:07:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:07:26 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:07:27 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:07:27 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:07:27 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:07:27 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:07:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:07:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:07:30 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:07:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dab58470b754d248933aa56b48394e3ee4db4561d430d23ea378f0371ca59cb`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 300.5 KB (300471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd514b608428ea44dae7dc67e641a276593e7715178d86d7702153521de849d7`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a437814dab55b178c71f55598a70d0b532b3f645bdeb43e89244a6ebcde01446`  
		Last Modified: Wed, 14 Apr 2021 20:08:18 GMT  
		Size: 11.3 MB (11272061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412be9af105c69ee35fec76e8c0dbde8c8ba61c774b7d354e9c9fc8f538e8155`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:fdb259b96e8413c959258115e3cc0ed6272cd362b32dcee80b7c5875b3cca213
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487217133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db78127126d7dbe748dc638552655f6a86f11faa664f34ed256da804f77de223`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:04:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:04:04 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:04:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:04:45 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:04:46 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:04:47 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:04:48 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:04:49 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:04:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:04:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:04:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:04:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:04:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:04:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:04:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:04:58 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:05:00 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:05:01 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:05:27 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:05:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98036a79f108b7c08eb62f3ef539549a6fe005aced8f3fa4971a4e576e8c045`  
		Last Modified: Wed, 14 Apr 2021 20:24:07 GMT  
		Size: 5.1 MB (5081237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1c0c34e473966a69a26492fc168338b6ee1afadedd4cfd3b84537129685128`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88365dd5b6b4b0188ad00f31b1114067b79a05d3eeaecbcdf86385c18e1e2bff`  
		Last Modified: Wed, 14 Apr 2021 20:24:16 GMT  
		Size: 12.0 MB (12047588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8761bc4a54d10c3f03507406d03f0161fece0b4f80913bc67f5218cf7acc0e`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23987f8593afe96ed2b00e5744c51d5678851dac567bde07c230d882b31db5b`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27edd7d612a33644ef095d4bd52c800d8e8a1bd73a56ddbeba0a2cda230947a6`  
		Last Modified: Wed, 14 Apr 2021 20:24:02 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c5b86f636ca1020805b216bf4ea83e1aaa4e5da4145ec671280678483c8084`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f097631ca96d803dd63f72849f1b76728a05c89e8451675f669fc655ae07600`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ace7f5f948c892db540a9734d885fb0695faf8cc55e9fa2df27c4aff76e485d`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57476c73327d061921cee32adad6344e762c80c1142357a6de89819e8577d3e6`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaad63b2ff3aa00f636a1f988a02040c9832ae1a184093cef2471115a787a8f`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1aef5aebcec7bd144ab11a819f8406f07a0dcfaf11684f464b56f5835633fb4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd29f97bbc5cd627a79fc205fd6f63257d27e45e45264ec1e1c3ab94b319e4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aeafc40e34b5ef3464715c082ddb0910edbd9a59ac2d4d9d6586a0022271b4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3fa5d1767b62495151be377ed814c0ce5766f1cb875b724b922d378249bb8`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f7d63263e3b381a5386cd4b13b21226da398d0c8d2bf59f111efb466b9959`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab5798a12c9581184fa73f7b74913b0cf6c4ae638f2886f07d70a9f32181d9a`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf434bfce197fbac09ffe0409a20f2a1ba646801b7dac739c6cea7bed0ce2fad`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0defeab0b694a738dc4b945c883e44f4118a4127f00e4cea32ab589fb194dc`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 308.9 KB (308863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d70335c993ba29c3325465e90a310fce3b41a934bc25ec1bc5220fd3424bfe`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:0a27a5dee7d386c823f3ad85b0ad3c7c6ebb739e7d7ad1cbc37662a3e955dfbc
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818160037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d01f580a5360a74b845ce6ffbd196e0930731b656954f6dafd810f4b69ae72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:07:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:07:15 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:09:01 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:09:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:09:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:09:05 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:09:06 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:09:07 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:09:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:09:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:09:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:09:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:09:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:09:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:09:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:09:16 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:09:17 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:09:18 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:29 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:10:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ea9969fcb8e31829ad2a30ccb77a30f56d17d992051bf6a04b0bd4ebb24a7`  
		Last Modified: Wed, 14 Apr 2021 20:24:45 GMT  
		Size: 5.7 MB (5661064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d2fcf25a0097bf75ef1b7b207a765b3c93bce2eb96e7ebf2ce894a0ca0bf1`  
		Last Modified: Wed, 14 Apr 2021 20:24:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1814c5a2050da8e869a225b62ac936693d7904fed473ed6d703acd42542916`  
		Last Modified: Wed, 14 Apr 2021 20:24:46 GMT  
		Size: 17.3 MB (17333583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93803b6c6c1e5befb69d029873c92020261e4faf5f97fa1ebe4474f2fcd761da`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bef042a1c15ba4cca6086f36ad82e03f037ebae2ec5218dc528ce8afa0cbbe7`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c22fd29bd95221222824495015750f062fcf337845032c4d11be1c8166d9911`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e034d998c8e3152093c8f2c30b0ac9122c528b8ba0889cadf3a3282059a8f96c`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cd579cdba6539c678c1cfd7184427e5b0777e34c965e8c6ca62f8301dd629f`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea0c59c3768ba8d3f4943669c834e3b8043899a0ee61ed325fa453559243f95`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5f4c914fc136d87d2e00167556104cf17827c516e84c53785225cfeb214a42`  
		Last Modified: Wed, 14 Apr 2021 20:24:40 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164712f851736c62b6da95357e6056173e390402e1a17b2f7559af8f42ce0134`  
		Last Modified: Wed, 14 Apr 2021 20:24:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d73f78d7b9ccdb5963233ef77dab1188e2678cc7c9136ff183494cd28f893f0`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b455a43ac6d0be6faf8dce0c59c609cc832963d9cc649b301f49ff79f218e439`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f00b0ac9199b716d513a33d44003af6cd00e4b9b7a2feab64b84649d80640`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ece2a763e6182c580aadb07399f77037c831dd03ee9cdad4f70b18759458094`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac88310e829bdb746ec804044c2a238dc2c6f64660688285a64205a255283c47`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed384ae90a546f9aad4b539596228057299114b9662407a708465a0ed7de3691`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de7a040e97ee693dc826cc6130e42fe7597fbf48fe035d0e5f9f039166edae5`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c1c4ddd499c8a111514a0d3bc3b97381c76a6b33d1cb3f74752d42ddc3e43c`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96251eba56a444a75ccc3480986386b2d2abcce41beadf2f267bedaee332c54a`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0-alpine`

```console
$ docker pull caddy@sha256:fa1ae85dc9b12ee47e98d7ef21db409eada3ed48f1865e4b1f1dd78f417132fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.3.0-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:6fbf52298c46c55c572670b5395ecaee5d399338003c9bb4e4abed875c542f4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14728953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7395cc3713b2ca5574a9b4aafc468a1533d16582efe47dcab74ed547540d698a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:10:47 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:10:49 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:10:49 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:10:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:10:53 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:10:53 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:10:53 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:10:54 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:10:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:10:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:10:55 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:10:56 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:56 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:10:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7a0cd9cca5be9b30bbc70611052d1456502e1f338ce4b14946233b21cd6a9a`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 300.0 KB (300016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5666523658a43fbbdff6b8fca498a988f4dcecc3ce027f1701414658c21d4ea`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b097228407f13a161f68b188b0a4f255855b64d84e7b076745a744d5aa7ed8cf`  
		Last Modified: Wed, 14 Apr 2021 20:11:49 GMT  
		Size: 11.6 MB (11622383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40682d93cc09b4592a1b9c08d48d0a956b5eef4f123d80d1a12942482edb6aab`  
		Last Modified: Wed, 14 Apr 2021 20:11:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:0df9df9725cab39fe073887c98b54bf7bf1c96b3ed0e23916737c7c4877576c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13856181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce1c33ce4509195edc1c67d2dcd15c6c5fc0b35cec2e90714ec3007739600eb`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:45:19 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:45:33 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:45:36 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:45:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:46:03 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:46:04 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:46:05 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:46:07 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:46:08 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:46:10 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:46:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:46:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:46:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:46:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:46:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:46:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:46:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:46:21 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:46:21 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:46:22 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:46:23 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:46:24 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b83e8a6ea044be2a9e3c87c5fdc047ce9a52d1a64e48f8330d9a19002ecffe1`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 300.1 KB (300117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9949bdfbb1d296dd158f8c2bb959f96c8da162a0d579f68fa3f5a4af58bed5b`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c5cc316af29a89f9a1d4e279b5d1bb964095a15795647d013f40921bc808c3`  
		Last Modified: Wed, 14 Apr 2021 19:47:54 GMT  
		Size: 10.9 MB (10944831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6670cc680ce5e5d9a0adfc380fe4a89ac2a2dcef5a7adeb874967a356e6742`  
		Last Modified: Wed, 14 Apr 2021 19:47:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1a41623f53d582c8b503ae859f6ae98c7c0695eddb11bdbf8514b9b914955c3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13639723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4b837694902a1a259a4915444feda59d895ed37ffbef66b8518b9a884f029c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:39:25 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 19:39:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 19:39:34 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:39:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:39:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:39:42 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:39:43 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:39:45 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:39:46 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:39:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:39:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:39:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:39:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:39:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:39:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:39:56 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:39:57 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:39:58 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:39:59 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:40:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b239ad5e698454501b0de011bffea35a660806a0b85a6141776581e3a98bc467`  
		Last Modified: Wed, 14 Apr 2021 19:41:24 GMT  
		Size: 299.2 KB (299210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0460b038be93717158ad9cdb6f83768b7129eaf4fcaef8620adc7509d0e5fe`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0905d1ca8c4f74966ae8a7b5ebe8fdb33854c4a759d543d767dd9a0add81f155`  
		Last Modified: Wed, 14 Apr 2021 19:41:29 GMT  
		Size: 10.9 MB (10925348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02da274f552e184a7fa5527990e666d77c70e3715a0d96b7588e7433b3022a`  
		Last Modified: Wed, 14 Apr 2021 19:41:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:789a609d1ac52d0bed8718bab07beff0633df8333c8f88a4a54ccc6fa14bfb1b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13616003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fab65bcfd86f1922cd2ec38aa336d5c219f99ed0d0878dede9732c770b2113`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:59:52 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 18:59:55 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 18:59:56 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 19:00:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 19:00:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 19:00:06 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 19:00:07 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 19:00:08 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 19:00:09 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 19:00:10 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 19:00:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 19:00:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 19:00:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 19:00:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 19:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 19:00:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 19:00:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 19:00:22 GMT
EXPOSE 80
# Wed, 14 Apr 2021 19:00:23 GMT
EXPOSE 443
# Wed, 14 Apr 2021 19:00:25 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 19:00:26 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 19:00:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96638d6a34d0588d1723cae433a6176b83e4bec10cb3a37ffac1891313dd144`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 300.4 KB (300352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27e448c61e8710f135f93f0f19db0e1e20005299e4e28dfcbba2fc048075b11`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955bb49759c02742bb3fe501b864201c3b2a349f8253b73d7114ba39a816ac02`  
		Last Modified: Wed, 14 Apr 2021 19:01:54 GMT  
		Size: 10.6 MB (10598977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639f923159f69301bb290369ef4804ec8ef52d3d159d531976474f8d34d3dc54`  
		Last Modified: Wed, 14 Apr 2021 19:01:50 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:f551e1db7910e2d5235d303760aff5b514fc6e8b49d8d67d434bb23c40ac25db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13356454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982bd235f46e537404cdab42c3dfb3d0058f97ed5d7984f2e71ad8734adcc6a8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:22 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Wed, 14 Apr 2021 19:31:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:09:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 22:09:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 22:09:24 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 22:09:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 22:09:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:09:56 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 22:10:01 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 22:10:06 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 22:10:15 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 22:10:22 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 22:10:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 22:10:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 22:10:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 22:10:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 22:10:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 22:11:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 22:11:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 22:11:14 GMT
EXPOSE 80
# Wed, 14 Apr 2021 22:11:20 GMT
EXPOSE 443
# Wed, 14 Apr 2021 22:11:27 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 22:11:35 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 22:11:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93dd31358a6e859a05bb506b946720f02c7ec7969776d811b20eaaa84508cd7`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 302.3 KB (302339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8077b8c9cca163d9a34281a866cf5fe991ff8c160ebd1ab1b617c6b722ec690`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55884816b8eca8150db9473989410e372c69c5431deb51a6cacd029895cf3dd6`  
		Last Modified: Wed, 14 Apr 2021 22:15:43 GMT  
		Size: 10.2 MB (10241380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51efee06e0a650ff5f146fc54a695d4bf2b44e19da18120fdc494982d52cdd62`  
		Last Modified: Wed, 14 Apr 2021 22:15:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:68aaf625a22bff4e71edf895129baa2d562765c24ac81a5c68aff2995ebf89c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14146947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfd454f0dfa64ee1a952f9ed74a3f3bda3688a9565f062c3ea37e48b54eb210`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:07:21 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 14 Apr 2021 20:07:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"
# Wed, 14 Apr 2021 20:07:22 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:07:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='7112a03bf341a4ccc5332b5ea715de9a68316d2aa2f468bdc263b192448ce412e002acfda68bd0606088b35c5de1f2e93f2aa64ccc065a039f87ee34e0b85b98' ;; 		armhf)   binArch='armv6'; checksum='a597dbfbd277648881cf51739382a509e5014b3342c78e444f6a680f93836d46c12fc1294e200358fd4a0a40688c5582c81bff14dffd0bba5303170a4d274014' ;; 		armv7)   binArch='armv7'; checksum='99e7703ffa9dd8f636f4624c0972fd3d4af01523953ebf487b919ce93e1989b5513785dd9e902326423eb334bb22dddbcccab382f46763ec11c43c9e513f7c38' ;; 		aarch64) binArch='arm64'; checksum='ef1e44293a935b05602524dbab96b51c862864b8a36c7de48b3329dab9b8a4b7d1930460868fded3afb3a74bdfb5a1c1c0ba46f1401edf648a370c0f7be8a05b' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='62e4a191cae8a1a023ab2653b76439cd4182ca49af4f00bff56507f9f1f4af3e72716a59c59ff157efa87c655110fb2491125baae72590719870dc795d19538d' ;; 		s390x)   binArch='s390x'; checksum='48cac248c29218e153d76408b172510f4f02e3fe7f7b2209371d2c69ed46d2bfa1f572f46390a00eda6f9296a8cac744a36e21cae6df791bd9d98f22b43ea42b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 14 Apr 2021 20:07:26 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:07:26 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 14 Apr 2021 20:07:27 GMT
ENV XDG_DATA_HOME=/data
# Wed, 14 Apr 2021 20:07:27 GMT
VOLUME [/config]
# Wed, 14 Apr 2021 20:07:27 GMT
VOLUME [/data]
# Wed, 14 Apr 2021 20:07:27 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:07:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:07:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:07:29 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:07:29 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:07:30 GMT
WORKDIR /srv
# Wed, 14 Apr 2021 20:07:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dab58470b754d248933aa56b48394e3ee4db4561d430d23ea378f0371ca59cb`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 300.5 KB (300471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd514b608428ea44dae7dc67e641a276593e7715178d86d7702153521de849d7`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a437814dab55b178c71f55598a70d0b532b3f645bdeb43e89244a6ebcde01446`  
		Last Modified: Wed, 14 Apr 2021 20:08:18 GMT  
		Size: 11.3 MB (11272061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412be9af105c69ee35fec76e8c0dbde8c8ba61c774b7d354e9c9fc8f538e8155`  
		Last Modified: Wed, 14 Apr 2021 20:08:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0-builder`

```console
$ docker pull caddy@sha256:c07035362aedef99a6b372f57271b164257d405a0ef4599f35439246bda34d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.3.0-builder` - linux; amd64

```console
$ docker pull caddy@sha256:6740d877ef515ceac8a37a496899fea4d7607bd9831a4a6c990949964ccf3536
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119554161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48e0382f0f224a95381e7fdb346fe40e28931bdec03923e00db3699d75eec90`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:29:08 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:29:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:29:09 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:25:19 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 23:27:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:27:21 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:27:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:27:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:27:22 GMT
WORKDIR /go
# Fri, 07 May 2021 01:56:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:56:04 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 07 May 2021 01:56:04 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 07 May 2021 01:56:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 07 May 2021 01:56:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 07 May 2021 01:56:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 07 May 2021 01:56:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22b54d2d4342f88201f48db57cae1f7edbacae870ee13d7962f999edd7529a9`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5898d3d0f1f95fd666f764bf918c1656be6169868335cb63bc428a5ef47cf32`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7bf786162598b899ee14cad74bdc1c8a634091a242e88aecef7426389cc2c4`  
		Last Modified: Thu, 06 May 2021 23:32:32 GMT  
		Size: 106.8 MB (106834379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6e1c1f19605c012184b2d0a8839483fcd208ac6cec2f7960703fdd1175dfcf`  
		Last Modified: Thu, 06 May 2021 23:32:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271517dcb3cc152671658ffe8a14ad9d506a93ecdf782757e9ae05c710b62b5`  
		Last Modified: Fri, 07 May 2021 01:56:41 GMT  
		Size: 8.3 MB (8326465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9f2fd9dcaaae8f453297e27e74f09fe28520c7c7c8665bc59870f9fabee0f7`  
		Last Modified: Fri, 07 May 2021 01:56:40 GMT  
		Size: 1.3 MB (1311156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e523069c0450345d7a7e25d5d975f68003c2311e50b473eaa1ea30f0586fdc2a`  
		Last Modified: Fri, 07 May 2021 01:56:40 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:980832939db15c6c49b8766e2280086f9f77df42313ceaa4b704ca9f312de749
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114743259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3834a17da42d3f0311833167382a844bb02d9fe3054be01d4fc62f70649d8b6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:19:47 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:19:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:19:52 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:34:21 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 21:37:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 21:37:16 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 21:37:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:37:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 21:37:22 GMT
WORKDIR /go
# Thu, 06 May 2021 22:09:57 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 06 May 2021 22:09:58 GMT
ENV XCADDY_VERSION=v0.1.9
# Thu, 06 May 2021 22:09:59 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 06 May 2021 22:10:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 06 May 2021 22:10:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 06 May 2021 22:10:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 06 May 2021 22:10:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76c231c184d802a569805e44837dd1ea2cb0522bb03ca5763ef5ed9fae5896c`  
		Last Modified: Wed, 14 Apr 2021 21:15:05 GMT  
		Size: 281.0 KB (280982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8ca9e585b85be2e7ddaaf213e22bdb986eba4da2a8cc4d8b45f762752e17df`  
		Last Modified: Wed, 14 Apr 2021 21:15:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207e70e1aafbd96d35878b34eac9d70629c7d0d5c95d6a6d595497dc16384314`  
		Last Modified: Thu, 06 May 2021 21:40:38 GMT  
		Size: 102.7 MB (102690906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafdae0ee7bc20a8ce52360fd0237c2d561f4dda69b5221756ee2fb08f3a25e9`  
		Last Modified: Thu, 06 May 2021 21:40:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37943907ed09326e414a914b2f13d600e2a94f806a260c7941e9930dc8e914db`  
		Last Modified: Thu, 06 May 2021 22:10:53 GMT  
		Size: 7.9 MB (7943728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a400fa97dfdb53333f7d2d7405ff6f39461b2e43eb8337b0b06fff17c362074c`  
		Last Modified: Thu, 06 May 2021 22:10:52 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fed79ee3fc09876eea261ab1cde8d9107b041a4d873ab2dbcacdc0f0b0db47`  
		Last Modified: Thu, 06 May 2021 22:10:51 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:6a27d36624d8ceafd50f9caf199d8583315839b6e47617242194192b6443fad3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113547980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc13dd897b9d3a097309d0364885377e102cd91c4dcec23ffd64375520f0029b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:28:16 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:28:21 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:28:26 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:22:53 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 23:25:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:25:38 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:25:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:25:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:25:46 GMT
WORKDIR /go
# Fri, 07 May 2021 02:33:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:33:55 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 07 May 2021 02:33:56 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 07 May 2021 02:33:56 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 07 May 2021 02:33:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 07 May 2021 02:33:59 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 07 May 2021 02:34:00 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a884c3a8500725e0f08f924091ec61ae3e3acee3b0ffe5839b06f874ee63dc08`  
		Last Modified: Wed, 14 Apr 2021 22:45:08 GMT  
		Size: 280.1 KB (280078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f87f08a98de1e7cb636267b626d4e644775ff7962ea1ff9b4813f740b89e67`  
		Last Modified: Wed, 14 Apr 2021 22:45:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73018330efc261efdcdccd072ee7b6ea3dc05bab6b4760a1ec828924d12acf96`  
		Last Modified: Thu, 06 May 2021 23:31:44 GMT  
		Size: 102.5 MB (102483682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12ff58945623ccdd317243b312562a87a60534d35bb0a88f1e2bdd4b800450a`  
		Last Modified: Thu, 06 May 2021 23:31:14 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada1f2ae57155d23410debd2de0fed3f494ac4cedb2d716f10ac64aa8f49350c`  
		Last Modified: Fri, 07 May 2021 02:34:45 GMT  
		Size: 7.2 MB (7154830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6132f297784ed0d2a64f3581da395b458a6ad21b2a884c3dbabf79410415362c`  
		Last Modified: Fri, 07 May 2021 02:34:44 GMT  
		Size: 1.2 MB (1219497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dd68f4d45c90ed4b3be4d5335c923e68cdd3317597b2575fabbdacf45f38fc`  
		Last Modified: Fri, 07 May 2021 02:34:44 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b7a5c24ebc428a66842618e2ad381544cd986e997f453e0d9a2f671ad0bfa2f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114864048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d2bfdb86bdd828c562eee0c551e06aa4e79276d99135f5bd2b7cfe798aed31`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:46:09 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:46:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:46:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:39:55 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 22:41:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 22:41:48 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 22:41:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:41:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 22:41:52 GMT
WORKDIR /go
# Fri, 07 May 2021 01:16:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:16:57 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 07 May 2021 01:16:57 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 07 May 2021 01:16:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 07 May 2021 01:17:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 07 May 2021 01:17:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 07 May 2021 01:17:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2150ab4b89a5dc832780f442998074db1582348dca0eb60d6b79b59df025f25f`  
		Last Modified: Wed, 14 Apr 2021 21:00:21 GMT  
		Size: 281.2 KB (281220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9d22c0ca7447b1a1b25889675e84f2ed68ecd519fdc513796712138820633b`  
		Last Modified: Wed, 14 Apr 2021 21:00:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2328eb5d68387c28c06740854a27e1f61291595913519fa3169b91f9b46bb9ca`  
		Last Modified: Thu, 06 May 2021 22:47:05 GMT  
		Size: 102.2 MB (102151470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2893b907041eb1a7fdd24da73ae2cfa10e6f9286ae37b7d7b77b3b322d2fafe1`  
		Last Modified: Thu, 06 May 2021 22:46:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02c9359228d2ef91a5f155bf4eb9cacf4d7a44958e4374cc497939e854cbedc`  
		Last Modified: Fri, 07 May 2021 01:17:51 GMT  
		Size: 8.5 MB (8518410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7b89f42f011d15cd85b0d0d03916e5eaa1015e732785e1508631c9d52a7ac3`  
		Last Modified: Fri, 07 May 2021 01:17:49 GMT  
		Size: 1.2 MB (1201538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f53e0aeae2a617ee063849011cb33db824b4ba6b3970945825fa7aed9143db`  
		Last Modified: Fri, 07 May 2021 01:17:49 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:91017bdca5b5a6e529ba9dbbf8b4cc0f1abad484dd2a19ff8162e5a20f1b7470
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114013692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c636d928211d0eebf80ad41447aae081460c4d3673fbb846379e0f71a65c581c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:22 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Wed, 14 Apr 2021 19:31:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:57:05 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 22:57:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:57:16 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:35:58 GMT
ENV GOLANG_VERSION=1.15.12
# Fri, 07 May 2021 00:38:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 07 May 2021 00:38:24 GMT
ENV GOPATH=/go
# Fri, 07 May 2021 00:38:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:38:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 07 May 2021 00:38:53 GMT
WORKDIR /go
# Fri, 07 May 2021 08:18:14 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 08:18:28 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 07 May 2021 08:18:33 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 07 May 2021 08:18:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 07 May 2021 08:19:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 07 May 2021 08:19:05 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 07 May 2021 08:19:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dca7bf08f7e7ef8f1c651b5ba53ba748e66f5a75400b38f67596867bfae4e2`  
		Last Modified: Wed, 14 Apr 2021 23:06:16 GMT  
		Size: 283.2 KB (283201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d495ca184c89fdc74ec1ec1cc670ff41be844b29174141c4602ac1400b0645`  
		Last Modified: Wed, 14 Apr 2021 23:06:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6d75cc8304f9250be10afcbb80447f234d1f01911e86274118bb6fdc34ed48`  
		Last Modified: Fri, 07 May 2021 00:44:07 GMT  
		Size: 100.8 MB (100812628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0997c196aa13c6e561f3432b7239d95ee90562c507e5a8c4f21acfcf1e17f5e3`  
		Last Modified: Fri, 07 May 2021 00:43:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb6e06aa8363e1138fed17e9f2a879be30ac49ebdee6931f49ea76200a4cab3`  
		Last Modified: Fri, 07 May 2021 08:22:00 GMT  
		Size: 8.9 MB (8939878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedccec34d2dc5617dde35e772984f1c60c1cf730c13faeef29d2ecf217b24df`  
		Last Modified: Fri, 07 May 2021 08:21:58 GMT  
		Size: 1.2 MB (1170522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b959e44e74065aea1788a48f30813a54b7121ff398a293ed94b2d6d370f57d8`  
		Last Modified: Fri, 07 May 2021 08:21:58 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder` - linux; s390x

```console
$ docker pull caddy@sha256:0de068b7cd9c14fc067305805ff915769769fc9cd7d7daafe247873960c9e481
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118429363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d6106b96bf5579d67b5457592a4408517a6015fbcd4144b7e04407d47a04d3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:46:59 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:47:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:47:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:29:16 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 23:32:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:32:38 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:32:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:32:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:32:41 GMT
WORKDIR /go
# Fri, 07 May 2021 02:02:15 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:02:15 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 07 May 2021 02:02:16 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 07 May 2021 02:02:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 07 May 2021 02:02:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 07 May 2021 02:02:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 07 May 2021 02:02:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c29c45d0e43ef7a36e47dfc16916a076f7ba26b656842380c26207ad30f5c8b`  
		Last Modified: Wed, 14 Apr 2021 20:52:52 GMT  
		Size: 281.3 KB (281343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f1645d6cbfccd2924337f37dc819e7edc27989ead8bc679441954a0e483c24`  
		Last Modified: Wed, 14 Apr 2021 20:52:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e82967ca9bc6ee6bdd75fdc4f9b9000c6fcb2c25b0d754591f4ea080d22c48`  
		Last Modified: Thu, 06 May 2021 23:36:04 GMT  
		Size: 105.9 MB (105944163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f7138aca5efa6f3f896323bc1d8d7e86ac97dc43934f657be7b59764fd1a93`  
		Last Modified: Thu, 06 May 2021 23:35:48 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1fc295bef09a7a41613606b2fab0bb9a2f237a924f638bbc1471e4cf7e8b91`  
		Last Modified: Fri, 07 May 2021 02:03:09 GMT  
		Size: 8.4 MB (8370195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e637a1eb5e336e7d0f477e2470ceb6a4501f134379834cd84e644993a10c733c`  
		Last Modified: Fri, 07 May 2021 02:03:08 GMT  
		Size: 1.3 MB (1264520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eeaadfe4374cccb5c1a67a72e18041ebe4ad77c344002126dc56db880377cfa`  
		Last Modified: Fri, 07 May 2021 02:03:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:8f4d4f165e89bd96ab3b55a4aaba1bbcdc01684f39842f7c14f29af9556a26ad
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2636156875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d926ae841023f3fb8cab1d9adff32345364c1cf5deb01395829a12bb325df2d2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:30:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:30:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:30:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:30:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:31:57 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:32:38 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:25:15 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 20:27:40 GMT
RUN $url = 'https://dl.google.com/go/go1.15.12.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '313e5ebc59b497319c4c3f9560322fcc20f7bc3b4e47494afc3b2d63a42fb2a5'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:27:42 GMT
WORKDIR C:\gopath
# Thu, 06 May 2021 21:00:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:00:18 GMT
ENV XCADDY_VERSION=v0.1.9
# Thu, 06 May 2021 21:00:19 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 06 May 2021 21:00:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 06 May 2021 21:00:45 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 06 May 2021 21:00:46 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac56922ba0ee0ac19bcae98f5fb4b7427d31ef3c709f27cfb2c785fd13a611c4`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1723430d5101a2d617d3dbf4bc2a121b3f4b4432105aa2941e1afab8f130b9`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f4dc6e9a77d69a3d172368f4ae471b31c588d6201c2386e4ac62fd83faa16`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea47861a9221a4f1e5750db237c619796c612756a5e75e2cb443b1731ae8a8`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4be4ebd8eabefdb01f27dafad85e65289b95ca15591c14304c7792db99b54b`  
		Last Modified: Wed, 14 Apr 2021 12:58:35 GMT  
		Size: 30.2 MB (30155601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f66ae3738a83ea41b428b49261d4522d57df1617fbd1aa362d93f1e2802643`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2108b314c24064a0c250f72017cc64b3bf68915655327728a267c98985a5ff7`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 324.6 KB (324649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16415296d3face20e924a55c6188167fe6fcec8047853d9a3329fd32ecfa809`  
		Last Modified: Thu, 06 May 2021 20:37:12 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfe9ab81ed864e1e57abe3b9de7dce25175ae2c9fb0dd05299b91a7c82af9c8`  
		Last Modified: Thu, 06 May 2021 20:39:47 GMT  
		Size: 134.2 MB (134170498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733982d15b62bc69f88a8ef0f14899354430a2e53109d6d5df680cfc24ca8ef3`  
		Last Modified: Thu, 06 May 2021 20:37:11 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc4ffe1de31b221cc09e55858e01b0a9463a797f2c7e0b7bf268d64508ea6db`  
		Last Modified: Thu, 06 May 2021 21:05:22 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea9e8041c91dd904fd8c0baca19b1928ef24e735180c202eb75fdc020a0b553`  
		Last Modified: Thu, 06 May 2021 21:05:19 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e5475c94630ce13e033d293ae16e48f43444482ecf3103b1876bd4281c74dc`  
		Last Modified: Thu, 06 May 2021 21:05:19 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57691d3ea242e7a1f0ac122639479d29884e42e1bfa260d539d0234558754df`  
		Last Modified: Thu, 06 May 2021 21:05:19 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63160481b402cb93d7aebf5f74c44b08d31bfe77ef3993bfa4e67705da57db48`  
		Last Modified: Thu, 06 May 2021 21:05:20 GMT  
		Size: 1.7 MB (1733758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6270fca3a63ff5136511a134f0f03f9cda4450f24220e76fa971ede16b4944d`  
		Last Modified: Thu, 06 May 2021 21:05:19 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:52c6e3d6ca5952ddd858264545275503420e98c397069b20af701ffb27332f80
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5982176037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d70484e9a3340b6f158df0bfb46df082eaff70c0443b954599df5cb22a8bccf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:35:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:35:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:35:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:35:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:38:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:39:34 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:27:58 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 20:31:23 GMT
RUN $url = 'https://dl.google.com/go/go1.15.12.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '313e5ebc59b497319c4c3f9560322fcc20f7bc3b4e47494afc3b2d63a42fb2a5'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:31:25 GMT
WORKDIR C:\gopath
# Thu, 06 May 2021 21:00:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:00:56 GMT
ENV XCADDY_VERSION=v0.1.9
# Thu, 06 May 2021 21:00:57 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 06 May 2021 21:00:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 06 May 2021 21:02:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 06 May 2021 21:02:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3360763b706a564d93471b21a342ebbda7e047567cf1cbee82dd592ad33e0c`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0f653700ac9b57cf3d694cc90107e3220fc678581d1e985219677733ce242`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59d82702c225a2ca8cd2a5476122f55d8619eae959c9cb8323b68d70a2ed19`  
		Last Modified: Wed, 14 Apr 2021 12:59:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62435cd2b7652fc97ef3dc1a8968446f3f6e95f0ff1d6dcb176a3f0c2b14c2f8`  
		Last Modified: Wed, 14 Apr 2021 12:59:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d78a3a3d6cb25f55dc9d9947f7449a14717e6b787e49571a837e72b79334cf`  
		Last Modified: Wed, 14 Apr 2021 12:59:41 GMT  
		Size: 30.8 MB (30752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b774a32e346c00e004abbbd7290530d0a3f3dfb11915be2b2fa73c402da6bdd`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d153061f2f0d8ef33f71c4b9afd90899e21556e320d7103a8a9fb544c1cb521`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 5.6 MB (5608025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77293b9e38b389fb10ca47df8ebed52eaa8d0b9d8fe67701f41f353b87fff7dd`  
		Last Modified: Thu, 06 May 2021 20:39:59 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5820129044179dd743c12eb760d4dc1b649b453884dbbc676f43db154e398755`  
		Last Modified: Thu, 06 May 2021 20:40:32 GMT  
		Size: 143.9 MB (143920323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e148ea2e33c621c36032ed6f1fe0e45feb3394fcf0a1b5fc24918333d9da7222`  
		Last Modified: Thu, 06 May 2021 20:39:59 GMT  
		Size: 1.6 KB (1587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b609033068047241fcc0a4f67b4a06a1daa731a5ebb2835f75f12db601fe90`  
		Last Modified: Thu, 06 May 2021 21:05:39 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af22c6a21c6ad89bffef63695e5b396725b1d542e49b9082bb17e5c9d98d4d9`  
		Last Modified: Thu, 06 May 2021 21:05:36 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e3edba755c397ed87f591e2eac50e2d1f992934d53e25a88d20c1925ff0ba4`  
		Last Modified: Thu, 06 May 2021 21:05:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b4285d0784135391adbf8943455eeae65aad2fbcc56386c6629a749ccbbd5a`  
		Last Modified: Thu, 06 May 2021 21:05:36 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3c1e1ca4ddc1f2725e123cd6fd1452388065bf5639107cbdf74c756f0b7a90`  
		Last Modified: Thu, 06 May 2021 21:05:44 GMT  
		Size: 7.0 MB (6993022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f61c3066c0e78987570ac749619beed620b38bb2851df7ca1a195e1ea279040`  
		Last Modified: Thu, 06 May 2021 21:05:36 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0-builder-alpine`

```console
$ docker pull caddy@sha256:e06d5cdcee711e9580fe595e8f03d31e17394fba29865720a64ddee23892b4a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.3.0-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:6740d877ef515ceac8a37a496899fea4d7607bd9831a4a6c990949964ccf3536
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119554161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48e0382f0f224a95381e7fdb346fe40e28931bdec03923e00db3699d75eec90`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:29:08 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:29:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:29:09 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:25:19 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 23:27:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:27:21 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:27:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:27:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:27:22 GMT
WORKDIR /go
# Fri, 07 May 2021 01:56:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:56:04 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 07 May 2021 01:56:04 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 07 May 2021 01:56:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 07 May 2021 01:56:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 07 May 2021 01:56:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 07 May 2021 01:56:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22b54d2d4342f88201f48db57cae1f7edbacae870ee13d7962f999edd7529a9`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5898d3d0f1f95fd666f764bf918c1656be6169868335cb63bc428a5ef47cf32`  
		Last Modified: Wed, 14 Apr 2021 21:35:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7bf786162598b899ee14cad74bdc1c8a634091a242e88aecef7426389cc2c4`  
		Last Modified: Thu, 06 May 2021 23:32:32 GMT  
		Size: 106.8 MB (106834379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6e1c1f19605c012184b2d0a8839483fcd208ac6cec2f7960703fdd1175dfcf`  
		Last Modified: Thu, 06 May 2021 23:32:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271517dcb3cc152671658ffe8a14ad9d506a93ecdf782757e9ae05c710b62b5`  
		Last Modified: Fri, 07 May 2021 01:56:41 GMT  
		Size: 8.3 MB (8326465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9f2fd9dcaaae8f453297e27e74f09fe28520c7c7c8665bc59870f9fabee0f7`  
		Last Modified: Fri, 07 May 2021 01:56:40 GMT  
		Size: 1.3 MB (1311156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e523069c0450345d7a7e25d5d975f68003c2311e50b473eaa1ea30f0586fdc2a`  
		Last Modified: Fri, 07 May 2021 01:56:40 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:980832939db15c6c49b8766e2280086f9f77df42313ceaa4b704ca9f312de749
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114743259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3834a17da42d3f0311833167382a844bb02d9fe3054be01d4fc62f70649d8b6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:19:47 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:19:50 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:19:52 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:34:21 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 21:37:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 21:37:16 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 21:37:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:37:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 21:37:22 GMT
WORKDIR /go
# Thu, 06 May 2021 22:09:57 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 06 May 2021 22:09:58 GMT
ENV XCADDY_VERSION=v0.1.9
# Thu, 06 May 2021 22:09:59 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 06 May 2021 22:10:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 06 May 2021 22:10:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 06 May 2021 22:10:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 06 May 2021 22:10:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76c231c184d802a569805e44837dd1ea2cb0522bb03ca5763ef5ed9fae5896c`  
		Last Modified: Wed, 14 Apr 2021 21:15:05 GMT  
		Size: 281.0 KB (280982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8ca9e585b85be2e7ddaaf213e22bdb986eba4da2a8cc4d8b45f762752e17df`  
		Last Modified: Wed, 14 Apr 2021 21:15:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207e70e1aafbd96d35878b34eac9d70629c7d0d5c95d6a6d595497dc16384314`  
		Last Modified: Thu, 06 May 2021 21:40:38 GMT  
		Size: 102.7 MB (102690906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafdae0ee7bc20a8ce52360fd0237c2d561f4dda69b5221756ee2fb08f3a25e9`  
		Last Modified: Thu, 06 May 2021 21:40:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37943907ed09326e414a914b2f13d600e2a94f806a260c7941e9930dc8e914db`  
		Last Modified: Thu, 06 May 2021 22:10:53 GMT  
		Size: 7.9 MB (7943728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a400fa97dfdb53333f7d2d7405ff6f39461b2e43eb8337b0b06fff17c362074c`  
		Last Modified: Thu, 06 May 2021 22:10:52 GMT  
		Size: 1.2 MB (1221675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fed79ee3fc09876eea261ab1cde8d9107b041a4d873ab2dbcacdc0f0b0db47`  
		Last Modified: Thu, 06 May 2021 22:10:51 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:6a27d36624d8ceafd50f9caf199d8583315839b6e47617242194192b6443fad3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113547980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc13dd897b9d3a097309d0364885377e102cd91c4dcec23ffd64375520f0029b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:28:16 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:28:21 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:28:26 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:22:53 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 23:25:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:25:38 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:25:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:25:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:25:46 GMT
WORKDIR /go
# Fri, 07 May 2021 02:33:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:33:55 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 07 May 2021 02:33:56 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 07 May 2021 02:33:56 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 07 May 2021 02:33:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 07 May 2021 02:33:59 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 07 May 2021 02:34:00 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a884c3a8500725e0f08f924091ec61ae3e3acee3b0ffe5839b06f874ee63dc08`  
		Last Modified: Wed, 14 Apr 2021 22:45:08 GMT  
		Size: 280.1 KB (280078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f87f08a98de1e7cb636267b626d4e644775ff7962ea1ff9b4813f740b89e67`  
		Last Modified: Wed, 14 Apr 2021 22:45:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73018330efc261efdcdccd072ee7b6ea3dc05bab6b4760a1ec828924d12acf96`  
		Last Modified: Thu, 06 May 2021 23:31:44 GMT  
		Size: 102.5 MB (102483682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12ff58945623ccdd317243b312562a87a60534d35bb0a88f1e2bdd4b800450a`  
		Last Modified: Thu, 06 May 2021 23:31:14 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada1f2ae57155d23410debd2de0fed3f494ac4cedb2d716f10ac64aa8f49350c`  
		Last Modified: Fri, 07 May 2021 02:34:45 GMT  
		Size: 7.2 MB (7154830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6132f297784ed0d2a64f3581da395b458a6ad21b2a884c3dbabf79410415362c`  
		Last Modified: Fri, 07 May 2021 02:34:44 GMT  
		Size: 1.2 MB (1219497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dd68f4d45c90ed4b3be4d5335c923e68cdd3317597b2575fabbdacf45f38fc`  
		Last Modified: Fri, 07 May 2021 02:34:44 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b7a5c24ebc428a66842618e2ad381544cd986e997f453e0d9a2f671ad0bfa2f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114864048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d2bfdb86bdd828c562eee0c551e06aa4e79276d99135f5bd2b7cfe798aed31`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:46:09 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:46:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:46:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:39:55 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 22:41:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 22:41:48 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 22:41:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:41:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 22:41:52 GMT
WORKDIR /go
# Fri, 07 May 2021 01:16:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:16:57 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 07 May 2021 01:16:57 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 07 May 2021 01:16:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 07 May 2021 01:17:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 07 May 2021 01:17:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 07 May 2021 01:17:04 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2150ab4b89a5dc832780f442998074db1582348dca0eb60d6b79b59df025f25f`  
		Last Modified: Wed, 14 Apr 2021 21:00:21 GMT  
		Size: 281.2 KB (281220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9d22c0ca7447b1a1b25889675e84f2ed68ecd519fdc513796712138820633b`  
		Last Modified: Wed, 14 Apr 2021 21:00:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2328eb5d68387c28c06740854a27e1f61291595913519fa3169b91f9b46bb9ca`  
		Last Modified: Thu, 06 May 2021 22:47:05 GMT  
		Size: 102.2 MB (102151470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2893b907041eb1a7fdd24da73ae2cfa10e6f9286ae37b7d7b77b3b322d2fafe1`  
		Last Modified: Thu, 06 May 2021 22:46:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02c9359228d2ef91a5f155bf4eb9cacf4d7a44958e4374cc497939e854cbedc`  
		Last Modified: Fri, 07 May 2021 01:17:51 GMT  
		Size: 8.5 MB (8518410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7b89f42f011d15cd85b0d0d03916e5eaa1015e732785e1508631c9d52a7ac3`  
		Last Modified: Fri, 07 May 2021 01:17:49 GMT  
		Size: 1.2 MB (1201538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f53e0aeae2a617ee063849011cb33db824b4ba6b3970945825fa7aed9143db`  
		Last Modified: Fri, 07 May 2021 01:17:49 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:91017bdca5b5a6e529ba9dbbf8b4cc0f1abad484dd2a19ff8162e5a20f1b7470
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114013692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c636d928211d0eebf80ad41447aae081460c4d3673fbb846379e0f71a65c581c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:22 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Wed, 14 Apr 2021 19:31:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:57:05 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 22:57:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:57:16 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:35:58 GMT
ENV GOLANG_VERSION=1.15.12
# Fri, 07 May 2021 00:38:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 07 May 2021 00:38:24 GMT
ENV GOPATH=/go
# Fri, 07 May 2021 00:38:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:38:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 07 May 2021 00:38:53 GMT
WORKDIR /go
# Fri, 07 May 2021 08:18:14 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 08:18:28 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 07 May 2021 08:18:33 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 07 May 2021 08:18:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 07 May 2021 08:19:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 07 May 2021 08:19:05 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 07 May 2021 08:19:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dca7bf08f7e7ef8f1c651b5ba53ba748e66f5a75400b38f67596867bfae4e2`  
		Last Modified: Wed, 14 Apr 2021 23:06:16 GMT  
		Size: 283.2 KB (283201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d495ca184c89fdc74ec1ec1cc670ff41be844b29174141c4602ac1400b0645`  
		Last Modified: Wed, 14 Apr 2021 23:06:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6d75cc8304f9250be10afcbb80447f234d1f01911e86274118bb6fdc34ed48`  
		Last Modified: Fri, 07 May 2021 00:44:07 GMT  
		Size: 100.8 MB (100812628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0997c196aa13c6e561f3432b7239d95ee90562c507e5a8c4f21acfcf1e17f5e3`  
		Last Modified: Fri, 07 May 2021 00:43:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb6e06aa8363e1138fed17e9f2a879be30ac49ebdee6931f49ea76200a4cab3`  
		Last Modified: Fri, 07 May 2021 08:22:00 GMT  
		Size: 8.9 MB (8939878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedccec34d2dc5617dde35e772984f1c60c1cf730c13faeef29d2ecf217b24df`  
		Last Modified: Fri, 07 May 2021 08:21:58 GMT  
		Size: 1.2 MB (1170522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b959e44e74065aea1788a48f30813a54b7121ff398a293ed94b2d6d370f57d8`  
		Last Modified: Fri, 07 May 2021 08:21:58 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:0de068b7cd9c14fc067305805ff915769769fc9cd7d7daafe247873960c9e481
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118429363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d6106b96bf5579d67b5457592a4408517a6015fbcd4144b7e04407d47a04d3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:46:59 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:47:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:47:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:29:16 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 23:32:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='387' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.15.12.src.tar.gz'; 	sha256='1c6911937df4a277fa74e7b7efc3d08594498c4c4adc0b6c4ae3566137528091'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:32:38 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:32:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:32:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:32:41 GMT
WORKDIR /go
# Fri, 07 May 2021 02:02:15 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:02:15 GMT
ENV XCADDY_VERSION=v0.1.9
# Fri, 07 May 2021 02:02:16 GMT
ENV CADDY_VERSION=v2.3.0
# Fri, 07 May 2021 02:02:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 07 May 2021 02:02:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 07 May 2021 02:02:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 07 May 2021 02:02:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c29c45d0e43ef7a36e47dfc16916a076f7ba26b656842380c26207ad30f5c8b`  
		Last Modified: Wed, 14 Apr 2021 20:52:52 GMT  
		Size: 281.3 KB (281343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f1645d6cbfccd2924337f37dc819e7edc27989ead8bc679441954a0e483c24`  
		Last Modified: Wed, 14 Apr 2021 20:52:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e82967ca9bc6ee6bdd75fdc4f9b9000c6fcb2c25b0d754591f4ea080d22c48`  
		Last Modified: Thu, 06 May 2021 23:36:04 GMT  
		Size: 105.9 MB (105944163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f7138aca5efa6f3f896323bc1d8d7e86ac97dc43934f657be7b59764fd1a93`  
		Last Modified: Thu, 06 May 2021 23:35:48 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1fc295bef09a7a41613606b2fab0bb9a2f237a924f638bbc1471e4cf7e8b91`  
		Last Modified: Fri, 07 May 2021 02:03:09 GMT  
		Size: 8.4 MB (8370195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e637a1eb5e336e7d0f477e2470ceb6a4501f134379834cd84e644993a10c733c`  
		Last Modified: Fri, 07 May 2021 02:03:08 GMT  
		Size: 1.3 MB (1264520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eeaadfe4374cccb5c1a67a72e18041ebe4ad77c344002126dc56db880377cfa`  
		Last Modified: Fri, 07 May 2021 02:03:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:9967ade45e8ffa17f8eda816bded85bfe3dea8bc64cb370d6cd5647873d3cc0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `caddy:2.3.0-builder-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:8f4d4f165e89bd96ab3b55a4aaba1bbcdc01684f39842f7c14f29af9556a26ad
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2636156875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d926ae841023f3fb8cab1d9adff32345364c1cf5deb01395829a12bb325df2d2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:30:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:30:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:30:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:30:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:31:57 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:32:38 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:25:15 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 20:27:40 GMT
RUN $url = 'https://dl.google.com/go/go1.15.12.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '313e5ebc59b497319c4c3f9560322fcc20f7bc3b4e47494afc3b2d63a42fb2a5'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:27:42 GMT
WORKDIR C:\gopath
# Thu, 06 May 2021 21:00:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:00:18 GMT
ENV XCADDY_VERSION=v0.1.9
# Thu, 06 May 2021 21:00:19 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 06 May 2021 21:00:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 06 May 2021 21:00:45 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 06 May 2021 21:00:46 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac56922ba0ee0ac19bcae98f5fb4b7427d31ef3c709f27cfb2c785fd13a611c4`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1723430d5101a2d617d3dbf4bc2a121b3f4b4432105aa2941e1afab8f130b9`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f4dc6e9a77d69a3d172368f4ae471b31c588d6201c2386e4ac62fd83faa16`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea47861a9221a4f1e5750db237c619796c612756a5e75e2cb443b1731ae8a8`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4be4ebd8eabefdb01f27dafad85e65289b95ca15591c14304c7792db99b54b`  
		Last Modified: Wed, 14 Apr 2021 12:58:35 GMT  
		Size: 30.2 MB (30155601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f66ae3738a83ea41b428b49261d4522d57df1617fbd1aa362d93f1e2802643`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2108b314c24064a0c250f72017cc64b3bf68915655327728a267c98985a5ff7`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 324.6 KB (324649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16415296d3face20e924a55c6188167fe6fcec8047853d9a3329fd32ecfa809`  
		Last Modified: Thu, 06 May 2021 20:37:12 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfe9ab81ed864e1e57abe3b9de7dce25175ae2c9fb0dd05299b91a7c82af9c8`  
		Last Modified: Thu, 06 May 2021 20:39:47 GMT  
		Size: 134.2 MB (134170498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733982d15b62bc69f88a8ef0f14899354430a2e53109d6d5df680cfc24ca8ef3`  
		Last Modified: Thu, 06 May 2021 20:37:11 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc4ffe1de31b221cc09e55858e01b0a9463a797f2c7e0b7bf268d64508ea6db`  
		Last Modified: Thu, 06 May 2021 21:05:22 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea9e8041c91dd904fd8c0baca19b1928ef24e735180c202eb75fdc020a0b553`  
		Last Modified: Thu, 06 May 2021 21:05:19 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e5475c94630ce13e033d293ae16e48f43444482ecf3103b1876bd4281c74dc`  
		Last Modified: Thu, 06 May 2021 21:05:19 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57691d3ea242e7a1f0ac122639479d29884e42e1bfa260d539d0234558754df`  
		Last Modified: Thu, 06 May 2021 21:05:19 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63160481b402cb93d7aebf5f74c44b08d31bfe77ef3993bfa4e67705da57db48`  
		Last Modified: Thu, 06 May 2021 21:05:20 GMT  
		Size: 1.7 MB (1733758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6270fca3a63ff5136511a134f0f03f9cda4450f24220e76fa971ede16b4944d`  
		Last Modified: Thu, 06 May 2021 21:05:19 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:527a997e7ab014059d378ab66388468c87b086a0752de107a0fdd8fe6adab4d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.3.0-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:52c6e3d6ca5952ddd858264545275503420e98c397069b20af701ffb27332f80
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5982176037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d70484e9a3340b6f158df0bfb46df082eaff70c0443b954599df5cb22a8bccf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:35:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:35:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:35:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:35:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:38:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:39:34 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:27:58 GMT
ENV GOLANG_VERSION=1.15.12
# Thu, 06 May 2021 20:31:23 GMT
RUN $url = 'https://dl.google.com/go/go1.15.12.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '313e5ebc59b497319c4c3f9560322fcc20f7bc3b4e47494afc3b2d63a42fb2a5'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:31:25 GMT
WORKDIR C:\gopath
# Thu, 06 May 2021 21:00:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:00:56 GMT
ENV XCADDY_VERSION=v0.1.9
# Thu, 06 May 2021 21:00:57 GMT
ENV CADDY_VERSION=v2.3.0
# Thu, 06 May 2021 21:00:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 06 May 2021 21:02:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 06 May 2021 21:02:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3360763b706a564d93471b21a342ebbda7e047567cf1cbee82dd592ad33e0c`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0f653700ac9b57cf3d694cc90107e3220fc678581d1e985219677733ce242`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59d82702c225a2ca8cd2a5476122f55d8619eae959c9cb8323b68d70a2ed19`  
		Last Modified: Wed, 14 Apr 2021 12:59:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62435cd2b7652fc97ef3dc1a8968446f3f6e95f0ff1d6dcb176a3f0c2b14c2f8`  
		Last Modified: Wed, 14 Apr 2021 12:59:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d78a3a3d6cb25f55dc9d9947f7449a14717e6b787e49571a837e72b79334cf`  
		Last Modified: Wed, 14 Apr 2021 12:59:41 GMT  
		Size: 30.8 MB (30752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b774a32e346c00e004abbbd7290530d0a3f3dfb11915be2b2fa73c402da6bdd`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d153061f2f0d8ef33f71c4b9afd90899e21556e320d7103a8a9fb544c1cb521`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 5.6 MB (5608025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77293b9e38b389fb10ca47df8ebed52eaa8d0b9d8fe67701f41f353b87fff7dd`  
		Last Modified: Thu, 06 May 2021 20:39:59 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5820129044179dd743c12eb760d4dc1b649b453884dbbc676f43db154e398755`  
		Last Modified: Thu, 06 May 2021 20:40:32 GMT  
		Size: 143.9 MB (143920323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e148ea2e33c621c36032ed6f1fe0e45feb3394fcf0a1b5fc24918333d9da7222`  
		Last Modified: Thu, 06 May 2021 20:39:59 GMT  
		Size: 1.6 KB (1587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b609033068047241fcc0a4f67b4a06a1daa731a5ebb2835f75f12db601fe90`  
		Last Modified: Thu, 06 May 2021 21:05:39 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af22c6a21c6ad89bffef63695e5b396725b1d542e49b9082bb17e5c9d98d4d9`  
		Last Modified: Thu, 06 May 2021 21:05:36 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e3edba755c397ed87f591e2eac50e2d1f992934d53e25a88d20c1925ff0ba4`  
		Last Modified: Thu, 06 May 2021 21:05:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b4285d0784135391adbf8943455eeae65aad2fbcc56386c6629a749ccbbd5a`  
		Last Modified: Thu, 06 May 2021 21:05:36 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3c1e1ca4ddc1f2725e123cd6fd1452388065bf5639107cbdf74c756f0b7a90`  
		Last Modified: Thu, 06 May 2021 21:05:44 GMT  
		Size: 7.0 MB (6993022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f61c3066c0e78987570ac749619beed620b38bb2851df7ca1a195e1ea279040`  
		Last Modified: Thu, 06 May 2021 21:05:36 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0-windowsservercore`

```console
$ docker pull caddy@sha256:6a199f80cee0da0b39f4deffc53efac536c60672f4d8d26887f8f8ec194da3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.3.0-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:fdb259b96e8413c959258115e3cc0ed6272cd362b32dcee80b7c5875b3cca213
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487217133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db78127126d7dbe748dc638552655f6a86f11faa664f34ed256da804f77de223`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:04:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:04:04 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:04:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:04:45 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:04:46 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:04:47 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:04:48 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:04:49 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:04:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:04:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:04:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:04:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:04:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:04:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:04:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:04:58 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:05:00 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:05:01 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:05:27 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:05:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98036a79f108b7c08eb62f3ef539549a6fe005aced8f3fa4971a4e576e8c045`  
		Last Modified: Wed, 14 Apr 2021 20:24:07 GMT  
		Size: 5.1 MB (5081237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1c0c34e473966a69a26492fc168338b6ee1afadedd4cfd3b84537129685128`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88365dd5b6b4b0188ad00f31b1114067b79a05d3eeaecbcdf86385c18e1e2bff`  
		Last Modified: Wed, 14 Apr 2021 20:24:16 GMT  
		Size: 12.0 MB (12047588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8761bc4a54d10c3f03507406d03f0161fece0b4f80913bc67f5218cf7acc0e`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23987f8593afe96ed2b00e5744c51d5678851dac567bde07c230d882b31db5b`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27edd7d612a33644ef095d4bd52c800d8e8a1bd73a56ddbeba0a2cda230947a6`  
		Last Modified: Wed, 14 Apr 2021 20:24:02 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c5b86f636ca1020805b216bf4ea83e1aaa4e5da4145ec671280678483c8084`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f097631ca96d803dd63f72849f1b76728a05c89e8451675f669fc655ae07600`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ace7f5f948c892db540a9734d885fb0695faf8cc55e9fa2df27c4aff76e485d`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57476c73327d061921cee32adad6344e762c80c1142357a6de89819e8577d3e6`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaad63b2ff3aa00f636a1f988a02040c9832ae1a184093cef2471115a787a8f`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1aef5aebcec7bd144ab11a819f8406f07a0dcfaf11684f464b56f5835633fb4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd29f97bbc5cd627a79fc205fd6f63257d27e45e45264ec1e1c3ab94b319e4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aeafc40e34b5ef3464715c082ddb0910edbd9a59ac2d4d9d6586a0022271b4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3fa5d1767b62495151be377ed814c0ce5766f1cb875b724b922d378249bb8`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f7d63263e3b381a5386cd4b13b21226da398d0c8d2bf59f111efb466b9959`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab5798a12c9581184fa73f7b74913b0cf6c4ae638f2886f07d70a9f32181d9a`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf434bfce197fbac09ffe0409a20f2a1ba646801b7dac739c6cea7bed0ce2fad`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0defeab0b694a738dc4b945c883e44f4118a4127f00e4cea32ab589fb194dc`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 308.9 KB (308863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d70335c993ba29c3325465e90a310fce3b41a934bc25ec1bc5220fd3424bfe`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.3.0-windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:0a27a5dee7d386c823f3ad85b0ad3c7c6ebb739e7d7ad1cbc37662a3e955dfbc
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818160037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d01f580a5360a74b845ce6ffbd196e0930731b656954f6dafd810f4b69ae72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:07:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:07:15 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:09:01 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:09:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:09:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:09:05 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:09:06 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:09:07 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:09:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:09:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:09:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:09:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:09:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:09:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:09:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:09:16 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:09:17 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:09:18 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:29 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:10:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ea9969fcb8e31829ad2a30ccb77a30f56d17d992051bf6a04b0bd4ebb24a7`  
		Last Modified: Wed, 14 Apr 2021 20:24:45 GMT  
		Size: 5.7 MB (5661064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d2fcf25a0097bf75ef1b7b207a765b3c93bce2eb96e7ebf2ce894a0ca0bf1`  
		Last Modified: Wed, 14 Apr 2021 20:24:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1814c5a2050da8e869a225b62ac936693d7904fed473ed6d703acd42542916`  
		Last Modified: Wed, 14 Apr 2021 20:24:46 GMT  
		Size: 17.3 MB (17333583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93803b6c6c1e5befb69d029873c92020261e4faf5f97fa1ebe4474f2fcd761da`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bef042a1c15ba4cca6086f36ad82e03f037ebae2ec5218dc528ce8afa0cbbe7`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c22fd29bd95221222824495015750f062fcf337845032c4d11be1c8166d9911`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e034d998c8e3152093c8f2c30b0ac9122c528b8ba0889cadf3a3282059a8f96c`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cd579cdba6539c678c1cfd7184427e5b0777e34c965e8c6ca62f8301dd629f`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea0c59c3768ba8d3f4943669c834e3b8043899a0ee61ed325fa453559243f95`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5f4c914fc136d87d2e00167556104cf17827c516e84c53785225cfeb214a42`  
		Last Modified: Wed, 14 Apr 2021 20:24:40 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164712f851736c62b6da95357e6056173e390402e1a17b2f7559af8f42ce0134`  
		Last Modified: Wed, 14 Apr 2021 20:24:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d73f78d7b9ccdb5963233ef77dab1188e2678cc7c9136ff183494cd28f893f0`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b455a43ac6d0be6faf8dce0c59c609cc832963d9cc649b301f49ff79f218e439`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f00b0ac9199b716d513a33d44003af6cd00e4b9b7a2feab64b84649d80640`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ece2a763e6182c580aadb07399f77037c831dd03ee9cdad4f70b18759458094`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac88310e829bdb746ec804044c2a238dc2c6f64660688285a64205a255283c47`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed384ae90a546f9aad4b539596228057299114b9662407a708465a0ed7de3691`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de7a040e97ee693dc826cc6130e42fe7597fbf48fe035d0e5f9f039166edae5`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c1c4ddd499c8a111514a0d3bc3b97381c76a6b33d1cb3f74752d42ddc3e43c`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96251eba56a444a75ccc3480986386b2d2abcce41beadf2f267bedaee332c54a`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0-windowsservercore-1809`

```console
$ docker pull caddy@sha256:89f75ffc06d5f7a7cc6d37f38c9198d869993fa7426542d14c1a8bfdbb467694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `caddy:2.3.0-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:fdb259b96e8413c959258115e3cc0ed6272cd362b32dcee80b7c5875b3cca213
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487217133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db78127126d7dbe748dc638552655f6a86f11faa664f34ed256da804f77de223`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:04:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:04:04 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:04:43 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:04:45 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:04:46 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:04:47 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:04:48 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:04:49 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:04:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:04:51 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:04:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:04:54 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:04:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:04:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:04:57 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:04:58 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:05:00 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:05:01 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:05:27 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:05:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98036a79f108b7c08eb62f3ef539549a6fe005aced8f3fa4971a4e576e8c045`  
		Last Modified: Wed, 14 Apr 2021 20:24:07 GMT  
		Size: 5.1 MB (5081237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1c0c34e473966a69a26492fc168338b6ee1afadedd4cfd3b84537129685128`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88365dd5b6b4b0188ad00f31b1114067b79a05d3eeaecbcdf86385c18e1e2bff`  
		Last Modified: Wed, 14 Apr 2021 20:24:16 GMT  
		Size: 12.0 MB (12047588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8761bc4a54d10c3f03507406d03f0161fece0b4f80913bc67f5218cf7acc0e`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23987f8593afe96ed2b00e5744c51d5678851dac567bde07c230d882b31db5b`  
		Last Modified: Wed, 14 Apr 2021 20:24:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27edd7d612a33644ef095d4bd52c800d8e8a1bd73a56ddbeba0a2cda230947a6`  
		Last Modified: Wed, 14 Apr 2021 20:24:02 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c5b86f636ca1020805b216bf4ea83e1aaa4e5da4145ec671280678483c8084`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f097631ca96d803dd63f72849f1b76728a05c89e8451675f669fc655ae07600`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ace7f5f948c892db540a9734d885fb0695faf8cc55e9fa2df27c4aff76e485d`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57476c73327d061921cee32adad6344e762c80c1142357a6de89819e8577d3e6`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaad63b2ff3aa00f636a1f988a02040c9832ae1a184093cef2471115a787a8f`  
		Last Modified: Wed, 14 Apr 2021 20:24:00 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1aef5aebcec7bd144ab11a819f8406f07a0dcfaf11684f464b56f5835633fb4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd29f97bbc5cd627a79fc205fd6f63257d27e45e45264ec1e1c3ab94b319e4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aeafc40e34b5ef3464715c082ddb0910edbd9a59ac2d4d9d6586a0022271b4`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3fa5d1767b62495151be377ed814c0ce5766f1cb875b724b922d378249bb8`  
		Last Modified: Wed, 14 Apr 2021 20:23:58 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f7d63263e3b381a5386cd4b13b21226da398d0c8d2bf59f111efb466b9959`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab5798a12c9581184fa73f7b74913b0cf6c4ae638f2886f07d70a9f32181d9a`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf434bfce197fbac09ffe0409a20f2a1ba646801b7dac739c6cea7bed0ce2fad`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0defeab0b694a738dc4b945c883e44f4118a4127f00e4cea32ab589fb194dc`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 308.9 KB (308863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d70335c993ba29c3325465e90a310fce3b41a934bc25ec1bc5220fd3424bfe`  
		Last Modified: Wed, 14 Apr 2021 20:23:55 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.3.0-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:a42a67f914fd976a839e8c725f15fec79415b331ffeaa3972e7bff363bec4ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.3.0-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:0a27a5dee7d386c823f3ad85b0ad3c7c6ebb739e7d7ad1cbc37662a3e955dfbc
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818160037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d01f580a5360a74b845ce6ffbd196e0930731b656954f6dafd810f4b69ae72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 20:07:14 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Apr 2021 20:07:15 GMT
ENV CADDY_VERSION=v2.3.0
# Wed, 14 Apr 2021 20:09:01 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.3.0/caddy_2.3.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('afc504cb0a641729ba546c0cadea524a170dcca2a915473aaf032a7c666c7c56ac059752f34b5d50700a692647b9b395b530cd8299ac3650c729adce5daa1ba5')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Apr 2021 20:09:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Apr 2021 20:09:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Apr 2021 20:09:05 GMT
VOLUME [c:/config]
# Wed, 14 Apr 2021 20:09:06 GMT
VOLUME [c:/data]
# Wed, 14 Apr 2021 20:09:07 GMT
LABEL org.opencontainers.image.version=v2.3.0
# Wed, 14 Apr 2021 20:09:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Apr 2021 20:09:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Apr 2021 20:09:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Apr 2021 20:09:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Apr 2021 20:09:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Apr 2021 20:09:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Apr 2021 20:09:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Apr 2021 20:09:16 GMT
EXPOSE 80
# Wed, 14 Apr 2021 20:09:17 GMT
EXPOSE 443
# Wed, 14 Apr 2021 20:09:18 GMT
EXPOSE 2019
# Wed, 14 Apr 2021 20:10:29 GMT
RUN caddy version
# Wed, 14 Apr 2021 20:10:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ea9969fcb8e31829ad2a30ccb77a30f56d17d992051bf6a04b0bd4ebb24a7`  
		Last Modified: Wed, 14 Apr 2021 20:24:45 GMT  
		Size: 5.7 MB (5661064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d2fcf25a0097bf75ef1b7b207a765b3c93bce2eb96e7ebf2ce894a0ca0bf1`  
		Last Modified: Wed, 14 Apr 2021 20:24:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1814c5a2050da8e869a225b62ac936693d7904fed473ed6d703acd42542916`  
		Last Modified: Wed, 14 Apr 2021 20:24:46 GMT  
		Size: 17.3 MB (17333583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93803b6c6c1e5befb69d029873c92020261e4faf5f97fa1ebe4474f2fcd761da`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bef042a1c15ba4cca6086f36ad82e03f037ebae2ec5218dc528ce8afa0cbbe7`  
		Last Modified: Wed, 14 Apr 2021 20:24:39 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c22fd29bd95221222824495015750f062fcf337845032c4d11be1c8166d9911`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e034d998c8e3152093c8f2c30b0ac9122c528b8ba0889cadf3a3282059a8f96c`  
		Last Modified: Wed, 14 Apr 2021 20:24:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cd579cdba6539c678c1cfd7184427e5b0777e34c965e8c6ca62f8301dd629f`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea0c59c3768ba8d3f4943669c834e3b8043899a0ee61ed325fa453559243f95`  
		Last Modified: Wed, 14 Apr 2021 20:24:36 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5f4c914fc136d87d2e00167556104cf17827c516e84c53785225cfeb214a42`  
		Last Modified: Wed, 14 Apr 2021 20:24:40 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164712f851736c62b6da95357e6056173e390402e1a17b2f7559af8f42ce0134`  
		Last Modified: Wed, 14 Apr 2021 20:24:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d73f78d7b9ccdb5963233ef77dab1188e2678cc7c9136ff183494cd28f893f0`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b455a43ac6d0be6faf8dce0c59c609cc832963d9cc649b301f49ff79f218e439`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f00b0ac9199b716d513a33d44003af6cd00e4b9b7a2feab64b84649d80640`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ece2a763e6182c580aadb07399f77037c831dd03ee9cdad4f70b18759458094`  
		Last Modified: Wed, 14 Apr 2021 20:24:34 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac88310e829bdb746ec804044c2a238dc2c6f64660688285a64205a255283c47`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed384ae90a546f9aad4b539596228057299114b9662407a708465a0ed7de3691`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de7a040e97ee693dc826cc6130e42fe7597fbf48fe035d0e5f9f039166edae5`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c1c4ddd499c8a111514a0d3bc3b97381c76a6b33d1cb3f74752d42ddc3e43c`  
		Last Modified: Wed, 14 Apr 2021 20:24:32 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96251eba56a444a75ccc3480986386b2d2abcce41beadf2f267bedaee332c54a`  
		Last Modified: Wed, 14 Apr 2021 20:24:31 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.0`

```console
$ docker pull caddy@sha256:385a805019a00604cda677ecab3def2b1f0e99edf622e4bbd33a5d18cf8a55f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.4.0` - linux; amd64

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

### `caddy:2.4.0` - linux; arm variant v6

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

### `caddy:2.4.0` - linux; arm variant v7

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

### `caddy:2.4.0` - linux; arm64 variant v8

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

### `caddy:2.4.0` - linux; ppc64le

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

### `caddy:2.4.0` - linux; s390x

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

### `caddy:2.4.0` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:dee876a8acfe0ad66efe5790b51e5ce47ee105518205c16c1e515107022ee466
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487145585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab04d82b7c1bbab4a4556a4ab389e58cf942f64806603d16b32d02b85377ddc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:15:27 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:15:28 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:16:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:16:04 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:16:06 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:16:07 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:16:08 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:16:10 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:16:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:16:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:16:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:16:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:16:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:16:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:16:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:16:21 GMT
EXPOSE 80
# Tue, 11 May 2021 00:16:22 GMT
EXPOSE 443
# Tue, 11 May 2021 00:16:24 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:16:51 GMT
RUN caddy version
# Tue, 11 May 2021 00:16:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a805066d9e28c5afaf71144648d2270f86d9d1dfbaa0da9a239607694e9315b6`  
		Last Modified: Tue, 11 May 2021 00:26:29 GMT  
		Size: 5.1 MB (5104734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbd0ec6de6085e7571da80b4408f11fada63d710eaf20b44c1ce63847f6455c`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1c04d9585e13e14d3ba056c3a17a8a23821f402c55d603f719fde9885fcc74`  
		Last Modified: Tue, 11 May 2021 00:26:31 GMT  
		Size: 11.9 MB (11930099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27b6dfe0db5cd7aad46afe881c42348361a2c19752cf5629eacb67967b8520`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41902606f9afaae6014164471bda32934d7f0304b3aaa65e2d7480497d85b0bc`  
		Last Modified: Tue, 11 May 2021 00:26:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9ff94e742183a75d4199b58723e286d55ecdd255b03a81ad9ec2b222c85fe1`  
		Last Modified: Tue, 11 May 2021 00:26:25 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1edf08b568698061ffae34580ddf83acab5de417993a30b8a209c919461e6a`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2873cb5c59a087bae99202d1b5f8e424378796848bf9f9f0576cb9e75da8011`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11858529cacdcdc2b7ff911a5df669b21b0efaa8c2fcbde324ccaf0a4a2d4d6`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b96fffb3765e29e3c670d5e14eb09f96a25c0222143cfac7d62c9fa6224896`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b40f5b20f6588f423dc4ba00206ef0b74da9619e96c8c26af206ea104cf85`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9116ab8bdbdeb3f51018f29b3c57d96ed1ebdff8866b0a503c7cb682741e5d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec28519386c9082afe64bc68c2e073b32a2287131bba90c6f56cc9315a638b04`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7649cdb04974c2bf32fa747aadcf57f6402a9c418e9e8f78ada74eae7aec3029`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9652bcbd02b47c702e6f2e8c374f7304cb91ba0186aede9c423104440004857d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33145d7abff94087dd683fd05403939e5aa91276d2693f6c5e8ca28641acd8e1`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a096c1bcb735f9b2cd6bf77eb582dd89b09a6cc75199dd35d65bd5cf6ad50e`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dde82b55b25477fe6eb7381cfdb3e48aa439cbd3f6352e033a85d124cecae7a`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67426815598f918caebff919df817435078c051338bebd944aafb6b25ef593f6`  
		Last Modified: Tue, 11 May 2021 00:26:20 GMT  
		Size: 331.3 KB (331282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf87ebb9031675a0e4407a36e79f274666df2a06d20c2452c1e0acec70fc60a6`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:b61efb630c29dfd10f857eed823207497fd9c94176f47243f48c641119c663d3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818059080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3940d8ab2b2d69a458bd9951c005b3703a5ac35754896cbfd380305f8dfe27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:18:49 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:18:50 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:20:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:20:40 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:20:42 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:20:43 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:20:45 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:20:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:20:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:20:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:20:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:20:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:20:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:20:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:20:56 GMT
EXPOSE 80
# Tue, 11 May 2021 00:20:58 GMT
EXPOSE 443
# Tue, 11 May 2021 00:20:59 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:22:14 GMT
RUN caddy version
# Tue, 11 May 2021 00:22:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc088e7513f9bd5e2261035715cd5f39aff459f086737be39631a5c03dd0bc9`  
		Last Modified: Tue, 11 May 2021 00:27:00 GMT  
		Size: 5.7 MB (5678806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a94477e69ebd7355bfc6230d3309aa20d4fda7d504dc34bd3b2adae7f5f2b4`  
		Last Modified: Tue, 11 May 2021 00:26:57 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db416be1d5a7c97652523c359440855c0ef2127ac11cb08595aa068d99d8a5`  
		Last Modified: Tue, 11 May 2021 00:27:03 GMT  
		Size: 17.2 MB (17201492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e500af558c7988b44d7fae2a1a8c1d4498cb130d1de721a37712c33f09147a`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87b8476ce7fba27f66c08050c4a692f8a19ec0c84e9d42537b4b4b8bbb5f56e`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2d6240d48682965790d983fc3f6b5404aeb7f3f023b517ab83b6e47c20af5c`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757d21ff239a36a372b7fb98d22d42afd8f3c779c7b342605186d6b2a14925e7`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5e64a8fa017a3b5df9f60508bc7b3f72fe2835f00c086648f26235c9358b14`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac63d4edb89dc9920755d7e04e444610a75ac1268b103c178ebff146f490d73`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fbb5cca77bbd06aabe9371bf1fe894938b82367a0ef11be873b231a43b64ab`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b0ecb05ae3d1fffc947acf96dea7fe481fd9a745d4fcf79bff9f4b21a28817`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f292068b665f33bccf70f8100aa252145e0f63abb2283fa29d36cadcc6291c52`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1995472761eea00392fa2ce2d1566a7233a89a019e939892cbb0aeb4a8a3a07a`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e8f37215e61d4f10f002f5ad82c4acadf4a56b559cf036050f33242bfe1e35`  
		Last Modified: Tue, 11 May 2021 00:26:49 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2f6fb7cf636418bada10647c66ee3b92246da967ebb611d58aad6725f5e2b`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271eda8ea06432cb0dae8fd93e8a85314e86201450cdbebf3efcbba2dbd4331`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a4da75f19907c0ee148b5369a63863a2752457cc31b02fe68779d83d56c1`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7013990e537c69857c80a4d6fb386f6d0f04e5a0a5ee5b12ed57c0e458fc8e`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b661b1f2a589a6717a5599a78cb0f3ef950c1a36bd411039dfd39afb20e901b`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 269.3 KB (269349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e686f1164cdcf35434a7d997c0c9ff058302aaade06ace7c5f8a2e4a718aa`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.0-alpine`

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

### `caddy:2.4.0-alpine` - linux; amd64

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

### `caddy:2.4.0-alpine` - linux; arm variant v6

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

### `caddy:2.4.0-alpine` - linux; arm variant v7

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

### `caddy:2.4.0-alpine` - linux; arm64 variant v8

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

### `caddy:2.4.0-alpine` - linux; ppc64le

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

### `caddy:2.4.0-alpine` - linux; s390x

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

## `caddy:2.4.0-builder`

```console
$ docker pull caddy@sha256:425b1075398c4ebde59024ee2847746c5b54171ee16096bb85d4a99aa6de8398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.4.0-builder` - linux; amd64

```console
$ docker pull caddy@sha256:046f9aa5dcf83fb25e28e43539c520c8cd0dfe05faf14ad780826c7c36775145
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116541075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd288b16c2ac5e35de34025c916a8a52cb8c3c35644e3e2beee860100beea6de`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:27:12 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:27:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:27:13 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:18:07 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:20:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:20:05 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:20:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:20:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:20:07 GMT
WORKDIR /go
# Fri, 07 May 2021 01:56:14 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:56:14 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 01:04:35 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:04:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 01:04:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 11 May 2021 01:04:38 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 11 May 2021 01:04:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc1eea9eeabb6de296adb3e0c1b0722cf13251ff3e4e2d0a5f7ed8e3d48342`  
		Last Modified: Wed, 14 Apr 2021 21:35:06 GMT  
		Size: 281.3 KB (281269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4ab2625f07be8d5c6e48046a05ff3ecc7f374b794a926fb62247b66b511909`  
		Last Modified: Wed, 14 Apr 2021 21:35:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e7595549f7536d76f08a8a23fb67e3e6fae08ccf3add715c5c1c956f9445d2`  
		Last Modified: Thu, 06 May 2021 23:29:42 GMT  
		Size: 105.7 MB (105745828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df88182f7acff97ffde9f614a0fd86e8a26590e445aa76e442c3a79d9e4c4f4`  
		Last Modified: Thu, 06 May 2021 23:29:25 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d573d19fd03835237c7687f4f394fa6b1fc1c894a901f2853846256ee7746eb`  
		Last Modified: Fri, 07 May 2021 01:56:57 GMT  
		Size: 6.4 MB (6390123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95db25f5b69783a08df8902a5330daddf1e8b10bd1d8401b25d8f8ab43b6586f`  
		Last Modified: Tue, 11 May 2021 01:05:15 GMT  
		Size: 1.3 MB (1311169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bfbae6287f60c1e9b89dd3e92e73d9f949ee6f11d78bc97a3e945ee20b2c68`  
		Last Modified: Tue, 11 May 2021 01:05:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:124237c870217e836b67b4697d7cddad2c3c58d50878dc51654db3605712c336
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112278566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bef88e43f4622abd673fe82f110eb193559dd1abb2d8550178eb66032b4b5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:00:55 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:01:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:01:02 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:24:09 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 21:27:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 21:27:32 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 21:27:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:27:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 21:27:35 GMT
WORKDIR /go
# Thu, 06 May 2021 22:10:19 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 06 May 2021 22:10:20 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:51:04 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:51:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:51:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:51:14 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:51:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4dea9fd179326b36ea137aad07e06571ffe7ad849e2a13a32354dcfd5d858d`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 281.4 KB (281379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abeb04d84d23abf8470fc95982483a9117a87e55b13c591f5332a460a5233bb`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a3721aaa7ffedbec829a557c2d5f99c4661695a51f82632ece4df509b71bc1`  
		Last Modified: Thu, 06 May 2021 21:38:30 GMT  
		Size: 101.9 MB (101925593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298c78bc6b40a671a2f9a64d2cecf253acd10da30924ff687012e02b0307a1a8`  
		Last Modified: Thu, 06 May 2021 21:37:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3d237d41fc2805c9d9a047d4bb2618233c7093cc31d682b5231e0261a8c201`  
		Last Modified: Thu, 06 May 2021 22:11:03 GMT  
		Size: 6.2 MB (6227066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ffbb7f2dd65c638ffd56b2ab5964193545041922501d15451a2b6f4b0b0edb`  
		Last Modified: Mon, 10 May 2021 23:51:50 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d30db79a4a633e8984befac9884a645ed6f3bd581f677daa8a26f2cbda65a4`  
		Last Modified: Mon, 10 May 2021 23:51:50 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:a4ecc2040cdcc0166a3fea577c4e704d291fe70c2c65c460ff347d06c2b54046
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111227459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d2c6dfa3a578099a3e909c80cd793b780fb7a9135d5f28ec25270157a0902f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:00:38 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:01:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:01:41 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:11:51 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:15:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:15:25 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:15:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:15:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:15:29 GMT
WORKDIR /go
# Fri, 07 May 2021 02:34:14 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:34:14 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 01:17:54 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:18:06 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 01:18:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 11 May 2021 01:18:32 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 11 May 2021 01:18:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6bd423db0b63fdc83c72eae7ef401cb2fb9eaa63961c71a867ff26bfe422f`  
		Last Modified: Wed, 14 Apr 2021 22:44:20 GMT  
		Size: 280.5 KB (280532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835b667ae68ff940439602ffbabae6e923c687cb56c62a793f23ddca67584049`  
		Last Modified: Wed, 14 Apr 2021 22:44:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5b93a32354ff48887c2e9c4540875b8aa57822ab5c261d95e3c186d27b5c5e`  
		Last Modified: Thu, 06 May 2021 23:28:23 GMT  
		Size: 101.7 MB (101743890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2925b4cee8520caf8150ba3410d1306c50fa326f2fd920488f9e432578fda5`  
		Last Modified: Thu, 06 May 2021 23:27:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc435726a63967cbbe522309fca3524e0e1fd01e955717cedc9e172d632cbd1`  
		Last Modified: Fri, 07 May 2021 02:34:54 GMT  
		Size: 5.6 MB (5558665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd402931cf263713336d2aa524723f4caec26b90c0d6406651b14a2f88a642ab`  
		Last Modified: Tue, 11 May 2021 01:19:24 GMT  
		Size: 1.2 MB (1219508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee3295bff1b446bc98e483336ce527bcd52ccfecd1930eba95c70c26e909f3a`  
		Last Modified: Tue, 11 May 2021 01:19:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:a8418ff913feb35632b8e2e0e2dde138632b289047de19713b0c24fe65c6eecc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111763060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68622e818b4c271dd7faf093081a9641f809d407eb6dc67bb6afe822393b4b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:40:18 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:40:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:40:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:31:41 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 22:33:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 22:33:53 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 22:33:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:33:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 22:33:57 GMT
WORKDIR /go
# Fri, 07 May 2021 01:17:18 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:17:19 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:40:20 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:40:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:40:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:40:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:40:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7186ed65a4f7bb0e9cd4b00f43359b47a4f19749dbd48e704fc578a4f43d7c96`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 281.5 KB (281488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316046926c0ae5f42710c1197ed3de9fc374986179c18611f523cf4521adeef1`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a969ea94b7c2e3938ec670b72c32f58ece636bb7ec6526d0efab40e760bce`  
		Last Modified: Thu, 06 May 2021 22:44:20 GMT  
		Size: 101.1 MB (101090590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff4d3f41a5567d10cda7e4f3c4267dbb9181eb63bb52c950c3dce3327a9a36e`  
		Last Modified: Thu, 06 May 2021 22:43:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ec12dccc6ac2c5238a0e958e58c89d37f56cf2e181ba8a4f291b176a2a20fa`  
		Last Modified: Fri, 07 May 2021 01:18:00 GMT  
		Size: 6.5 MB (6476691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803dba8659a2ec5c5a177383797832eca7c7d301ec4253e47ee42527aa617bac`  
		Last Modified: Mon, 10 May 2021 23:40:59 GMT  
		Size: 1.2 MB (1201547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e70f326991067a04529de021321ce20d6920e81d14aaef93afb92136c976508`  
		Last Modified: Mon, 10 May 2021 23:40:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:58ffe092c4ccbd15cf9faf25d63caa632bb639d53188a377038834ebf2dac85a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110621059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2321e3937c686734c8c9124a34811d9eb4092b7611145be19ea453a5bbb389a4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:53:57 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 22:54:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:54:14 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:22:47 GMT
ENV GOLANG_VERSION=1.16.4
# Fri, 07 May 2021 00:25:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 07 May 2021 00:25:26 GMT
ENV GOPATH=/go
# Fri, 07 May 2021 00:25:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:25:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 07 May 2021 00:26:14 GMT
WORKDIR /go
# Fri, 07 May 2021 08:19:51 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 08:19:57 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 01:19:13 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:19:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 01:19:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 11 May 2021 01:19:30 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 11 May 2021 01:19:37 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf726c40dc4802009a4b6f0f7947c86242c2c078623e8f1f21343864093b3a9`  
		Last Modified: Wed, 14 Apr 2021 23:05:31 GMT  
		Size: 283.4 KB (283413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c17712dac96942b05a27f88ea5346bd57b4cabdb33c153562ef144635225b3`  
		Last Modified: Wed, 14 Apr 2021 23:05:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d2e93731067b7b48232c826d062ff4fead572dbd98e0a28642db4802342a8e`  
		Last Modified: Fri, 07 May 2021 00:41:39 GMT  
		Size: 99.5 MB (99528032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca0e521f95ca5f22fdd4b7917d06aead7df46288885c4fd3ffac0242b96643f`  
		Last Modified: Fri, 07 May 2021 00:41:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9dfa7e81a349fea3e170fbc6f6b9fd3245ee43c53b329a3ae72c9e5ebaddfb`  
		Last Modified: Fri, 07 May 2021 08:22:18 GMT  
		Size: 6.8 MB (6825232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f3bfd07b70b357098f4ba50744bf3c838e8c3ab709598b79864f29b676311`  
		Last Modified: Tue, 11 May 2021 01:20:23 GMT  
		Size: 1.2 MB (1170526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68dce6545308f135393f568603954610d88f7a8a61ca402820d75500d925926c`  
		Last Modified: Tue, 11 May 2021 01:20:23 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-builder` - linux; s390x

```console
$ docker pull caddy@sha256:e72252e76203d04b2ed847e26d71ca0de7ed89c2d76990ac177fb80755d88617
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115474412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08b1e73df9c564bfdb9249c0d32c47642dd69cd88bfa280b4682767ef8fe671`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:45:11 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:45:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:45:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:16:38 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:20:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:20:18 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:20:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:20:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:20:21 GMT
WORKDIR /go
# Fri, 07 May 2021 02:02:34 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:02:35 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:42:03 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:42:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:42:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:42:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:42:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc746875ae346ee6ec3c9080f8a7a50bef3899ea9d5ae9dac45a81bfe861c9d`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 281.7 KB (281708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0242688236000dd8f33d16f89f36da3ef1bb2a7a32bb59a7eb97a18ed3d5158`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37dab17b6808078a43afd3d62f1a202857192406e914c33d5ceb5eec1eb05eeb`  
		Last Modified: Thu, 06 May 2021 23:34:08 GMT  
		Size: 104.8 MB (104849388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6059cb089a1bd1108012ddff056f297d814995f95d29d57b15c13d11baede00d`  
		Last Modified: Thu, 06 May 2021 23:33:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84919c1c43955cfb518f179d4f6b541cdfa94579f6f6ef10fdc6e6b3ca4d51a3`  
		Last Modified: Fri, 07 May 2021 02:03:18 GMT  
		Size: 6.5 MB (6475416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3025f5e46ec68c9ef05a49a22ca89718a0d154f401122b0505a18d1c9217fc`  
		Last Modified: Mon, 10 May 2021 23:42:38 GMT  
		Size: 1.3 MB (1264531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bb5d9c7e67f1492e82b3f7c19e6900095d43b1f65fa5496f752a95169cd953`  
		Last Modified: Mon, 10 May 2021 23:42:38 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-builder` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:bc783b828c95b331d7fad4be39c04af02ab0b76ff396546a2d118771441f398e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2641373061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed813a8f2c9cd1366b5455eb1fd1c585aa4ab0f42e380f58cb6a58f23c27eead`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:30:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:30:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:30:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:30:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:31:57 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:32:38 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:16:07 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 20:18:44 GMT
RUN $url = 'https://dl.google.com/go/go1.16.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'd40139b7ade8a3008e3240a6f86fe8f899a9c465c917e11dac8758af216f5eb0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:18:46 GMT
WORKDIR C:\gopath
# Thu, 06 May 2021 21:02:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:02:30 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 00:22:36 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:22:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 00:23:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 May 2021 00:23:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac56922ba0ee0ac19bcae98f5fb4b7427d31ef3c709f27cfb2c785fd13a611c4`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1723430d5101a2d617d3dbf4bc2a121b3f4b4432105aa2941e1afab8f130b9`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f4dc6e9a77d69a3d172368f4ae471b31c588d6201c2386e4ac62fd83faa16`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea47861a9221a4f1e5750db237c619796c612756a5e75e2cb443b1731ae8a8`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4be4ebd8eabefdb01f27dafad85e65289b95ca15591c14304c7792db99b54b`  
		Last Modified: Wed, 14 Apr 2021 12:58:35 GMT  
		Size: 30.2 MB (30155601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f66ae3738a83ea41b428b49261d4522d57df1617fbd1aa362d93f1e2802643`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2108b314c24064a0c250f72017cc64b3bf68915655327728a267c98985a5ff7`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 324.6 KB (324649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa51985154dd0edd95ef4cc022400dc16b657c4a75cb3ade3675c58d316d0101`  
		Last Modified: Thu, 06 May 2021 20:34:43 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26942e7cec550ceca0e7b0ef319dc3f732731719adfc676869678adce06d1193`  
		Last Modified: Thu, 06 May 2021 20:35:15 GMT  
		Size: 139.4 MB (139382398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e6b3adacda0d1c5092f48a23fa73f5bb807876cf3dcf7fd71632b48d8b1987`  
		Last Modified: Thu, 06 May 2021 20:34:43 GMT  
		Size: 1.6 KB (1598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6d89568ee8ac19213ae2e66b14601f80c6dd3c4a1205da5fa55da7003cd3a0`  
		Last Modified: Thu, 06 May 2021 21:06:02 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0aa20834bcdb38f731b9f6528281005b29ae951a02ef46190bf1be1cab5946`  
		Last Modified: Thu, 06 May 2021 21:06:00 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada218f8f73674eea11444ee4fa8048f2cfd6e2bfc8f8c2bb4cc40954436b6b0`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815ac3cbadfa3d6463be2a02130f663d74e486df33a07b582def59fe66dd48b0`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da0a5d30891cb84455c6b13f7a6b778a19b3a271813ef7066eb0ba908192ee7`  
		Last Modified: Tue, 11 May 2021 00:27:20 GMT  
		Size: 1.7 MB (1738012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e2cb2540135f046b5adb4957a0f75118aeb15e30d46af750522a16e6f0cc2`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-builder` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:1b2ba73c8dc7fce225f65c457524b3830589cf0fa3e9c62faa0c88b15c73c74f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5987368241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd19fd51f0fc365a83899a16ab9d8fb86585a512ff6cc33bd07e7af1bc5d89d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:35:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:35:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:35:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:35:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:38:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:39:34 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:19:05 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 20:22:32 GMT
RUN $url = 'https://dl.google.com/go/go1.16.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'd40139b7ade8a3008e3240a6f86fe8f899a9c465c917e11dac8758af216f5eb0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:22:34 GMT
WORKDIR C:\gopath
# Thu, 06 May 2021 21:03:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:03:07 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 00:23:23 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:23:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 00:25:06 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 May 2021 00:25:08 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3360763b706a564d93471b21a342ebbda7e047567cf1cbee82dd592ad33e0c`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0f653700ac9b57cf3d694cc90107e3220fc678581d1e985219677733ce242`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59d82702c225a2ca8cd2a5476122f55d8619eae959c9cb8323b68d70a2ed19`  
		Last Modified: Wed, 14 Apr 2021 12:59:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62435cd2b7652fc97ef3dc1a8968446f3f6e95f0ff1d6dcb176a3f0c2b14c2f8`  
		Last Modified: Wed, 14 Apr 2021 12:59:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d78a3a3d6cb25f55dc9d9947f7449a14717e6b787e49571a837e72b79334cf`  
		Last Modified: Wed, 14 Apr 2021 12:59:41 GMT  
		Size: 30.8 MB (30752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b774a32e346c00e004abbbd7290530d0a3f3dfb11915be2b2fa73c402da6bdd`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d153061f2f0d8ef33f71c4b9afd90899e21556e320d7103a8a9fb544c1cb521`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 5.6 MB (5608025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c85bf3447935a123c186c94d58b02a7e89b566366ab0c7a20b57fbc9e453e1`  
		Last Modified: Thu, 06 May 2021 20:35:33 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7558c3fc6da1f41d9317a885b7d1d896986e9e4a81b6487a543b93ca372649cd`  
		Last Modified: Thu, 06 May 2021 20:36:08 GMT  
		Size: 149.1 MB (149112181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d97cea35310e2e19e356bf67efe44136adb4df53f744e6497511765af70f7e`  
		Last Modified: Thu, 06 May 2021 20:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5214a4bbf455290910bf5850bebdd3fdde0c4bf2616c2975a8a91b62cfe7a`  
		Last Modified: Thu, 06 May 2021 21:06:13 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f9311ef107812e0fc28e80ff17843a7d95e33d9b4311d0ff921022f5d199c3`  
		Last Modified: Thu, 06 May 2021 21:06:10 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b921e314d8bdd24486247a7d82137f437b1572bec858ea76813dc27e580670`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8450625dd9bbf2232b7a3d1cbce4d8795d03b140b1fb962bb6042b82a073633`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394074991c1e1b9a6750cf551fb9f7fe9eaffa1a25889bebcf0f35682cb69afe`  
		Last Modified: Tue, 11 May 2021 00:27:37 GMT  
		Size: 7.0 MB (6993409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5f2fa898b0d7f2684b17b889c9c68aa767c0a1f408e2e4eceb3374cdf48393`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.0-builder-alpine`

```console
$ docker pull caddy@sha256:8b8beeef5c72efc27da7a1cdf0a8f816303907f9733c13386d25ebc6e7f785b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.4.0-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:046f9aa5dcf83fb25e28e43539c520c8cd0dfe05faf14ad780826c7c36775145
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116541075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd288b16c2ac5e35de34025c916a8a52cb8c3c35644e3e2beee860100beea6de`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:27:12 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:27:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:27:13 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:18:07 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:20:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:20:05 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:20:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:20:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:20:07 GMT
WORKDIR /go
# Fri, 07 May 2021 01:56:14 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:56:14 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 01:04:35 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:04:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 01:04:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 11 May 2021 01:04:38 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 11 May 2021 01:04:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc1eea9eeabb6de296adb3e0c1b0722cf13251ff3e4e2d0a5f7ed8e3d48342`  
		Last Modified: Wed, 14 Apr 2021 21:35:06 GMT  
		Size: 281.3 KB (281269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4ab2625f07be8d5c6e48046a05ff3ecc7f374b794a926fb62247b66b511909`  
		Last Modified: Wed, 14 Apr 2021 21:35:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e7595549f7536d76f08a8a23fb67e3e6fae08ccf3add715c5c1c956f9445d2`  
		Last Modified: Thu, 06 May 2021 23:29:42 GMT  
		Size: 105.7 MB (105745828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df88182f7acff97ffde9f614a0fd86e8a26590e445aa76e442c3a79d9e4c4f4`  
		Last Modified: Thu, 06 May 2021 23:29:25 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d573d19fd03835237c7687f4f394fa6b1fc1c894a901f2853846256ee7746eb`  
		Last Modified: Fri, 07 May 2021 01:56:57 GMT  
		Size: 6.4 MB (6390123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95db25f5b69783a08df8902a5330daddf1e8b10bd1d8401b25d8f8ab43b6586f`  
		Last Modified: Tue, 11 May 2021 01:05:15 GMT  
		Size: 1.3 MB (1311169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bfbae6287f60c1e9b89dd3e92e73d9f949ee6f11d78bc97a3e945ee20b2c68`  
		Last Modified: Tue, 11 May 2021 01:05:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:124237c870217e836b67b4697d7cddad2c3c58d50878dc51654db3605712c336
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112278566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bef88e43f4622abd673fe82f110eb193559dd1abb2d8550178eb66032b4b5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:00:55 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:01:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:01:02 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:24:09 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 21:27:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 21:27:32 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 21:27:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:27:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 21:27:35 GMT
WORKDIR /go
# Thu, 06 May 2021 22:10:19 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 06 May 2021 22:10:20 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:51:04 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:51:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:51:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:51:14 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:51:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4dea9fd179326b36ea137aad07e06571ffe7ad849e2a13a32354dcfd5d858d`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 281.4 KB (281379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abeb04d84d23abf8470fc95982483a9117a87e55b13c591f5332a460a5233bb`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a3721aaa7ffedbec829a557c2d5f99c4661695a51f82632ece4df509b71bc1`  
		Last Modified: Thu, 06 May 2021 21:38:30 GMT  
		Size: 101.9 MB (101925593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298c78bc6b40a671a2f9a64d2cecf253acd10da30924ff687012e02b0307a1a8`  
		Last Modified: Thu, 06 May 2021 21:37:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3d237d41fc2805c9d9a047d4bb2618233c7093cc31d682b5231e0261a8c201`  
		Last Modified: Thu, 06 May 2021 22:11:03 GMT  
		Size: 6.2 MB (6227066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ffbb7f2dd65c638ffd56b2ab5964193545041922501d15451a2b6f4b0b0edb`  
		Last Modified: Mon, 10 May 2021 23:51:50 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d30db79a4a633e8984befac9884a645ed6f3bd581f677daa8a26f2cbda65a4`  
		Last Modified: Mon, 10 May 2021 23:51:50 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:a4ecc2040cdcc0166a3fea577c4e704d291fe70c2c65c460ff347d06c2b54046
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111227459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d2c6dfa3a578099a3e909c80cd793b780fb7a9135d5f28ec25270157a0902f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:00:38 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:01:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:01:41 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:11:51 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:15:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:15:25 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:15:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:15:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:15:29 GMT
WORKDIR /go
# Fri, 07 May 2021 02:34:14 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:34:14 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 01:17:54 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:18:06 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 01:18:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 11 May 2021 01:18:32 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 11 May 2021 01:18:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6bd423db0b63fdc83c72eae7ef401cb2fb9eaa63961c71a867ff26bfe422f`  
		Last Modified: Wed, 14 Apr 2021 22:44:20 GMT  
		Size: 280.5 KB (280532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835b667ae68ff940439602ffbabae6e923c687cb56c62a793f23ddca67584049`  
		Last Modified: Wed, 14 Apr 2021 22:44:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5b93a32354ff48887c2e9c4540875b8aa57822ab5c261d95e3c186d27b5c5e`  
		Last Modified: Thu, 06 May 2021 23:28:23 GMT  
		Size: 101.7 MB (101743890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2925b4cee8520caf8150ba3410d1306c50fa326f2fd920488f9e432578fda5`  
		Last Modified: Thu, 06 May 2021 23:27:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc435726a63967cbbe522309fca3524e0e1fd01e955717cedc9e172d632cbd1`  
		Last Modified: Fri, 07 May 2021 02:34:54 GMT  
		Size: 5.6 MB (5558665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd402931cf263713336d2aa524723f4caec26b90c0d6406651b14a2f88a642ab`  
		Last Modified: Tue, 11 May 2021 01:19:24 GMT  
		Size: 1.2 MB (1219508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee3295bff1b446bc98e483336ce527bcd52ccfecd1930eba95c70c26e909f3a`  
		Last Modified: Tue, 11 May 2021 01:19:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:a8418ff913feb35632b8e2e0e2dde138632b289047de19713b0c24fe65c6eecc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111763060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68622e818b4c271dd7faf093081a9641f809d407eb6dc67bb6afe822393b4b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:40:18 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:40:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:40:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:31:41 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 22:33:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 22:33:53 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 22:33:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:33:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 22:33:57 GMT
WORKDIR /go
# Fri, 07 May 2021 01:17:18 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:17:19 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:40:20 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:40:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:40:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:40:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:40:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7186ed65a4f7bb0e9cd4b00f43359b47a4f19749dbd48e704fc578a4f43d7c96`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 281.5 KB (281488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316046926c0ae5f42710c1197ed3de9fc374986179c18611f523cf4521adeef1`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a969ea94b7c2e3938ec670b72c32f58ece636bb7ec6526d0efab40e760bce`  
		Last Modified: Thu, 06 May 2021 22:44:20 GMT  
		Size: 101.1 MB (101090590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff4d3f41a5567d10cda7e4f3c4267dbb9181eb63bb52c950c3dce3327a9a36e`  
		Last Modified: Thu, 06 May 2021 22:43:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ec12dccc6ac2c5238a0e958e58c89d37f56cf2e181ba8a4f291b176a2a20fa`  
		Last Modified: Fri, 07 May 2021 01:18:00 GMT  
		Size: 6.5 MB (6476691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803dba8659a2ec5c5a177383797832eca7c7d301ec4253e47ee42527aa617bac`  
		Last Modified: Mon, 10 May 2021 23:40:59 GMT  
		Size: 1.2 MB (1201547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e70f326991067a04529de021321ce20d6920e81d14aaef93afb92136c976508`  
		Last Modified: Mon, 10 May 2021 23:40:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:58ffe092c4ccbd15cf9faf25d63caa632bb639d53188a377038834ebf2dac85a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110621059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2321e3937c686734c8c9124a34811d9eb4092b7611145be19ea453a5bbb389a4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:53:57 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 22:54:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:54:14 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:22:47 GMT
ENV GOLANG_VERSION=1.16.4
# Fri, 07 May 2021 00:25:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 07 May 2021 00:25:26 GMT
ENV GOPATH=/go
# Fri, 07 May 2021 00:25:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:25:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 07 May 2021 00:26:14 GMT
WORKDIR /go
# Fri, 07 May 2021 08:19:51 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 08:19:57 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 01:19:13 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:19:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 01:19:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 11 May 2021 01:19:30 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 11 May 2021 01:19:37 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf726c40dc4802009a4b6f0f7947c86242c2c078623e8f1f21343864093b3a9`  
		Last Modified: Wed, 14 Apr 2021 23:05:31 GMT  
		Size: 283.4 KB (283413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c17712dac96942b05a27f88ea5346bd57b4cabdb33c153562ef144635225b3`  
		Last Modified: Wed, 14 Apr 2021 23:05:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d2e93731067b7b48232c826d062ff4fead572dbd98e0a28642db4802342a8e`  
		Last Modified: Fri, 07 May 2021 00:41:39 GMT  
		Size: 99.5 MB (99528032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca0e521f95ca5f22fdd4b7917d06aead7df46288885c4fd3ffac0242b96643f`  
		Last Modified: Fri, 07 May 2021 00:41:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9dfa7e81a349fea3e170fbc6f6b9fd3245ee43c53b329a3ae72c9e5ebaddfb`  
		Last Modified: Fri, 07 May 2021 08:22:18 GMT  
		Size: 6.8 MB (6825232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f3bfd07b70b357098f4ba50744bf3c838e8c3ab709598b79864f29b676311`  
		Last Modified: Tue, 11 May 2021 01:20:23 GMT  
		Size: 1.2 MB (1170526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68dce6545308f135393f568603954610d88f7a8a61ca402820d75500d925926c`  
		Last Modified: Tue, 11 May 2021 01:20:23 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:e72252e76203d04b2ed847e26d71ca0de7ed89c2d76990ac177fb80755d88617
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115474412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08b1e73df9c564bfdb9249c0d32c47642dd69cd88bfa280b4682767ef8fe671`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:45:11 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:45:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:45:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:16:38 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:20:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:20:18 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:20:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:20:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:20:21 GMT
WORKDIR /go
# Fri, 07 May 2021 02:02:34 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:02:35 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:42:03 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:42:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:42:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:42:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:42:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc746875ae346ee6ec3c9080f8a7a50bef3899ea9d5ae9dac45a81bfe861c9d`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 281.7 KB (281708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0242688236000dd8f33d16f89f36da3ef1bb2a7a32bb59a7eb97a18ed3d5158`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37dab17b6808078a43afd3d62f1a202857192406e914c33d5ceb5eec1eb05eeb`  
		Last Modified: Thu, 06 May 2021 23:34:08 GMT  
		Size: 104.8 MB (104849388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6059cb089a1bd1108012ddff056f297d814995f95d29d57b15c13d11baede00d`  
		Last Modified: Thu, 06 May 2021 23:33:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84919c1c43955cfb518f179d4f6b541cdfa94579f6f6ef10fdc6e6b3ca4d51a3`  
		Last Modified: Fri, 07 May 2021 02:03:18 GMT  
		Size: 6.5 MB (6475416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3025f5e46ec68c9ef05a49a22ca89718a0d154f401122b0505a18d1c9217fc`  
		Last Modified: Mon, 10 May 2021 23:42:38 GMT  
		Size: 1.3 MB (1264531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bb5d9c7e67f1492e82b3f7c19e6900095d43b1f65fa5496f752a95169cd953`  
		Last Modified: Mon, 10 May 2021 23:42:38 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.0-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:a6cb45df3913c41d877ad5dea68ac399f038d58e244fc5f2637971201ece8f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `caddy:2.4.0-builder-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:bc783b828c95b331d7fad4be39c04af02ab0b76ff396546a2d118771441f398e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2641373061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed813a8f2c9cd1366b5455eb1fd1c585aa4ab0f42e380f58cb6a58f23c27eead`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:30:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:30:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:30:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:30:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:31:57 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:32:38 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:16:07 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 20:18:44 GMT
RUN $url = 'https://dl.google.com/go/go1.16.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'd40139b7ade8a3008e3240a6f86fe8f899a9c465c917e11dac8758af216f5eb0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:18:46 GMT
WORKDIR C:\gopath
# Thu, 06 May 2021 21:02:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:02:30 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 00:22:36 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:22:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 00:23:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 May 2021 00:23:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac56922ba0ee0ac19bcae98f5fb4b7427d31ef3c709f27cfb2c785fd13a611c4`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1723430d5101a2d617d3dbf4bc2a121b3f4b4432105aa2941e1afab8f130b9`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f4dc6e9a77d69a3d172368f4ae471b31c588d6201c2386e4ac62fd83faa16`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea47861a9221a4f1e5750db237c619796c612756a5e75e2cb443b1731ae8a8`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4be4ebd8eabefdb01f27dafad85e65289b95ca15591c14304c7792db99b54b`  
		Last Modified: Wed, 14 Apr 2021 12:58:35 GMT  
		Size: 30.2 MB (30155601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f66ae3738a83ea41b428b49261d4522d57df1617fbd1aa362d93f1e2802643`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2108b314c24064a0c250f72017cc64b3bf68915655327728a267c98985a5ff7`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 324.6 KB (324649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa51985154dd0edd95ef4cc022400dc16b657c4a75cb3ade3675c58d316d0101`  
		Last Modified: Thu, 06 May 2021 20:34:43 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26942e7cec550ceca0e7b0ef319dc3f732731719adfc676869678adce06d1193`  
		Last Modified: Thu, 06 May 2021 20:35:15 GMT  
		Size: 139.4 MB (139382398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e6b3adacda0d1c5092f48a23fa73f5bb807876cf3dcf7fd71632b48d8b1987`  
		Last Modified: Thu, 06 May 2021 20:34:43 GMT  
		Size: 1.6 KB (1598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6d89568ee8ac19213ae2e66b14601f80c6dd3c4a1205da5fa55da7003cd3a0`  
		Last Modified: Thu, 06 May 2021 21:06:02 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0aa20834bcdb38f731b9f6528281005b29ae951a02ef46190bf1be1cab5946`  
		Last Modified: Thu, 06 May 2021 21:06:00 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada218f8f73674eea11444ee4fa8048f2cfd6e2bfc8f8c2bb4cc40954436b6b0`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815ac3cbadfa3d6463be2a02130f663d74e486df33a07b582def59fe66dd48b0`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da0a5d30891cb84455c6b13f7a6b778a19b3a271813ef7066eb0ba908192ee7`  
		Last Modified: Tue, 11 May 2021 00:27:20 GMT  
		Size: 1.7 MB (1738012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e2cb2540135f046b5adb4957a0f75118aeb15e30d46af750522a16e6f0cc2`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.0-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:78645def8ffaedba4067a39b9ea2318211900b0a00230c004ab61982f9d41958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.4.0-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:1b2ba73c8dc7fce225f65c457524b3830589cf0fa3e9c62faa0c88b15c73c74f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5987368241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd19fd51f0fc365a83899a16ab9d8fb86585a512ff6cc33bd07e7af1bc5d89d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:35:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:35:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:35:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:35:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:38:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:39:34 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:19:05 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 20:22:32 GMT
RUN $url = 'https://dl.google.com/go/go1.16.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'd40139b7ade8a3008e3240a6f86fe8f899a9c465c917e11dac8758af216f5eb0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:22:34 GMT
WORKDIR C:\gopath
# Thu, 06 May 2021 21:03:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:03:07 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 00:23:23 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:23:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 00:25:06 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 May 2021 00:25:08 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3360763b706a564d93471b21a342ebbda7e047567cf1cbee82dd592ad33e0c`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0f653700ac9b57cf3d694cc90107e3220fc678581d1e985219677733ce242`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59d82702c225a2ca8cd2a5476122f55d8619eae959c9cb8323b68d70a2ed19`  
		Last Modified: Wed, 14 Apr 2021 12:59:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62435cd2b7652fc97ef3dc1a8968446f3f6e95f0ff1d6dcb176a3f0c2b14c2f8`  
		Last Modified: Wed, 14 Apr 2021 12:59:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d78a3a3d6cb25f55dc9d9947f7449a14717e6b787e49571a837e72b79334cf`  
		Last Modified: Wed, 14 Apr 2021 12:59:41 GMT  
		Size: 30.8 MB (30752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b774a32e346c00e004abbbd7290530d0a3f3dfb11915be2b2fa73c402da6bdd`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d153061f2f0d8ef33f71c4b9afd90899e21556e320d7103a8a9fb544c1cb521`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 5.6 MB (5608025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c85bf3447935a123c186c94d58b02a7e89b566366ab0c7a20b57fbc9e453e1`  
		Last Modified: Thu, 06 May 2021 20:35:33 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7558c3fc6da1f41d9317a885b7d1d896986e9e4a81b6487a543b93ca372649cd`  
		Last Modified: Thu, 06 May 2021 20:36:08 GMT  
		Size: 149.1 MB (149112181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d97cea35310e2e19e356bf67efe44136adb4df53f744e6497511765af70f7e`  
		Last Modified: Thu, 06 May 2021 20:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5214a4bbf455290910bf5850bebdd3fdde0c4bf2616c2975a8a91b62cfe7a`  
		Last Modified: Thu, 06 May 2021 21:06:13 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f9311ef107812e0fc28e80ff17843a7d95e33d9b4311d0ff921022f5d199c3`  
		Last Modified: Thu, 06 May 2021 21:06:10 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b921e314d8bdd24486247a7d82137f437b1572bec858ea76813dc27e580670`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8450625dd9bbf2232b7a3d1cbce4d8795d03b140b1fb962bb6042b82a073633`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394074991c1e1b9a6750cf551fb9f7fe9eaffa1a25889bebcf0f35682cb69afe`  
		Last Modified: Tue, 11 May 2021 00:27:37 GMT  
		Size: 7.0 MB (6993409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5f2fa898b0d7f2684b17b889c9c68aa767c0a1f408e2e4eceb3374cdf48393`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.0-windowsservercore`

```console
$ docker pull caddy@sha256:817273f476c97d5eb6805ecb4f1d622dd1d1eb3fcf0b537151eec68e01df8fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.4.0-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:dee876a8acfe0ad66efe5790b51e5ce47ee105518205c16c1e515107022ee466
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487145585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab04d82b7c1bbab4a4556a4ab389e58cf942f64806603d16b32d02b85377ddc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:15:27 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:15:28 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:16:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:16:04 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:16:06 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:16:07 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:16:08 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:16:10 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:16:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:16:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:16:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:16:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:16:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:16:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:16:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:16:21 GMT
EXPOSE 80
# Tue, 11 May 2021 00:16:22 GMT
EXPOSE 443
# Tue, 11 May 2021 00:16:24 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:16:51 GMT
RUN caddy version
# Tue, 11 May 2021 00:16:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a805066d9e28c5afaf71144648d2270f86d9d1dfbaa0da9a239607694e9315b6`  
		Last Modified: Tue, 11 May 2021 00:26:29 GMT  
		Size: 5.1 MB (5104734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbd0ec6de6085e7571da80b4408f11fada63d710eaf20b44c1ce63847f6455c`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1c04d9585e13e14d3ba056c3a17a8a23821f402c55d603f719fde9885fcc74`  
		Last Modified: Tue, 11 May 2021 00:26:31 GMT  
		Size: 11.9 MB (11930099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27b6dfe0db5cd7aad46afe881c42348361a2c19752cf5629eacb67967b8520`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41902606f9afaae6014164471bda32934d7f0304b3aaa65e2d7480497d85b0bc`  
		Last Modified: Tue, 11 May 2021 00:26:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9ff94e742183a75d4199b58723e286d55ecdd255b03a81ad9ec2b222c85fe1`  
		Last Modified: Tue, 11 May 2021 00:26:25 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1edf08b568698061ffae34580ddf83acab5de417993a30b8a209c919461e6a`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2873cb5c59a087bae99202d1b5f8e424378796848bf9f9f0576cb9e75da8011`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11858529cacdcdc2b7ff911a5df669b21b0efaa8c2fcbde324ccaf0a4a2d4d6`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b96fffb3765e29e3c670d5e14eb09f96a25c0222143cfac7d62c9fa6224896`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b40f5b20f6588f423dc4ba00206ef0b74da9619e96c8c26af206ea104cf85`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9116ab8bdbdeb3f51018f29b3c57d96ed1ebdff8866b0a503c7cb682741e5d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec28519386c9082afe64bc68c2e073b32a2287131bba90c6f56cc9315a638b04`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7649cdb04974c2bf32fa747aadcf57f6402a9c418e9e8f78ada74eae7aec3029`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9652bcbd02b47c702e6f2e8c374f7304cb91ba0186aede9c423104440004857d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33145d7abff94087dd683fd05403939e5aa91276d2693f6c5e8ca28641acd8e1`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a096c1bcb735f9b2cd6bf77eb582dd89b09a6cc75199dd35d65bd5cf6ad50e`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dde82b55b25477fe6eb7381cfdb3e48aa439cbd3f6352e033a85d124cecae7a`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67426815598f918caebff919df817435078c051338bebd944aafb6b25ef593f6`  
		Last Modified: Tue, 11 May 2021 00:26:20 GMT  
		Size: 331.3 KB (331282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf87ebb9031675a0e4407a36e79f274666df2a06d20c2452c1e0acec70fc60a6`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.0-windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:b61efb630c29dfd10f857eed823207497fd9c94176f47243f48c641119c663d3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818059080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3940d8ab2b2d69a458bd9951c005b3703a5ac35754896cbfd380305f8dfe27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:18:49 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:18:50 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:20:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:20:40 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:20:42 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:20:43 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:20:45 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:20:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:20:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:20:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:20:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:20:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:20:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:20:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:20:56 GMT
EXPOSE 80
# Tue, 11 May 2021 00:20:58 GMT
EXPOSE 443
# Tue, 11 May 2021 00:20:59 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:22:14 GMT
RUN caddy version
# Tue, 11 May 2021 00:22:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc088e7513f9bd5e2261035715cd5f39aff459f086737be39631a5c03dd0bc9`  
		Last Modified: Tue, 11 May 2021 00:27:00 GMT  
		Size: 5.7 MB (5678806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a94477e69ebd7355bfc6230d3309aa20d4fda7d504dc34bd3b2adae7f5f2b4`  
		Last Modified: Tue, 11 May 2021 00:26:57 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db416be1d5a7c97652523c359440855c0ef2127ac11cb08595aa068d99d8a5`  
		Last Modified: Tue, 11 May 2021 00:27:03 GMT  
		Size: 17.2 MB (17201492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e500af558c7988b44d7fae2a1a8c1d4498cb130d1de721a37712c33f09147a`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87b8476ce7fba27f66c08050c4a692f8a19ec0c84e9d42537b4b4b8bbb5f56e`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2d6240d48682965790d983fc3f6b5404aeb7f3f023b517ab83b6e47c20af5c`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757d21ff239a36a372b7fb98d22d42afd8f3c779c7b342605186d6b2a14925e7`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5e64a8fa017a3b5df9f60508bc7b3f72fe2835f00c086648f26235c9358b14`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac63d4edb89dc9920755d7e04e444610a75ac1268b103c178ebff146f490d73`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fbb5cca77bbd06aabe9371bf1fe894938b82367a0ef11be873b231a43b64ab`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b0ecb05ae3d1fffc947acf96dea7fe481fd9a745d4fcf79bff9f4b21a28817`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f292068b665f33bccf70f8100aa252145e0f63abb2283fa29d36cadcc6291c52`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1995472761eea00392fa2ce2d1566a7233a89a019e939892cbb0aeb4a8a3a07a`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e8f37215e61d4f10f002f5ad82c4acadf4a56b559cf036050f33242bfe1e35`  
		Last Modified: Tue, 11 May 2021 00:26:49 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2f6fb7cf636418bada10647c66ee3b92246da967ebb611d58aad6725f5e2b`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271eda8ea06432cb0dae8fd93e8a85314e86201450cdbebf3efcbba2dbd4331`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a4da75f19907c0ee148b5369a63863a2752457cc31b02fe68779d83d56c1`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7013990e537c69857c80a4d6fb386f6d0f04e5a0a5ee5b12ed57c0e458fc8e`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b661b1f2a589a6717a5599a78cb0f3ef950c1a36bd411039dfd39afb20e901b`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 269.3 KB (269349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e686f1164cdcf35434a7d997c0c9ff058302aaade06ace7c5f8a2e4a718aa`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.0-windowsservercore-1809`

```console
$ docker pull caddy@sha256:a72b70da0fa644b846c169807c236cbe93c8103aa45a3e172d7c9247d5ebc445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `caddy:2.4.0-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:dee876a8acfe0ad66efe5790b51e5ce47ee105518205c16c1e515107022ee466
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487145585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab04d82b7c1bbab4a4556a4ab389e58cf942f64806603d16b32d02b85377ddc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:15:27 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:15:28 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:16:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:16:04 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:16:06 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:16:07 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:16:08 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:16:10 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:16:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:16:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:16:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:16:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:16:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:16:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:16:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:16:21 GMT
EXPOSE 80
# Tue, 11 May 2021 00:16:22 GMT
EXPOSE 443
# Tue, 11 May 2021 00:16:24 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:16:51 GMT
RUN caddy version
# Tue, 11 May 2021 00:16:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a805066d9e28c5afaf71144648d2270f86d9d1dfbaa0da9a239607694e9315b6`  
		Last Modified: Tue, 11 May 2021 00:26:29 GMT  
		Size: 5.1 MB (5104734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbd0ec6de6085e7571da80b4408f11fada63d710eaf20b44c1ce63847f6455c`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1c04d9585e13e14d3ba056c3a17a8a23821f402c55d603f719fde9885fcc74`  
		Last Modified: Tue, 11 May 2021 00:26:31 GMT  
		Size: 11.9 MB (11930099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27b6dfe0db5cd7aad46afe881c42348361a2c19752cf5629eacb67967b8520`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41902606f9afaae6014164471bda32934d7f0304b3aaa65e2d7480497d85b0bc`  
		Last Modified: Tue, 11 May 2021 00:26:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9ff94e742183a75d4199b58723e286d55ecdd255b03a81ad9ec2b222c85fe1`  
		Last Modified: Tue, 11 May 2021 00:26:25 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1edf08b568698061ffae34580ddf83acab5de417993a30b8a209c919461e6a`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2873cb5c59a087bae99202d1b5f8e424378796848bf9f9f0576cb9e75da8011`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11858529cacdcdc2b7ff911a5df669b21b0efaa8c2fcbde324ccaf0a4a2d4d6`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b96fffb3765e29e3c670d5e14eb09f96a25c0222143cfac7d62c9fa6224896`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b40f5b20f6588f423dc4ba00206ef0b74da9619e96c8c26af206ea104cf85`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9116ab8bdbdeb3f51018f29b3c57d96ed1ebdff8866b0a503c7cb682741e5d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec28519386c9082afe64bc68c2e073b32a2287131bba90c6f56cc9315a638b04`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7649cdb04974c2bf32fa747aadcf57f6402a9c418e9e8f78ada74eae7aec3029`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9652bcbd02b47c702e6f2e8c374f7304cb91ba0186aede9c423104440004857d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33145d7abff94087dd683fd05403939e5aa91276d2693f6c5e8ca28641acd8e1`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a096c1bcb735f9b2cd6bf77eb582dd89b09a6cc75199dd35d65bd5cf6ad50e`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dde82b55b25477fe6eb7381cfdb3e48aa439cbd3f6352e033a85d124cecae7a`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67426815598f918caebff919df817435078c051338bebd944aafb6b25ef593f6`  
		Last Modified: Tue, 11 May 2021 00:26:20 GMT  
		Size: 331.3 KB (331282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf87ebb9031675a0e4407a36e79f274666df2a06d20c2452c1e0acec70fc60a6`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.0-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:54f2ce6cefa5785e781847e6fe0fbe6ce716fb6c5bc0de5a49b4cb71cc8f1cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `caddy:2.4.0-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:b61efb630c29dfd10f857eed823207497fd9c94176f47243f48c641119c663d3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818059080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3940d8ab2b2d69a458bd9951c005b3703a5ac35754896cbfd380305f8dfe27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:18:49 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:18:50 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:20:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:20:40 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:20:42 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:20:43 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:20:45 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:20:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:20:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:20:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:20:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:20:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:20:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:20:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:20:56 GMT
EXPOSE 80
# Tue, 11 May 2021 00:20:58 GMT
EXPOSE 443
# Tue, 11 May 2021 00:20:59 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:22:14 GMT
RUN caddy version
# Tue, 11 May 2021 00:22:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc088e7513f9bd5e2261035715cd5f39aff459f086737be39631a5c03dd0bc9`  
		Last Modified: Tue, 11 May 2021 00:27:00 GMT  
		Size: 5.7 MB (5678806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a94477e69ebd7355bfc6230d3309aa20d4fda7d504dc34bd3b2adae7f5f2b4`  
		Last Modified: Tue, 11 May 2021 00:26:57 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db416be1d5a7c97652523c359440855c0ef2127ac11cb08595aa068d99d8a5`  
		Last Modified: Tue, 11 May 2021 00:27:03 GMT  
		Size: 17.2 MB (17201492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e500af558c7988b44d7fae2a1a8c1d4498cb130d1de721a37712c33f09147a`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87b8476ce7fba27f66c08050c4a692f8a19ec0c84e9d42537b4b4b8bbb5f56e`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2d6240d48682965790d983fc3f6b5404aeb7f3f023b517ab83b6e47c20af5c`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757d21ff239a36a372b7fb98d22d42afd8f3c779c7b342605186d6b2a14925e7`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5e64a8fa017a3b5df9f60508bc7b3f72fe2835f00c086648f26235c9358b14`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac63d4edb89dc9920755d7e04e444610a75ac1268b103c178ebff146f490d73`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fbb5cca77bbd06aabe9371bf1fe894938b82367a0ef11be873b231a43b64ab`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b0ecb05ae3d1fffc947acf96dea7fe481fd9a745d4fcf79bff9f4b21a28817`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f292068b665f33bccf70f8100aa252145e0f63abb2283fa29d36cadcc6291c52`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1995472761eea00392fa2ce2d1566a7233a89a019e939892cbb0aeb4a8a3a07a`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e8f37215e61d4f10f002f5ad82c4acadf4a56b559cf036050f33242bfe1e35`  
		Last Modified: Tue, 11 May 2021 00:26:49 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2f6fb7cf636418bada10647c66ee3b92246da967ebb611d58aad6725f5e2b`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271eda8ea06432cb0dae8fd93e8a85314e86201450cdbebf3efcbba2dbd4331`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a4da75f19907c0ee148b5369a63863a2752457cc31b02fe68779d83d56c1`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7013990e537c69857c80a4d6fb386f6d0f04e5a0a5ee5b12ed57c0e458fc8e`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b661b1f2a589a6717a5599a78cb0f3ef950c1a36bd411039dfd39afb20e901b`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 269.3 KB (269349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e686f1164cdcf35434a7d997c0c9ff058302aaade06ace7c5f8a2e4a718aa`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

## `caddy:builder`

```console
$ docker pull caddy@sha256:425b1075398c4ebde59024ee2847746c5b54171ee16096bb85d4a99aa6de8398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:046f9aa5dcf83fb25e28e43539c520c8cd0dfe05faf14ad780826c7c36775145
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116541075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd288b16c2ac5e35de34025c916a8a52cb8c3c35644e3e2beee860100beea6de`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:27:12 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:27:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:27:13 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:18:07 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:20:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:20:05 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:20:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:20:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:20:07 GMT
WORKDIR /go
# Fri, 07 May 2021 01:56:14 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:56:14 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 01:04:35 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:04:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 01:04:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 11 May 2021 01:04:38 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 11 May 2021 01:04:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc1eea9eeabb6de296adb3e0c1b0722cf13251ff3e4e2d0a5f7ed8e3d48342`  
		Last Modified: Wed, 14 Apr 2021 21:35:06 GMT  
		Size: 281.3 KB (281269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4ab2625f07be8d5c6e48046a05ff3ecc7f374b794a926fb62247b66b511909`  
		Last Modified: Wed, 14 Apr 2021 21:35:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e7595549f7536d76f08a8a23fb67e3e6fae08ccf3add715c5c1c956f9445d2`  
		Last Modified: Thu, 06 May 2021 23:29:42 GMT  
		Size: 105.7 MB (105745828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df88182f7acff97ffde9f614a0fd86e8a26590e445aa76e442c3a79d9e4c4f4`  
		Last Modified: Thu, 06 May 2021 23:29:25 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d573d19fd03835237c7687f4f394fa6b1fc1c894a901f2853846256ee7746eb`  
		Last Modified: Fri, 07 May 2021 01:56:57 GMT  
		Size: 6.4 MB (6390123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95db25f5b69783a08df8902a5330daddf1e8b10bd1d8401b25d8f8ab43b6586f`  
		Last Modified: Tue, 11 May 2021 01:05:15 GMT  
		Size: 1.3 MB (1311169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bfbae6287f60c1e9b89dd3e92e73d9f949ee6f11d78bc97a3e945ee20b2c68`  
		Last Modified: Tue, 11 May 2021 01:05:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:124237c870217e836b67b4697d7cddad2c3c58d50878dc51654db3605712c336
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112278566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bef88e43f4622abd673fe82f110eb193559dd1abb2d8550178eb66032b4b5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:00:55 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:01:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:01:02 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:24:09 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 21:27:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 21:27:32 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 21:27:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:27:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 21:27:35 GMT
WORKDIR /go
# Thu, 06 May 2021 22:10:19 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 06 May 2021 22:10:20 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:51:04 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:51:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:51:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:51:14 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:51:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4dea9fd179326b36ea137aad07e06571ffe7ad849e2a13a32354dcfd5d858d`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 281.4 KB (281379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abeb04d84d23abf8470fc95982483a9117a87e55b13c591f5332a460a5233bb`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a3721aaa7ffedbec829a557c2d5f99c4661695a51f82632ece4df509b71bc1`  
		Last Modified: Thu, 06 May 2021 21:38:30 GMT  
		Size: 101.9 MB (101925593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298c78bc6b40a671a2f9a64d2cecf253acd10da30924ff687012e02b0307a1a8`  
		Last Modified: Thu, 06 May 2021 21:37:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3d237d41fc2805c9d9a047d4bb2618233c7093cc31d682b5231e0261a8c201`  
		Last Modified: Thu, 06 May 2021 22:11:03 GMT  
		Size: 6.2 MB (6227066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ffbb7f2dd65c638ffd56b2ab5964193545041922501d15451a2b6f4b0b0edb`  
		Last Modified: Mon, 10 May 2021 23:51:50 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d30db79a4a633e8984befac9884a645ed6f3bd581f677daa8a26f2cbda65a4`  
		Last Modified: Mon, 10 May 2021 23:51:50 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:a4ecc2040cdcc0166a3fea577c4e704d291fe70c2c65c460ff347d06c2b54046
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111227459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d2c6dfa3a578099a3e909c80cd793b780fb7a9135d5f28ec25270157a0902f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:00:38 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:01:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:01:41 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:11:51 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:15:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:15:25 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:15:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:15:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:15:29 GMT
WORKDIR /go
# Fri, 07 May 2021 02:34:14 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:34:14 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 01:17:54 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:18:06 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 01:18:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 11 May 2021 01:18:32 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 11 May 2021 01:18:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6bd423db0b63fdc83c72eae7ef401cb2fb9eaa63961c71a867ff26bfe422f`  
		Last Modified: Wed, 14 Apr 2021 22:44:20 GMT  
		Size: 280.5 KB (280532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835b667ae68ff940439602ffbabae6e923c687cb56c62a793f23ddca67584049`  
		Last Modified: Wed, 14 Apr 2021 22:44:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5b93a32354ff48887c2e9c4540875b8aa57822ab5c261d95e3c186d27b5c5e`  
		Last Modified: Thu, 06 May 2021 23:28:23 GMT  
		Size: 101.7 MB (101743890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2925b4cee8520caf8150ba3410d1306c50fa326f2fd920488f9e432578fda5`  
		Last Modified: Thu, 06 May 2021 23:27:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc435726a63967cbbe522309fca3524e0e1fd01e955717cedc9e172d632cbd1`  
		Last Modified: Fri, 07 May 2021 02:34:54 GMT  
		Size: 5.6 MB (5558665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd402931cf263713336d2aa524723f4caec26b90c0d6406651b14a2f88a642ab`  
		Last Modified: Tue, 11 May 2021 01:19:24 GMT  
		Size: 1.2 MB (1219508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee3295bff1b446bc98e483336ce527bcd52ccfecd1930eba95c70c26e909f3a`  
		Last Modified: Tue, 11 May 2021 01:19:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:a8418ff913feb35632b8e2e0e2dde138632b289047de19713b0c24fe65c6eecc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111763060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68622e818b4c271dd7faf093081a9641f809d407eb6dc67bb6afe822393b4b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:40:18 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:40:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:40:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:31:41 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 22:33:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 22:33:53 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 22:33:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:33:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 22:33:57 GMT
WORKDIR /go
# Fri, 07 May 2021 01:17:18 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:17:19 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:40:20 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:40:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:40:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:40:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:40:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7186ed65a4f7bb0e9cd4b00f43359b47a4f19749dbd48e704fc578a4f43d7c96`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 281.5 KB (281488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316046926c0ae5f42710c1197ed3de9fc374986179c18611f523cf4521adeef1`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a969ea94b7c2e3938ec670b72c32f58ece636bb7ec6526d0efab40e760bce`  
		Last Modified: Thu, 06 May 2021 22:44:20 GMT  
		Size: 101.1 MB (101090590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff4d3f41a5567d10cda7e4f3c4267dbb9181eb63bb52c950c3dce3327a9a36e`  
		Last Modified: Thu, 06 May 2021 22:43:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ec12dccc6ac2c5238a0e958e58c89d37f56cf2e181ba8a4f291b176a2a20fa`  
		Last Modified: Fri, 07 May 2021 01:18:00 GMT  
		Size: 6.5 MB (6476691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803dba8659a2ec5c5a177383797832eca7c7d301ec4253e47ee42527aa617bac`  
		Last Modified: Mon, 10 May 2021 23:40:59 GMT  
		Size: 1.2 MB (1201547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e70f326991067a04529de021321ce20d6920e81d14aaef93afb92136c976508`  
		Last Modified: Mon, 10 May 2021 23:40:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:58ffe092c4ccbd15cf9faf25d63caa632bb639d53188a377038834ebf2dac85a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110621059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2321e3937c686734c8c9124a34811d9eb4092b7611145be19ea453a5bbb389a4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:53:57 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 22:54:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:54:14 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:22:47 GMT
ENV GOLANG_VERSION=1.16.4
# Fri, 07 May 2021 00:25:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 07 May 2021 00:25:26 GMT
ENV GOPATH=/go
# Fri, 07 May 2021 00:25:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:25:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 07 May 2021 00:26:14 GMT
WORKDIR /go
# Fri, 07 May 2021 08:19:51 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 08:19:57 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 01:19:13 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:19:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 01:19:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 11 May 2021 01:19:30 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 11 May 2021 01:19:37 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf726c40dc4802009a4b6f0f7947c86242c2c078623e8f1f21343864093b3a9`  
		Last Modified: Wed, 14 Apr 2021 23:05:31 GMT  
		Size: 283.4 KB (283413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c17712dac96942b05a27f88ea5346bd57b4cabdb33c153562ef144635225b3`  
		Last Modified: Wed, 14 Apr 2021 23:05:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d2e93731067b7b48232c826d062ff4fead572dbd98e0a28642db4802342a8e`  
		Last Modified: Fri, 07 May 2021 00:41:39 GMT  
		Size: 99.5 MB (99528032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca0e521f95ca5f22fdd4b7917d06aead7df46288885c4fd3ffac0242b96643f`  
		Last Modified: Fri, 07 May 2021 00:41:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9dfa7e81a349fea3e170fbc6f6b9fd3245ee43c53b329a3ae72c9e5ebaddfb`  
		Last Modified: Fri, 07 May 2021 08:22:18 GMT  
		Size: 6.8 MB (6825232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f3bfd07b70b357098f4ba50744bf3c838e8c3ab709598b79864f29b676311`  
		Last Modified: Tue, 11 May 2021 01:20:23 GMT  
		Size: 1.2 MB (1170526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68dce6545308f135393f568603954610d88f7a8a61ca402820d75500d925926c`  
		Last Modified: Tue, 11 May 2021 01:20:23 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:e72252e76203d04b2ed847e26d71ca0de7ed89c2d76990ac177fb80755d88617
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115474412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08b1e73df9c564bfdb9249c0d32c47642dd69cd88bfa280b4682767ef8fe671`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:45:11 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:45:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:45:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:16:38 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:20:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:20:18 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:20:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:20:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:20:21 GMT
WORKDIR /go
# Fri, 07 May 2021 02:02:34 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:02:35 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:42:03 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:42:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:42:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:42:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:42:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc746875ae346ee6ec3c9080f8a7a50bef3899ea9d5ae9dac45a81bfe861c9d`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 281.7 KB (281708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0242688236000dd8f33d16f89f36da3ef1bb2a7a32bb59a7eb97a18ed3d5158`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37dab17b6808078a43afd3d62f1a202857192406e914c33d5ceb5eec1eb05eeb`  
		Last Modified: Thu, 06 May 2021 23:34:08 GMT  
		Size: 104.8 MB (104849388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6059cb089a1bd1108012ddff056f297d814995f95d29d57b15c13d11baede00d`  
		Last Modified: Thu, 06 May 2021 23:33:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84919c1c43955cfb518f179d4f6b541cdfa94579f6f6ef10fdc6e6b3ca4d51a3`  
		Last Modified: Fri, 07 May 2021 02:03:18 GMT  
		Size: 6.5 MB (6475416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3025f5e46ec68c9ef05a49a22ca89718a0d154f401122b0505a18d1c9217fc`  
		Last Modified: Mon, 10 May 2021 23:42:38 GMT  
		Size: 1.3 MB (1264531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bb5d9c7e67f1492e82b3f7c19e6900095d43b1f65fa5496f752a95169cd953`  
		Last Modified: Mon, 10 May 2021 23:42:38 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:bc783b828c95b331d7fad4be39c04af02ab0b76ff396546a2d118771441f398e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2641373061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed813a8f2c9cd1366b5455eb1fd1c585aa4ab0f42e380f58cb6a58f23c27eead`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:30:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:30:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:30:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:30:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:31:57 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:32:38 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:16:07 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 20:18:44 GMT
RUN $url = 'https://dl.google.com/go/go1.16.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'd40139b7ade8a3008e3240a6f86fe8f899a9c465c917e11dac8758af216f5eb0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:18:46 GMT
WORKDIR C:\gopath
# Thu, 06 May 2021 21:02:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:02:30 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 00:22:36 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:22:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 00:23:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 May 2021 00:23:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac56922ba0ee0ac19bcae98f5fb4b7427d31ef3c709f27cfb2c785fd13a611c4`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1723430d5101a2d617d3dbf4bc2a121b3f4b4432105aa2941e1afab8f130b9`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f4dc6e9a77d69a3d172368f4ae471b31c588d6201c2386e4ac62fd83faa16`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea47861a9221a4f1e5750db237c619796c612756a5e75e2cb443b1731ae8a8`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4be4ebd8eabefdb01f27dafad85e65289b95ca15591c14304c7792db99b54b`  
		Last Modified: Wed, 14 Apr 2021 12:58:35 GMT  
		Size: 30.2 MB (30155601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f66ae3738a83ea41b428b49261d4522d57df1617fbd1aa362d93f1e2802643`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2108b314c24064a0c250f72017cc64b3bf68915655327728a267c98985a5ff7`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 324.6 KB (324649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa51985154dd0edd95ef4cc022400dc16b657c4a75cb3ade3675c58d316d0101`  
		Last Modified: Thu, 06 May 2021 20:34:43 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26942e7cec550ceca0e7b0ef319dc3f732731719adfc676869678adce06d1193`  
		Last Modified: Thu, 06 May 2021 20:35:15 GMT  
		Size: 139.4 MB (139382398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e6b3adacda0d1c5092f48a23fa73f5bb807876cf3dcf7fd71632b48d8b1987`  
		Last Modified: Thu, 06 May 2021 20:34:43 GMT  
		Size: 1.6 KB (1598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6d89568ee8ac19213ae2e66b14601f80c6dd3c4a1205da5fa55da7003cd3a0`  
		Last Modified: Thu, 06 May 2021 21:06:02 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0aa20834bcdb38f731b9f6528281005b29ae951a02ef46190bf1be1cab5946`  
		Last Modified: Thu, 06 May 2021 21:06:00 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada218f8f73674eea11444ee4fa8048f2cfd6e2bfc8f8c2bb4cc40954436b6b0`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815ac3cbadfa3d6463be2a02130f663d74e486df33a07b582def59fe66dd48b0`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da0a5d30891cb84455c6b13f7a6b778a19b3a271813ef7066eb0ba908192ee7`  
		Last Modified: Tue, 11 May 2021 00:27:20 GMT  
		Size: 1.7 MB (1738012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e2cb2540135f046b5adb4957a0f75118aeb15e30d46af750522a16e6f0cc2`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:1b2ba73c8dc7fce225f65c457524b3830589cf0fa3e9c62faa0c88b15c73c74f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5987368241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd19fd51f0fc365a83899a16ab9d8fb86585a512ff6cc33bd07e7af1bc5d89d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:35:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:35:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:35:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:35:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:38:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:39:34 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:19:05 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 20:22:32 GMT
RUN $url = 'https://dl.google.com/go/go1.16.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'd40139b7ade8a3008e3240a6f86fe8f899a9c465c917e11dac8758af216f5eb0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:22:34 GMT
WORKDIR C:\gopath
# Thu, 06 May 2021 21:03:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:03:07 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 00:23:23 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:23:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 00:25:06 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 May 2021 00:25:08 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3360763b706a564d93471b21a342ebbda7e047567cf1cbee82dd592ad33e0c`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0f653700ac9b57cf3d694cc90107e3220fc678581d1e985219677733ce242`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59d82702c225a2ca8cd2a5476122f55d8619eae959c9cb8323b68d70a2ed19`  
		Last Modified: Wed, 14 Apr 2021 12:59:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62435cd2b7652fc97ef3dc1a8968446f3f6e95f0ff1d6dcb176a3f0c2b14c2f8`  
		Last Modified: Wed, 14 Apr 2021 12:59:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d78a3a3d6cb25f55dc9d9947f7449a14717e6b787e49571a837e72b79334cf`  
		Last Modified: Wed, 14 Apr 2021 12:59:41 GMT  
		Size: 30.8 MB (30752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b774a32e346c00e004abbbd7290530d0a3f3dfb11915be2b2fa73c402da6bdd`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d153061f2f0d8ef33f71c4b9afd90899e21556e320d7103a8a9fb544c1cb521`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 5.6 MB (5608025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c85bf3447935a123c186c94d58b02a7e89b566366ab0c7a20b57fbc9e453e1`  
		Last Modified: Thu, 06 May 2021 20:35:33 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7558c3fc6da1f41d9317a885b7d1d896986e9e4a81b6487a543b93ca372649cd`  
		Last Modified: Thu, 06 May 2021 20:36:08 GMT  
		Size: 149.1 MB (149112181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d97cea35310e2e19e356bf67efe44136adb4df53f744e6497511765af70f7e`  
		Last Modified: Thu, 06 May 2021 20:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5214a4bbf455290910bf5850bebdd3fdde0c4bf2616c2975a8a91b62cfe7a`  
		Last Modified: Thu, 06 May 2021 21:06:13 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f9311ef107812e0fc28e80ff17843a7d95e33d9b4311d0ff921022f5d199c3`  
		Last Modified: Thu, 06 May 2021 21:06:10 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b921e314d8bdd24486247a7d82137f437b1572bec858ea76813dc27e580670`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8450625dd9bbf2232b7a3d1cbce4d8795d03b140b1fb962bb6042b82a073633`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394074991c1e1b9a6750cf551fb9f7fe9eaffa1a25889bebcf0f35682cb69afe`  
		Last Modified: Tue, 11 May 2021 00:27:37 GMT  
		Size: 7.0 MB (6993409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5f2fa898b0d7f2684b17b889c9c68aa767c0a1f408e2e4eceb3374cdf48393`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:8b8beeef5c72efc27da7a1cdf0a8f816303907f9733c13386d25ebc6e7f785b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:046f9aa5dcf83fb25e28e43539c520c8cd0dfe05faf14ad780826c7c36775145
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116541075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd288b16c2ac5e35de34025c916a8a52cb8c3c35644e3e2beee860100beea6de`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:27:12 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:27:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:27:13 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:18:07 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:20:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:20:05 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:20:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:20:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:20:07 GMT
WORKDIR /go
# Fri, 07 May 2021 01:56:14 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:56:14 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 01:04:35 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:04:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 01:04:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 11 May 2021 01:04:38 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 11 May 2021 01:04:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc1eea9eeabb6de296adb3e0c1b0722cf13251ff3e4e2d0a5f7ed8e3d48342`  
		Last Modified: Wed, 14 Apr 2021 21:35:06 GMT  
		Size: 281.3 KB (281269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4ab2625f07be8d5c6e48046a05ff3ecc7f374b794a926fb62247b66b511909`  
		Last Modified: Wed, 14 Apr 2021 21:35:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e7595549f7536d76f08a8a23fb67e3e6fae08ccf3add715c5c1c956f9445d2`  
		Last Modified: Thu, 06 May 2021 23:29:42 GMT  
		Size: 105.7 MB (105745828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df88182f7acff97ffde9f614a0fd86e8a26590e445aa76e442c3a79d9e4c4f4`  
		Last Modified: Thu, 06 May 2021 23:29:25 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d573d19fd03835237c7687f4f394fa6b1fc1c894a901f2853846256ee7746eb`  
		Last Modified: Fri, 07 May 2021 01:56:57 GMT  
		Size: 6.4 MB (6390123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95db25f5b69783a08df8902a5330daddf1e8b10bd1d8401b25d8f8ab43b6586f`  
		Last Modified: Tue, 11 May 2021 01:05:15 GMT  
		Size: 1.3 MB (1311169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bfbae6287f60c1e9b89dd3e92e73d9f949ee6f11d78bc97a3e945ee20b2c68`  
		Last Modified: Tue, 11 May 2021 01:05:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:124237c870217e836b67b4697d7cddad2c3c58d50878dc51654db3605712c336
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112278566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bef88e43f4622abd673fe82f110eb193559dd1abb2d8550178eb66032b4b5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:00:55 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:01:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:01:02 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:24:09 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 21:27:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 21:27:32 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 21:27:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:27:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 21:27:35 GMT
WORKDIR /go
# Thu, 06 May 2021 22:10:19 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 06 May 2021 22:10:20 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:51:04 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:51:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:51:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:51:14 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:51:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4dea9fd179326b36ea137aad07e06571ffe7ad849e2a13a32354dcfd5d858d`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 281.4 KB (281379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abeb04d84d23abf8470fc95982483a9117a87e55b13c591f5332a460a5233bb`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a3721aaa7ffedbec829a557c2d5f99c4661695a51f82632ece4df509b71bc1`  
		Last Modified: Thu, 06 May 2021 21:38:30 GMT  
		Size: 101.9 MB (101925593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298c78bc6b40a671a2f9a64d2cecf253acd10da30924ff687012e02b0307a1a8`  
		Last Modified: Thu, 06 May 2021 21:37:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3d237d41fc2805c9d9a047d4bb2618233c7093cc31d682b5231e0261a8c201`  
		Last Modified: Thu, 06 May 2021 22:11:03 GMT  
		Size: 6.2 MB (6227066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ffbb7f2dd65c638ffd56b2ab5964193545041922501d15451a2b6f4b0b0edb`  
		Last Modified: Mon, 10 May 2021 23:51:50 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d30db79a4a633e8984befac9884a645ed6f3bd581f677daa8a26f2cbda65a4`  
		Last Modified: Mon, 10 May 2021 23:51:50 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:a4ecc2040cdcc0166a3fea577c4e704d291fe70c2c65c460ff347d06c2b54046
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111227459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d2c6dfa3a578099a3e909c80cd793b780fb7a9135d5f28ec25270157a0902f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:00:38 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:01:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:01:41 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:11:51 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:15:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:15:25 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:15:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:15:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:15:29 GMT
WORKDIR /go
# Fri, 07 May 2021 02:34:14 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:34:14 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 01:17:54 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:18:06 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 01:18:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 11 May 2021 01:18:32 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 11 May 2021 01:18:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6bd423db0b63fdc83c72eae7ef401cb2fb9eaa63961c71a867ff26bfe422f`  
		Last Modified: Wed, 14 Apr 2021 22:44:20 GMT  
		Size: 280.5 KB (280532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835b667ae68ff940439602ffbabae6e923c687cb56c62a793f23ddca67584049`  
		Last Modified: Wed, 14 Apr 2021 22:44:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5b93a32354ff48887c2e9c4540875b8aa57822ab5c261d95e3c186d27b5c5e`  
		Last Modified: Thu, 06 May 2021 23:28:23 GMT  
		Size: 101.7 MB (101743890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2925b4cee8520caf8150ba3410d1306c50fa326f2fd920488f9e432578fda5`  
		Last Modified: Thu, 06 May 2021 23:27:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc435726a63967cbbe522309fca3524e0e1fd01e955717cedc9e172d632cbd1`  
		Last Modified: Fri, 07 May 2021 02:34:54 GMT  
		Size: 5.6 MB (5558665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd402931cf263713336d2aa524723f4caec26b90c0d6406651b14a2f88a642ab`  
		Last Modified: Tue, 11 May 2021 01:19:24 GMT  
		Size: 1.2 MB (1219508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee3295bff1b446bc98e483336ce527bcd52ccfecd1930eba95c70c26e909f3a`  
		Last Modified: Tue, 11 May 2021 01:19:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:a8418ff913feb35632b8e2e0e2dde138632b289047de19713b0c24fe65c6eecc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111763060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68622e818b4c271dd7faf093081a9641f809d407eb6dc67bb6afe822393b4b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:40:18 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:40:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:40:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:31:41 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 22:33:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 22:33:53 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 22:33:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:33:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 22:33:57 GMT
WORKDIR /go
# Fri, 07 May 2021 01:17:18 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:17:19 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:40:20 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:40:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:40:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:40:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:40:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7186ed65a4f7bb0e9cd4b00f43359b47a4f19749dbd48e704fc578a4f43d7c96`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 281.5 KB (281488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316046926c0ae5f42710c1197ed3de9fc374986179c18611f523cf4521adeef1`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a969ea94b7c2e3938ec670b72c32f58ece636bb7ec6526d0efab40e760bce`  
		Last Modified: Thu, 06 May 2021 22:44:20 GMT  
		Size: 101.1 MB (101090590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff4d3f41a5567d10cda7e4f3c4267dbb9181eb63bb52c950c3dce3327a9a36e`  
		Last Modified: Thu, 06 May 2021 22:43:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ec12dccc6ac2c5238a0e958e58c89d37f56cf2e181ba8a4f291b176a2a20fa`  
		Last Modified: Fri, 07 May 2021 01:18:00 GMT  
		Size: 6.5 MB (6476691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803dba8659a2ec5c5a177383797832eca7c7d301ec4253e47ee42527aa617bac`  
		Last Modified: Mon, 10 May 2021 23:40:59 GMT  
		Size: 1.2 MB (1201547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e70f326991067a04529de021321ce20d6920e81d14aaef93afb92136c976508`  
		Last Modified: Mon, 10 May 2021 23:40:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:58ffe092c4ccbd15cf9faf25d63caa632bb639d53188a377038834ebf2dac85a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110621059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2321e3937c686734c8c9124a34811d9eb4092b7611145be19ea453a5bbb389a4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:53:57 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 22:54:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:54:14 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:22:47 GMT
ENV GOLANG_VERSION=1.16.4
# Fri, 07 May 2021 00:25:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 07 May 2021 00:25:26 GMT
ENV GOPATH=/go
# Fri, 07 May 2021 00:25:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:25:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 07 May 2021 00:26:14 GMT
WORKDIR /go
# Fri, 07 May 2021 08:19:51 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 08:19:57 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 01:19:13 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:19:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 01:19:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 11 May 2021 01:19:30 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 11 May 2021 01:19:37 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf726c40dc4802009a4b6f0f7947c86242c2c078623e8f1f21343864093b3a9`  
		Last Modified: Wed, 14 Apr 2021 23:05:31 GMT  
		Size: 283.4 KB (283413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c17712dac96942b05a27f88ea5346bd57b4cabdb33c153562ef144635225b3`  
		Last Modified: Wed, 14 Apr 2021 23:05:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d2e93731067b7b48232c826d062ff4fead572dbd98e0a28642db4802342a8e`  
		Last Modified: Fri, 07 May 2021 00:41:39 GMT  
		Size: 99.5 MB (99528032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca0e521f95ca5f22fdd4b7917d06aead7df46288885c4fd3ffac0242b96643f`  
		Last Modified: Fri, 07 May 2021 00:41:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9dfa7e81a349fea3e170fbc6f6b9fd3245ee43c53b329a3ae72c9e5ebaddfb`  
		Last Modified: Fri, 07 May 2021 08:22:18 GMT  
		Size: 6.8 MB (6825232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f3bfd07b70b357098f4ba50744bf3c838e8c3ab709598b79864f29b676311`  
		Last Modified: Tue, 11 May 2021 01:20:23 GMT  
		Size: 1.2 MB (1170526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68dce6545308f135393f568603954610d88f7a8a61ca402820d75500d925926c`  
		Last Modified: Tue, 11 May 2021 01:20:23 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:e72252e76203d04b2ed847e26d71ca0de7ed89c2d76990ac177fb80755d88617
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115474412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08b1e73df9c564bfdb9249c0d32c47642dd69cd88bfa280b4682767ef8fe671`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:45:11 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:45:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:45:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:16:38 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:20:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:20:18 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:20:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:20:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:20:21 GMT
WORKDIR /go
# Fri, 07 May 2021 02:02:34 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:02:35 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:42:03 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:42:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:42:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:42:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:42:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc746875ae346ee6ec3c9080f8a7a50bef3899ea9d5ae9dac45a81bfe861c9d`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 281.7 KB (281708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0242688236000dd8f33d16f89f36da3ef1bb2a7a32bb59a7eb97a18ed3d5158`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37dab17b6808078a43afd3d62f1a202857192406e914c33d5ceb5eec1eb05eeb`  
		Last Modified: Thu, 06 May 2021 23:34:08 GMT  
		Size: 104.8 MB (104849388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6059cb089a1bd1108012ddff056f297d814995f95d29d57b15c13d11baede00d`  
		Last Modified: Thu, 06 May 2021 23:33:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84919c1c43955cfb518f179d4f6b541cdfa94579f6f6ef10fdc6e6b3ca4d51a3`  
		Last Modified: Fri, 07 May 2021 02:03:18 GMT  
		Size: 6.5 MB (6475416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3025f5e46ec68c9ef05a49a22ca89718a0d154f401122b0505a18d1c9217fc`  
		Last Modified: Mon, 10 May 2021 23:42:38 GMT  
		Size: 1.3 MB (1264531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bb5d9c7e67f1492e82b3f7c19e6900095d43b1f65fa5496f752a95169cd953`  
		Last Modified: Mon, 10 May 2021 23:42:38 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:a6cb45df3913c41d877ad5dea68ac399f038d58e244fc5f2637971201ece8f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:bc783b828c95b331d7fad4be39c04af02ab0b76ff396546a2d118771441f398e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2641373061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed813a8f2c9cd1366b5455eb1fd1c585aa4ab0f42e380f58cb6a58f23c27eead`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:30:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:30:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:30:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:30:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:31:57 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:32:38 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:16:07 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 20:18:44 GMT
RUN $url = 'https://dl.google.com/go/go1.16.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'd40139b7ade8a3008e3240a6f86fe8f899a9c465c917e11dac8758af216f5eb0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:18:46 GMT
WORKDIR C:\gopath
# Thu, 06 May 2021 21:02:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:02:30 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 00:22:36 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:22:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 00:23:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 May 2021 00:23:13 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac56922ba0ee0ac19bcae98f5fb4b7427d31ef3c709f27cfb2c785fd13a611c4`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1723430d5101a2d617d3dbf4bc2a121b3f4b4432105aa2941e1afab8f130b9`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f4dc6e9a77d69a3d172368f4ae471b31c588d6201c2386e4ac62fd83faa16`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea47861a9221a4f1e5750db237c619796c612756a5e75e2cb443b1731ae8a8`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4be4ebd8eabefdb01f27dafad85e65289b95ca15591c14304c7792db99b54b`  
		Last Modified: Wed, 14 Apr 2021 12:58:35 GMT  
		Size: 30.2 MB (30155601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f66ae3738a83ea41b428b49261d4522d57df1617fbd1aa362d93f1e2802643`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2108b314c24064a0c250f72017cc64b3bf68915655327728a267c98985a5ff7`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 324.6 KB (324649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa51985154dd0edd95ef4cc022400dc16b657c4a75cb3ade3675c58d316d0101`  
		Last Modified: Thu, 06 May 2021 20:34:43 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26942e7cec550ceca0e7b0ef319dc3f732731719adfc676869678adce06d1193`  
		Last Modified: Thu, 06 May 2021 20:35:15 GMT  
		Size: 139.4 MB (139382398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e6b3adacda0d1c5092f48a23fa73f5bb807876cf3dcf7fd71632b48d8b1987`  
		Last Modified: Thu, 06 May 2021 20:34:43 GMT  
		Size: 1.6 KB (1598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6d89568ee8ac19213ae2e66b14601f80c6dd3c4a1205da5fa55da7003cd3a0`  
		Last Modified: Thu, 06 May 2021 21:06:02 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0aa20834bcdb38f731b9f6528281005b29ae951a02ef46190bf1be1cab5946`  
		Last Modified: Thu, 06 May 2021 21:06:00 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada218f8f73674eea11444ee4fa8048f2cfd6e2bfc8f8c2bb4cc40954436b6b0`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815ac3cbadfa3d6463be2a02130f663d74e486df33a07b582def59fe66dd48b0`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da0a5d30891cb84455c6b13f7a6b778a19b3a271813ef7066eb0ba908192ee7`  
		Last Modified: Tue, 11 May 2021 00:27:20 GMT  
		Size: 1.7 MB (1738012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e2cb2540135f046b5adb4957a0f75118aeb15e30d46af750522a16e6f0cc2`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:78645def8ffaedba4067a39b9ea2318211900b0a00230c004ab61982f9d41958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `caddy:builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:1b2ba73c8dc7fce225f65c457524b3830589cf0fa3e9c62faa0c88b15c73c74f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5987368241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd19fd51f0fc365a83899a16ab9d8fb86585a512ff6cc33bd07e7af1bc5d89d4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:35:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:35:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:35:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:35:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:38:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:39:34 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:19:05 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 20:22:32 GMT
RUN $url = 'https://dl.google.com/go/go1.16.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'd40139b7ade8a3008e3240a6f86fe8f899a9c465c917e11dac8758af216f5eb0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:22:34 GMT
WORKDIR C:\gopath
# Thu, 06 May 2021 21:03:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:03:07 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 00:23:23 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:23:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 00:25:06 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 May 2021 00:25:08 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3360763b706a564d93471b21a342ebbda7e047567cf1cbee82dd592ad33e0c`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0f653700ac9b57cf3d694cc90107e3220fc678581d1e985219677733ce242`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59d82702c225a2ca8cd2a5476122f55d8619eae959c9cb8323b68d70a2ed19`  
		Last Modified: Wed, 14 Apr 2021 12:59:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62435cd2b7652fc97ef3dc1a8968446f3f6e95f0ff1d6dcb176a3f0c2b14c2f8`  
		Last Modified: Wed, 14 Apr 2021 12:59:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d78a3a3d6cb25f55dc9d9947f7449a14717e6b787e49571a837e72b79334cf`  
		Last Modified: Wed, 14 Apr 2021 12:59:41 GMT  
		Size: 30.8 MB (30752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b774a32e346c00e004abbbd7290530d0a3f3dfb11915be2b2fa73c402da6bdd`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d153061f2f0d8ef33f71c4b9afd90899e21556e320d7103a8a9fb544c1cb521`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 5.6 MB (5608025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c85bf3447935a123c186c94d58b02a7e89b566366ab0c7a20b57fbc9e453e1`  
		Last Modified: Thu, 06 May 2021 20:35:33 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7558c3fc6da1f41d9317a885b7d1d896986e9e4a81b6487a543b93ca372649cd`  
		Last Modified: Thu, 06 May 2021 20:36:08 GMT  
		Size: 149.1 MB (149112181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d97cea35310e2e19e356bf67efe44136adb4df53f744e6497511765af70f7e`  
		Last Modified: Thu, 06 May 2021 20:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5214a4bbf455290910bf5850bebdd3fdde0c4bf2616c2975a8a91b62cfe7a`  
		Last Modified: Thu, 06 May 2021 21:06:13 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f9311ef107812e0fc28e80ff17843a7d95e33d9b4311d0ff921022f5d199c3`  
		Last Modified: Thu, 06 May 2021 21:06:10 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b921e314d8bdd24486247a7d82137f437b1572bec858ea76813dc27e580670`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8450625dd9bbf2232b7a3d1cbce4d8795d03b140b1fb962bb6042b82a073633`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394074991c1e1b9a6750cf551fb9f7fe9eaffa1a25889bebcf0f35682cb69afe`  
		Last Modified: Tue, 11 May 2021 00:27:37 GMT  
		Size: 7.0 MB (6993409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5f2fa898b0d7f2684b17b889c9c68aa767c0a1f408e2e4eceb3374cdf48393`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:385a805019a00604cda677ecab3def2b1f0e99edf622e4bbd33a5d18cf8a55f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:latest` - linux; amd64

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

### `caddy:latest` - linux; arm variant v6

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

### `caddy:latest` - linux; arm variant v7

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

### `caddy:latest` - linux; arm64 variant v8

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

### `caddy:latest` - linux; ppc64le

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

### `caddy:latest` - linux; s390x

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

### `caddy:latest` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:dee876a8acfe0ad66efe5790b51e5ce47ee105518205c16c1e515107022ee466
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487145585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab04d82b7c1bbab4a4556a4ab389e58cf942f64806603d16b32d02b85377ddc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:15:27 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:15:28 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:16:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:16:04 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:16:06 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:16:07 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:16:08 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:16:10 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:16:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:16:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:16:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:16:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:16:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:16:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:16:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:16:21 GMT
EXPOSE 80
# Tue, 11 May 2021 00:16:22 GMT
EXPOSE 443
# Tue, 11 May 2021 00:16:24 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:16:51 GMT
RUN caddy version
# Tue, 11 May 2021 00:16:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a805066d9e28c5afaf71144648d2270f86d9d1dfbaa0da9a239607694e9315b6`  
		Last Modified: Tue, 11 May 2021 00:26:29 GMT  
		Size: 5.1 MB (5104734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbd0ec6de6085e7571da80b4408f11fada63d710eaf20b44c1ce63847f6455c`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1c04d9585e13e14d3ba056c3a17a8a23821f402c55d603f719fde9885fcc74`  
		Last Modified: Tue, 11 May 2021 00:26:31 GMT  
		Size: 11.9 MB (11930099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27b6dfe0db5cd7aad46afe881c42348361a2c19752cf5629eacb67967b8520`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41902606f9afaae6014164471bda32934d7f0304b3aaa65e2d7480497d85b0bc`  
		Last Modified: Tue, 11 May 2021 00:26:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9ff94e742183a75d4199b58723e286d55ecdd255b03a81ad9ec2b222c85fe1`  
		Last Modified: Tue, 11 May 2021 00:26:25 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1edf08b568698061ffae34580ddf83acab5de417993a30b8a209c919461e6a`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2873cb5c59a087bae99202d1b5f8e424378796848bf9f9f0576cb9e75da8011`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11858529cacdcdc2b7ff911a5df669b21b0efaa8c2fcbde324ccaf0a4a2d4d6`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b96fffb3765e29e3c670d5e14eb09f96a25c0222143cfac7d62c9fa6224896`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b40f5b20f6588f423dc4ba00206ef0b74da9619e96c8c26af206ea104cf85`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9116ab8bdbdeb3f51018f29b3c57d96ed1ebdff8866b0a503c7cb682741e5d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec28519386c9082afe64bc68c2e073b32a2287131bba90c6f56cc9315a638b04`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7649cdb04974c2bf32fa747aadcf57f6402a9c418e9e8f78ada74eae7aec3029`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9652bcbd02b47c702e6f2e8c374f7304cb91ba0186aede9c423104440004857d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33145d7abff94087dd683fd05403939e5aa91276d2693f6c5e8ca28641acd8e1`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a096c1bcb735f9b2cd6bf77eb582dd89b09a6cc75199dd35d65bd5cf6ad50e`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dde82b55b25477fe6eb7381cfdb3e48aa439cbd3f6352e033a85d124cecae7a`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67426815598f918caebff919df817435078c051338bebd944aafb6b25ef593f6`  
		Last Modified: Tue, 11 May 2021 00:26:20 GMT  
		Size: 331.3 KB (331282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf87ebb9031675a0e4407a36e79f274666df2a06d20c2452c1e0acec70fc60a6`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:b61efb630c29dfd10f857eed823207497fd9c94176f47243f48c641119c663d3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818059080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3940d8ab2b2d69a458bd9951c005b3703a5ac35754896cbfd380305f8dfe27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:18:49 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:18:50 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:20:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:20:40 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:20:42 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:20:43 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:20:45 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:20:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:20:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:20:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:20:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:20:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:20:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:20:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:20:56 GMT
EXPOSE 80
# Tue, 11 May 2021 00:20:58 GMT
EXPOSE 443
# Tue, 11 May 2021 00:20:59 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:22:14 GMT
RUN caddy version
# Tue, 11 May 2021 00:22:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc088e7513f9bd5e2261035715cd5f39aff459f086737be39631a5c03dd0bc9`  
		Last Modified: Tue, 11 May 2021 00:27:00 GMT  
		Size: 5.7 MB (5678806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a94477e69ebd7355bfc6230d3309aa20d4fda7d504dc34bd3b2adae7f5f2b4`  
		Last Modified: Tue, 11 May 2021 00:26:57 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db416be1d5a7c97652523c359440855c0ef2127ac11cb08595aa068d99d8a5`  
		Last Modified: Tue, 11 May 2021 00:27:03 GMT  
		Size: 17.2 MB (17201492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e500af558c7988b44d7fae2a1a8c1d4498cb130d1de721a37712c33f09147a`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87b8476ce7fba27f66c08050c4a692f8a19ec0c84e9d42537b4b4b8bbb5f56e`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2d6240d48682965790d983fc3f6b5404aeb7f3f023b517ab83b6e47c20af5c`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757d21ff239a36a372b7fb98d22d42afd8f3c779c7b342605186d6b2a14925e7`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5e64a8fa017a3b5df9f60508bc7b3f72fe2835f00c086648f26235c9358b14`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac63d4edb89dc9920755d7e04e444610a75ac1268b103c178ebff146f490d73`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fbb5cca77bbd06aabe9371bf1fe894938b82367a0ef11be873b231a43b64ab`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b0ecb05ae3d1fffc947acf96dea7fe481fd9a745d4fcf79bff9f4b21a28817`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f292068b665f33bccf70f8100aa252145e0f63abb2283fa29d36cadcc6291c52`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1995472761eea00392fa2ce2d1566a7233a89a019e939892cbb0aeb4a8a3a07a`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e8f37215e61d4f10f002f5ad82c4acadf4a56b559cf036050f33242bfe1e35`  
		Last Modified: Tue, 11 May 2021 00:26:49 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2f6fb7cf636418bada10647c66ee3b92246da967ebb611d58aad6725f5e2b`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271eda8ea06432cb0dae8fd93e8a85314e86201450cdbebf3efcbba2dbd4331`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a4da75f19907c0ee148b5369a63863a2752457cc31b02fe68779d83d56c1`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7013990e537c69857c80a4d6fb386f6d0f04e5a0a5ee5b12ed57c0e458fc8e`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b661b1f2a589a6717a5599a78cb0f3ef950c1a36bd411039dfd39afb20e901b`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 269.3 KB (269349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e686f1164cdcf35434a7d997c0c9ff058302aaade06ace7c5f8a2e4a718aa`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:817273f476c97d5eb6805ecb4f1d622dd1d1eb3fcf0b537151eec68e01df8fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:dee876a8acfe0ad66efe5790b51e5ce47ee105518205c16c1e515107022ee466
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487145585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab04d82b7c1bbab4a4556a4ab389e58cf942f64806603d16b32d02b85377ddc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:15:27 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:15:28 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:16:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:16:04 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:16:06 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:16:07 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:16:08 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:16:10 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:16:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:16:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:16:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:16:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:16:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:16:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:16:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:16:21 GMT
EXPOSE 80
# Tue, 11 May 2021 00:16:22 GMT
EXPOSE 443
# Tue, 11 May 2021 00:16:24 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:16:51 GMT
RUN caddy version
# Tue, 11 May 2021 00:16:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a805066d9e28c5afaf71144648d2270f86d9d1dfbaa0da9a239607694e9315b6`  
		Last Modified: Tue, 11 May 2021 00:26:29 GMT  
		Size: 5.1 MB (5104734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbd0ec6de6085e7571da80b4408f11fada63d710eaf20b44c1ce63847f6455c`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1c04d9585e13e14d3ba056c3a17a8a23821f402c55d603f719fde9885fcc74`  
		Last Modified: Tue, 11 May 2021 00:26:31 GMT  
		Size: 11.9 MB (11930099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27b6dfe0db5cd7aad46afe881c42348361a2c19752cf5629eacb67967b8520`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41902606f9afaae6014164471bda32934d7f0304b3aaa65e2d7480497d85b0bc`  
		Last Modified: Tue, 11 May 2021 00:26:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9ff94e742183a75d4199b58723e286d55ecdd255b03a81ad9ec2b222c85fe1`  
		Last Modified: Tue, 11 May 2021 00:26:25 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1edf08b568698061ffae34580ddf83acab5de417993a30b8a209c919461e6a`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2873cb5c59a087bae99202d1b5f8e424378796848bf9f9f0576cb9e75da8011`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11858529cacdcdc2b7ff911a5df669b21b0efaa8c2fcbde324ccaf0a4a2d4d6`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b96fffb3765e29e3c670d5e14eb09f96a25c0222143cfac7d62c9fa6224896`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b40f5b20f6588f423dc4ba00206ef0b74da9619e96c8c26af206ea104cf85`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9116ab8bdbdeb3f51018f29b3c57d96ed1ebdff8866b0a503c7cb682741e5d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec28519386c9082afe64bc68c2e073b32a2287131bba90c6f56cc9315a638b04`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7649cdb04974c2bf32fa747aadcf57f6402a9c418e9e8f78ada74eae7aec3029`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9652bcbd02b47c702e6f2e8c374f7304cb91ba0186aede9c423104440004857d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33145d7abff94087dd683fd05403939e5aa91276d2693f6c5e8ca28641acd8e1`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a096c1bcb735f9b2cd6bf77eb582dd89b09a6cc75199dd35d65bd5cf6ad50e`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dde82b55b25477fe6eb7381cfdb3e48aa439cbd3f6352e033a85d124cecae7a`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67426815598f918caebff919df817435078c051338bebd944aafb6b25ef593f6`  
		Last Modified: Tue, 11 May 2021 00:26:20 GMT  
		Size: 331.3 KB (331282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf87ebb9031675a0e4407a36e79f274666df2a06d20c2452c1e0acec70fc60a6`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:b61efb630c29dfd10f857eed823207497fd9c94176f47243f48c641119c663d3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818059080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3940d8ab2b2d69a458bd9951c005b3703a5ac35754896cbfd380305f8dfe27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:18:49 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:18:50 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:20:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:20:40 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:20:42 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:20:43 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:20:45 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:20:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:20:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:20:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:20:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:20:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:20:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:20:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:20:56 GMT
EXPOSE 80
# Tue, 11 May 2021 00:20:58 GMT
EXPOSE 443
# Tue, 11 May 2021 00:20:59 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:22:14 GMT
RUN caddy version
# Tue, 11 May 2021 00:22:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc088e7513f9bd5e2261035715cd5f39aff459f086737be39631a5c03dd0bc9`  
		Last Modified: Tue, 11 May 2021 00:27:00 GMT  
		Size: 5.7 MB (5678806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a94477e69ebd7355bfc6230d3309aa20d4fda7d504dc34bd3b2adae7f5f2b4`  
		Last Modified: Tue, 11 May 2021 00:26:57 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db416be1d5a7c97652523c359440855c0ef2127ac11cb08595aa068d99d8a5`  
		Last Modified: Tue, 11 May 2021 00:27:03 GMT  
		Size: 17.2 MB (17201492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e500af558c7988b44d7fae2a1a8c1d4498cb130d1de721a37712c33f09147a`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87b8476ce7fba27f66c08050c4a692f8a19ec0c84e9d42537b4b4b8bbb5f56e`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2d6240d48682965790d983fc3f6b5404aeb7f3f023b517ab83b6e47c20af5c`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757d21ff239a36a372b7fb98d22d42afd8f3c779c7b342605186d6b2a14925e7`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5e64a8fa017a3b5df9f60508bc7b3f72fe2835f00c086648f26235c9358b14`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac63d4edb89dc9920755d7e04e444610a75ac1268b103c178ebff146f490d73`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fbb5cca77bbd06aabe9371bf1fe894938b82367a0ef11be873b231a43b64ab`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b0ecb05ae3d1fffc947acf96dea7fe481fd9a745d4fcf79bff9f4b21a28817`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f292068b665f33bccf70f8100aa252145e0f63abb2283fa29d36cadcc6291c52`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1995472761eea00392fa2ce2d1566a7233a89a019e939892cbb0aeb4a8a3a07a`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e8f37215e61d4f10f002f5ad82c4acadf4a56b559cf036050f33242bfe1e35`  
		Last Modified: Tue, 11 May 2021 00:26:49 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2f6fb7cf636418bada10647c66ee3b92246da967ebb611d58aad6725f5e2b`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271eda8ea06432cb0dae8fd93e8a85314e86201450cdbebf3efcbba2dbd4331`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a4da75f19907c0ee148b5369a63863a2752457cc31b02fe68779d83d56c1`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7013990e537c69857c80a4d6fb386f6d0f04e5a0a5ee5b12ed57c0e458fc8e`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b661b1f2a589a6717a5599a78cb0f3ef950c1a36bd411039dfd39afb20e901b`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 269.3 KB (269349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e686f1164cdcf35434a7d997c0c9ff058302aaade06ace7c5f8a2e4a718aa`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:a72b70da0fa644b846c169807c236cbe93c8103aa45a3e172d7c9247d5ebc445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:dee876a8acfe0ad66efe5790b51e5ce47ee105518205c16c1e515107022ee466
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2487145585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab04d82b7c1bbab4a4556a4ab389e58cf942f64806603d16b32d02b85377ddc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:15:27 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:15:28 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:16:03 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:16:04 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:16:06 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:16:07 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:16:08 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:16:10 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:16:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:16:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:16:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:16:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:16:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:16:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:16:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:16:21 GMT
EXPOSE 80
# Tue, 11 May 2021 00:16:22 GMT
EXPOSE 443
# Tue, 11 May 2021 00:16:24 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:16:51 GMT
RUN caddy version
# Tue, 11 May 2021 00:16:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a805066d9e28c5afaf71144648d2270f86d9d1dfbaa0da9a239607694e9315b6`  
		Last Modified: Tue, 11 May 2021 00:26:29 GMT  
		Size: 5.1 MB (5104734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbd0ec6de6085e7571da80b4408f11fada63d710eaf20b44c1ce63847f6455c`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1c04d9585e13e14d3ba056c3a17a8a23821f402c55d603f719fde9885fcc74`  
		Last Modified: Tue, 11 May 2021 00:26:31 GMT  
		Size: 11.9 MB (11930099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27b6dfe0db5cd7aad46afe881c42348361a2c19752cf5629eacb67967b8520`  
		Last Modified: Tue, 11 May 2021 00:26:27 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41902606f9afaae6014164471bda32934d7f0304b3aaa65e2d7480497d85b0bc`  
		Last Modified: Tue, 11 May 2021 00:26:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9ff94e742183a75d4199b58723e286d55ecdd255b03a81ad9ec2b222c85fe1`  
		Last Modified: Tue, 11 May 2021 00:26:25 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1edf08b568698061ffae34580ddf83acab5de417993a30b8a209c919461e6a`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2873cb5c59a087bae99202d1b5f8e424378796848bf9f9f0576cb9e75da8011`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11858529cacdcdc2b7ff911a5df669b21b0efaa8c2fcbde324ccaf0a4a2d4d6`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b96fffb3765e29e3c670d5e14eb09f96a25c0222143cfac7d62c9fa6224896`  
		Last Modified: Tue, 11 May 2021 00:26:24 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b40f5b20f6588f423dc4ba00206ef0b74da9619e96c8c26af206ea104cf85`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9116ab8bdbdeb3f51018f29b3c57d96ed1ebdff8866b0a503c7cb682741e5d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec28519386c9082afe64bc68c2e073b32a2287131bba90c6f56cc9315a638b04`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7649cdb04974c2bf32fa747aadcf57f6402a9c418e9e8f78ada74eae7aec3029`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9652bcbd02b47c702e6f2e8c374f7304cb91ba0186aede9c423104440004857d`  
		Last Modified: Tue, 11 May 2021 00:26:22 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33145d7abff94087dd683fd05403939e5aa91276d2693f6c5e8ca28641acd8e1`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a096c1bcb735f9b2cd6bf77eb582dd89b09a6cc75199dd35d65bd5cf6ad50e`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dde82b55b25477fe6eb7381cfdb3e48aa439cbd3f6352e033a85d124cecae7a`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67426815598f918caebff919df817435078c051338bebd944aafb6b25ef593f6`  
		Last Modified: Tue, 11 May 2021 00:26:20 GMT  
		Size: 331.3 KB (331282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf87ebb9031675a0e4407a36e79f274666df2a06d20c2452c1e0acec70fc60a6`  
		Last Modified: Tue, 11 May 2021 00:26:19 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:54f2ce6cefa5785e781847e6fe0fbe6ce716fb6c5bc0de5a49b4cb71cc8f1cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4350; amd64

### `caddy:windowsservercore-ltsc2016` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:b61efb630c29dfd10f857eed823207497fd9c94176f47243f48c641119c663d3
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5818059080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3940d8ab2b2d69a458bd9951c005b3703a5ac35754896cbfd380305f8dfe27`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 May 2021 00:18:49 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Tue, 11 May 2021 00:18:50 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:20:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.0/caddy_2.4.0_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('66c1f96e5ceb44aec53727ec02bbbb52eb58b4a41ac1134c5635693f40aa81cc4fa8e5418fdf712c8aa9c710aa0b19d6f52c0b46c6af54b4c79ca602e599694a')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Tue, 11 May 2021 00:20:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Tue, 11 May 2021 00:20:40 GMT
ENV XDG_DATA_HOME=c:/data
# Tue, 11 May 2021 00:20:42 GMT
VOLUME [c:/config]
# Tue, 11 May 2021 00:20:43 GMT
VOLUME [c:/data]
# Tue, 11 May 2021 00:20:45 GMT
LABEL org.opencontainers.image.version=v2.4.0
# Tue, 11 May 2021 00:20:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 11 May 2021 00:20:47 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 11 May 2021 00:20:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 11 May 2021 00:20:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 11 May 2021 00:20:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 11 May 2021 00:20:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 May 2021 00:20:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 11 May 2021 00:20:56 GMT
EXPOSE 80
# Tue, 11 May 2021 00:20:58 GMT
EXPOSE 443
# Tue, 11 May 2021 00:20:59 GMT
EXPOSE 2019
# Tue, 11 May 2021 00:22:14 GMT
RUN caddy version
# Tue, 11 May 2021 00:22:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc088e7513f9bd5e2261035715cd5f39aff459f086737be39631a5c03dd0bc9`  
		Last Modified: Tue, 11 May 2021 00:27:00 GMT  
		Size: 5.7 MB (5678806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a94477e69ebd7355bfc6230d3309aa20d4fda7d504dc34bd3b2adae7f5f2b4`  
		Last Modified: Tue, 11 May 2021 00:26:57 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db416be1d5a7c97652523c359440855c0ef2127ac11cb08595aa068d99d8a5`  
		Last Modified: Tue, 11 May 2021 00:27:03 GMT  
		Size: 17.2 MB (17201492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e500af558c7988b44d7fae2a1a8c1d4498cb130d1de721a37712c33f09147a`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87b8476ce7fba27f66c08050c4a692f8a19ec0c84e9d42537b4b4b8bbb5f56e`  
		Last Modified: Tue, 11 May 2021 00:26:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2d6240d48682965790d983fc3f6b5404aeb7f3f023b517ab83b6e47c20af5c`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757d21ff239a36a372b7fb98d22d42afd8f3c779c7b342605186d6b2a14925e7`  
		Last Modified: Tue, 11 May 2021 00:26:53 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5e64a8fa017a3b5df9f60508bc7b3f72fe2835f00c086648f26235c9358b14`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac63d4edb89dc9920755d7e04e444610a75ac1268b103c178ebff146f490d73`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fbb5cca77bbd06aabe9371bf1fe894938b82367a0ef11be873b231a43b64ab`  
		Last Modified: Tue, 11 May 2021 00:26:52 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b0ecb05ae3d1fffc947acf96dea7fe481fd9a745d4fcf79bff9f4b21a28817`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f292068b665f33bccf70f8100aa252145e0f63abb2283fa29d36cadcc6291c52`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1995472761eea00392fa2ce2d1566a7233a89a019e939892cbb0aeb4a8a3a07a`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e8f37215e61d4f10f002f5ad82c4acadf4a56b559cf036050f33242bfe1e35`  
		Last Modified: Tue, 11 May 2021 00:26:49 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2f6fb7cf636418bada10647c66ee3b92246da967ebb611d58aad6725f5e2b`  
		Last Modified: Tue, 11 May 2021 00:26:50 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271eda8ea06432cb0dae8fd93e8a85314e86201450cdbebf3efcbba2dbd4331`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a4da75f19907c0ee148b5369a63863a2752457cc31b02fe68779d83d56c1`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7013990e537c69857c80a4d6fb386f6d0f04e5a0a5ee5b12ed57c0e458fc8e`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b661b1f2a589a6717a5599a78cb0f3ef950c1a36bd411039dfd39afb20e901b`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 269.3 KB (269349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e686f1164cdcf35434a7d997c0c9ff058302aaade06ace7c5f8a2e4a718aa`  
		Last Modified: Tue, 11 May 2021 00:26:47 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
