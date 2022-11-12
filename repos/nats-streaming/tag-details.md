<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats-streaming`

-	[`nats-streaming:0.25`](#nats-streaming025)
-	[`nats-streaming:0.25-alpine`](#nats-streaming025-alpine)
-	[`nats-streaming:0.25-alpine3.16`](#nats-streaming025-alpine316)
-	[`nats-streaming:0.25-linux`](#nats-streaming025-linux)
-	[`nats-streaming:0.25-nanoserver`](#nats-streaming025-nanoserver)
-	[`nats-streaming:0.25-nanoserver-1809`](#nats-streaming025-nanoserver-1809)
-	[`nats-streaming:0.25-scratch`](#nats-streaming025-scratch)
-	[`nats-streaming:0.25-windowsservercore`](#nats-streaming025-windowsservercore)
-	[`nats-streaming:0.25-windowsservercore-1809`](#nats-streaming025-windowsservercore-1809)
-	[`nats-streaming:0.25.2`](#nats-streaming0252)
-	[`nats-streaming:0.25.2-alpine`](#nats-streaming0252-alpine)
-	[`nats-streaming:0.25.2-alpine3.16`](#nats-streaming0252-alpine316)
-	[`nats-streaming:0.25.2-linux`](#nats-streaming0252-linux)
-	[`nats-streaming:0.25.2-nanoserver`](#nats-streaming0252-nanoserver)
-	[`nats-streaming:0.25.2-nanoserver-1809`](#nats-streaming0252-nanoserver-1809)
-	[`nats-streaming:0.25.2-scratch`](#nats-streaming0252-scratch)
-	[`nats-streaming:0.25.2-windowsservercore`](#nats-streaming0252-windowsservercore)
-	[`nats-streaming:0.25.2-windowsservercore-1809`](#nats-streaming0252-windowsservercore-1809)
-	[`nats-streaming:alpine`](#nats-streamingalpine)
-	[`nats-streaming:alpine3.16`](#nats-streamingalpine316)
-	[`nats-streaming:latest`](#nats-streaminglatest)
-	[`nats-streaming:linux`](#nats-streaminglinux)
-	[`nats-streaming:nanoserver`](#nats-streamingnanoserver)
-	[`nats-streaming:nanoserver-1809`](#nats-streamingnanoserver-1809)
-	[`nats-streaming:scratch`](#nats-streamingscratch)
-	[`nats-streaming:windowsservercore`](#nats-streamingwindowsservercore)
-	[`nats-streaming:windowsservercore-1809`](#nats-streamingwindowsservercore-1809)

## `nats-streaming:0.25`

```console
$ docker pull nats-streaming@sha256:053a9fea38f67d1360c7e9b80ccf85f0539c78fc8a8d916fec83f6316422ca3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3650; amd64

### `nats-streaming:0.25` - linux; amd64

```console
$ docker pull nats-streaming@sha256:287d05564c4c6750f56fdda41f05e552d88ddf386a6e44e1cc834e0a65c0eb49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7637811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f455b7760d72d079088195f9cc0441f3fe22e1b46ecc2b8f49b3cda5ec483adf`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 11 Oct 2022 23:20:21 GMT
COPY file:89087473017a2e985e9741a8aa3ec73c208da928bb57f2f24e30c00a31eafa8a in /nats-streaming-server 
# Tue, 11 Oct 2022 23:20:21 GMT
EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:20:21 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 11 Oct 2022 23:20:21 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:66e24392f842ad35144e78bc3adad500757ab527859ee38957e527487ef8b47a`  
		Last Modified: Tue, 11 Oct 2022 23:21:01 GMT  
		Size: 7.6 MB (7637811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7a9e727242f052ad7f1aef67b29982a8d3f8bd6ea7e8cc8c76f3c7d2b044c667
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7300810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fad641972f0ff8f1dab2e34dca1f8e4011c5d32c7607c5bff6949a6a86d90b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 11:34:26 GMT
COPY file:f7568230fc06888b50a5f3da0004bb7dc7a70b1defec143315a57570b4b91602 in /nats-streaming-server 
# Fri, 11 Nov 2022 11:34:26 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 11:34:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 11:34:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ac505d089b210f05398eb249b7f3065fef3921be727978b70df4c11955da8d8`  
		Last Modified: Tue, 11 Oct 2022 23:50:41 GMT  
		Size: 7.3 MB (7300810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:45afd9c11672161333d5775564d46f19d15ba48f4a1bbd188da2e79c5d7b4a07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7288898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8f3428876076d61520fde190b5fc4f479e3f80a5d6c914c210470635215bd6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 10 Nov 2022 21:12:17 GMT
COPY file:bf11e23254626a7629546dd0e7e134984e019132c260d1733b972d9775ff8160 in /nats-streaming-server 
# Thu, 10 Nov 2022 21:12:18 GMT
EXPOSE 4222 8222
# Thu, 10 Nov 2022 21:12:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 10 Nov 2022 21:12:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2d5acf820909de2ff213199833cde1d52214f332d026d6f0b3807d819e2f657d`  
		Last Modified: Wed, 12 Oct 2022 01:12:22 GMT  
		Size: 7.3 MB (7288898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bdfae072b67d1ab734914a443796e974f5a7d73caa19aa5ba1a7abb335155705
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6994195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e5a4af7852aeaf241bd9103b8dcf4f7a1e9bd382a49dcfadf25aa83a1c404a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 08:57:36 GMT
COPY file:215fac5233cbc7ee50e4033b703c84c22a4b219b4ab4c43d7317bc92b89f206c in /nats-streaming-server 
# Fri, 11 Nov 2022 08:57:36 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 08:57:36 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 08:57:36 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:921e27ff4fbea0ffa1980a0bb3e13d378b150d7a7167d0dae7a3efbdc4408e37`  
		Last Modified: Tue, 11 Oct 2022 23:41:25 GMT  
		Size: 7.0 MB (6994195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats-streaming@sha256:1f1e6264687708ba147bbd17d4d8c0dbe98259726ffc9bb6ea485fa585064a96
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114490570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9db05f817ddff2380c6c06c5f0710aafb45b503d2b38a4e3c8cf28e6ea5268`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Wed, 09 Nov 2022 16:47:43 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 18:20:03 GMT
RUN cmd /S /C #(nop) COPY file:8231e132ceae2f5beb184edb8fd6927d5df2cb8a2774f0cb9b809b1a9176fa02 in C:\nats-streaming-server.exe 
# Wed, 09 Nov 2022 18:20:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6708525607bc7a2985c6a423e6cb63d6175e3ad60d997873c4519fab371772fe`  
		Last Modified: Wed, 09 Nov 2022 16:48:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99f48e4ed4473a894a45d73f972fe18df0a98679b3c4301c3ef4c106a4c90fc`  
		Last Modified: Wed, 09 Nov 2022 18:20:52 GMT  
		Size: 7.8 MB (7762375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df1a9be4b1efdbcb89bb3b190b84cfbec9ab0eea4729cc2b7e3750a8e24df18`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de08e4620648f95dc56478f2e325a786fd136adf51e18bd16695a4ae85df6a2c`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69d1ba207c958d270c4c71a6ccc34821c6bf32eb74a6239578be3ef5209c824`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine`

```console
$ docker pull nats-streaming@sha256:e81914ab4fe7447eaa19609b3d97ef06705e727c3781f93123cc46682dff5278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:817810dde65bec1eddf00bb911b5b98c5cd4bf022348d3e0f89f161c46840da7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10727161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2559fccd4f8c32253c08492a5fe5845131c30326428dc5e5fce026196e9082f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:35:13 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 08:35:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 08:35:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 08:35:17 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 08:35:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:35:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecf7a1f53c2673094ef2477f3b0962290b95401bc815aa48e9168d95dcb4b25`  
		Last Modified: Sat, 12 Nov 2022 08:35:46 GMT  
		Size: 7.9 MB (7920469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d99aeab13b93df1ce70cbbefbd4432ca2dd64687d78a9503cbbd3ffbbaffea5`  
		Last Modified: Sat, 12 Nov 2022 08:35:44 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9a84378f6b3a668fedf7d1908766712692a0427b503266badbfab6df61a983a4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10199935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdb717a997ff33a2c27c4e733da6080a7f1e6a30a5b470972fd6b5c6de78af9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:31:01 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 08:31:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 08:31:04 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 08:31:04 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 08:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:31:05 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a7266d1a66f2ea5b801d7764a52c8ee1d5693f9a6476b22dc66f3d99b171a7`  
		Last Modified: Sat, 12 Nov 2022 08:32:07 GMT  
		Size: 7.6 MB (7584409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628b93aaed041cd2ed4718e5e62302bf5ab47b44d537da490b4fa040ee70e1b`  
		Last Modified: Sat, 12 Nov 2022 08:32:06 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b2b3ec423704edec471faf6d4c57d892812027757fb8c4aa97255537a70004fd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9995817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc32f0df9620c827713e111965cf77d4bd6eff53fe4a56562d4534d8351f552a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 16:04:11 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 16:04:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 16:04:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 16:04:14 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 16:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 16:04:14 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180214698f74077e0eb6b8658703ee6ae21d61b258f469176c194359241e8b41`  
		Last Modified: Sat, 12 Nov 2022 16:05:19 GMT  
		Size: 7.6 MB (7576609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4021d0b15354056e35afae8cd207d047215bb1ea39c0ca58f51e1d19240b2420`  
		Last Modified: Sat, 12 Nov 2022 16:05:17 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ca778943e5f90ed98acff12f9648ae2c3a21578623afef9bfebf2a79b49f8404
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc0a84c9f36fd674923539f491f501c0d857b0223c3c3c56cac515342227db3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:35:47 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 04:35:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 04:35:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 04:35:50 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 04:35:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 04:35:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63798248065feda710b4713523655c77febcbb996582363fe8c7f3409f4ff5f6`  
		Last Modified: Sat, 12 Nov 2022 04:36:20 GMT  
		Size: 7.3 MB (7277445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e07236f67dbbb6a2886398ef3bcbccf3a5872498eec2846d9e1daea137bc54f`  
		Last Modified: Sat, 12 Nov 2022 04:36:18 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine3.16`

```console
$ docker pull nats-streaming@sha256:e81914ab4fe7447eaa19609b3d97ef06705e727c3781f93123cc46682dff5278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-alpine3.16` - linux; amd64

```console
$ docker pull nats-streaming@sha256:817810dde65bec1eddf00bb911b5b98c5cd4bf022348d3e0f89f161c46840da7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10727161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2559fccd4f8c32253c08492a5fe5845131c30326428dc5e5fce026196e9082f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:35:13 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 08:35:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 08:35:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 08:35:17 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 08:35:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:35:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecf7a1f53c2673094ef2477f3b0962290b95401bc815aa48e9168d95dcb4b25`  
		Last Modified: Sat, 12 Nov 2022 08:35:46 GMT  
		Size: 7.9 MB (7920469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d99aeab13b93df1ce70cbbefbd4432ca2dd64687d78a9503cbbd3ffbbaffea5`  
		Last Modified: Sat, 12 Nov 2022 08:35:44 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine3.16` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9a84378f6b3a668fedf7d1908766712692a0427b503266badbfab6df61a983a4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10199935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdb717a997ff33a2c27c4e733da6080a7f1e6a30a5b470972fd6b5c6de78af9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:31:01 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 08:31:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 08:31:04 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 08:31:04 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 08:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:31:05 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a7266d1a66f2ea5b801d7764a52c8ee1d5693f9a6476b22dc66f3d99b171a7`  
		Last Modified: Sat, 12 Nov 2022 08:32:07 GMT  
		Size: 7.6 MB (7584409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628b93aaed041cd2ed4718e5e62302bf5ab47b44d537da490b4fa040ee70e1b`  
		Last Modified: Sat, 12 Nov 2022 08:32:06 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine3.16` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b2b3ec423704edec471faf6d4c57d892812027757fb8c4aa97255537a70004fd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9995817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc32f0df9620c827713e111965cf77d4bd6eff53fe4a56562d4534d8351f552a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 16:04:11 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 16:04:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 16:04:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 16:04:14 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 16:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 16:04:14 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180214698f74077e0eb6b8658703ee6ae21d61b258f469176c194359241e8b41`  
		Last Modified: Sat, 12 Nov 2022 16:05:19 GMT  
		Size: 7.6 MB (7576609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4021d0b15354056e35afae8cd207d047215bb1ea39c0ca58f51e1d19240b2420`  
		Last Modified: Sat, 12 Nov 2022 16:05:17 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ca778943e5f90ed98acff12f9648ae2c3a21578623afef9bfebf2a79b49f8404
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc0a84c9f36fd674923539f491f501c0d857b0223c3c3c56cac515342227db3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:35:47 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 04:35:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 04:35:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 04:35:50 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 04:35:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 04:35:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63798248065feda710b4713523655c77febcbb996582363fe8c7f3409f4ff5f6`  
		Last Modified: Sat, 12 Nov 2022 04:36:20 GMT  
		Size: 7.3 MB (7277445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e07236f67dbbb6a2886398ef3bcbccf3a5872498eec2846d9e1daea137bc54f`  
		Last Modified: Sat, 12 Nov 2022 04:36:18 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-linux`

```console
$ docker pull nats-streaming@sha256:4ddb50b6f43dfb76ba44400dac36a4998155db22c3fa4b7ae513a65e6afda1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:287d05564c4c6750f56fdda41f05e552d88ddf386a6e44e1cc834e0a65c0eb49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7637811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f455b7760d72d079088195f9cc0441f3fe22e1b46ecc2b8f49b3cda5ec483adf`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 11 Oct 2022 23:20:21 GMT
COPY file:89087473017a2e985e9741a8aa3ec73c208da928bb57f2f24e30c00a31eafa8a in /nats-streaming-server 
# Tue, 11 Oct 2022 23:20:21 GMT
EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:20:21 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 11 Oct 2022 23:20:21 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:66e24392f842ad35144e78bc3adad500757ab527859ee38957e527487ef8b47a`  
		Last Modified: Tue, 11 Oct 2022 23:21:01 GMT  
		Size: 7.6 MB (7637811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7a9e727242f052ad7f1aef67b29982a8d3f8bd6ea7e8cc8c76f3c7d2b044c667
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7300810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fad641972f0ff8f1dab2e34dca1f8e4011c5d32c7607c5bff6949a6a86d90b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 11:34:26 GMT
COPY file:f7568230fc06888b50a5f3da0004bb7dc7a70b1defec143315a57570b4b91602 in /nats-streaming-server 
# Fri, 11 Nov 2022 11:34:26 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 11:34:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 11:34:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ac505d089b210f05398eb249b7f3065fef3921be727978b70df4c11955da8d8`  
		Last Modified: Tue, 11 Oct 2022 23:50:41 GMT  
		Size: 7.3 MB (7300810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:45afd9c11672161333d5775564d46f19d15ba48f4a1bbd188da2e79c5d7b4a07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7288898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8f3428876076d61520fde190b5fc4f479e3f80a5d6c914c210470635215bd6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 10 Nov 2022 21:12:17 GMT
COPY file:bf11e23254626a7629546dd0e7e134984e019132c260d1733b972d9775ff8160 in /nats-streaming-server 
# Thu, 10 Nov 2022 21:12:18 GMT
EXPOSE 4222 8222
# Thu, 10 Nov 2022 21:12:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 10 Nov 2022 21:12:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2d5acf820909de2ff213199833cde1d52214f332d026d6f0b3807d819e2f657d`  
		Last Modified: Wed, 12 Oct 2022 01:12:22 GMT  
		Size: 7.3 MB (7288898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bdfae072b67d1ab734914a443796e974f5a7d73caa19aa5ba1a7abb335155705
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6994195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e5a4af7852aeaf241bd9103b8dcf4f7a1e9bd382a49dcfadf25aa83a1c404a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 08:57:36 GMT
COPY file:215fac5233cbc7ee50e4033b703c84c22a4b219b4ab4c43d7317bc92b89f206c in /nats-streaming-server 
# Fri, 11 Nov 2022 08:57:36 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 08:57:36 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 08:57:36 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:921e27ff4fbea0ffa1980a0bb3e13d378b150d7a7167d0dae7a3efbdc4408e37`  
		Last Modified: Tue, 11 Oct 2022 23:41:25 GMT  
		Size: 7.0 MB (6994195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver`

```console
$ docker pull nats-streaming@sha256:b33b9d9cf97a3d87b8b1247410c6fa1c444f8b5713ac91bfc1c4c812186ee7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `nats-streaming:0.25-nanoserver` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats-streaming@sha256:1f1e6264687708ba147bbd17d4d8c0dbe98259726ffc9bb6ea485fa585064a96
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114490570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9db05f817ddff2380c6c06c5f0710aafb45b503d2b38a4e3c8cf28e6ea5268`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Wed, 09 Nov 2022 16:47:43 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 18:20:03 GMT
RUN cmd /S /C #(nop) COPY file:8231e132ceae2f5beb184edb8fd6927d5df2cb8a2774f0cb9b809b1a9176fa02 in C:\nats-streaming-server.exe 
# Wed, 09 Nov 2022 18:20:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6708525607bc7a2985c6a423e6cb63d6175e3ad60d997873c4519fab371772fe`  
		Last Modified: Wed, 09 Nov 2022 16:48:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99f48e4ed4473a894a45d73f972fe18df0a98679b3c4301c3ef4c106a4c90fc`  
		Last Modified: Wed, 09 Nov 2022 18:20:52 GMT  
		Size: 7.8 MB (7762375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df1a9be4b1efdbcb89bb3b190b84cfbec9ab0eea4729cc2b7e3750a8e24df18`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de08e4620648f95dc56478f2e325a786fd136adf51e18bd16695a4ae85df6a2c`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69d1ba207c958d270c4c71a6ccc34821c6bf32eb74a6239578be3ef5209c824`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:b33b9d9cf97a3d87b8b1247410c6fa1c444f8b5713ac91bfc1c4c812186ee7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `nats-streaming:0.25-nanoserver-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats-streaming@sha256:1f1e6264687708ba147bbd17d4d8c0dbe98259726ffc9bb6ea485fa585064a96
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114490570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9db05f817ddff2380c6c06c5f0710aafb45b503d2b38a4e3c8cf28e6ea5268`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Wed, 09 Nov 2022 16:47:43 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 18:20:03 GMT
RUN cmd /S /C #(nop) COPY file:8231e132ceae2f5beb184edb8fd6927d5df2cb8a2774f0cb9b809b1a9176fa02 in C:\nats-streaming-server.exe 
# Wed, 09 Nov 2022 18:20:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6708525607bc7a2985c6a423e6cb63d6175e3ad60d997873c4519fab371772fe`  
		Last Modified: Wed, 09 Nov 2022 16:48:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99f48e4ed4473a894a45d73f972fe18df0a98679b3c4301c3ef4c106a4c90fc`  
		Last Modified: Wed, 09 Nov 2022 18:20:52 GMT  
		Size: 7.8 MB (7762375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df1a9be4b1efdbcb89bb3b190b84cfbec9ab0eea4729cc2b7e3750a8e24df18`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de08e4620648f95dc56478f2e325a786fd136adf51e18bd16695a4ae85df6a2c`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69d1ba207c958d270c4c71a6ccc34821c6bf32eb74a6239578be3ef5209c824`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-scratch`

```console
$ docker pull nats-streaming@sha256:4ddb50b6f43dfb76ba44400dac36a4998155db22c3fa4b7ae513a65e6afda1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:287d05564c4c6750f56fdda41f05e552d88ddf386a6e44e1cc834e0a65c0eb49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7637811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f455b7760d72d079088195f9cc0441f3fe22e1b46ecc2b8f49b3cda5ec483adf`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 11 Oct 2022 23:20:21 GMT
COPY file:89087473017a2e985e9741a8aa3ec73c208da928bb57f2f24e30c00a31eafa8a in /nats-streaming-server 
# Tue, 11 Oct 2022 23:20:21 GMT
EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:20:21 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 11 Oct 2022 23:20:21 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:66e24392f842ad35144e78bc3adad500757ab527859ee38957e527487ef8b47a`  
		Last Modified: Tue, 11 Oct 2022 23:21:01 GMT  
		Size: 7.6 MB (7637811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7a9e727242f052ad7f1aef67b29982a8d3f8bd6ea7e8cc8c76f3c7d2b044c667
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7300810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fad641972f0ff8f1dab2e34dca1f8e4011c5d32c7607c5bff6949a6a86d90b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 11:34:26 GMT
COPY file:f7568230fc06888b50a5f3da0004bb7dc7a70b1defec143315a57570b4b91602 in /nats-streaming-server 
# Fri, 11 Nov 2022 11:34:26 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 11:34:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 11:34:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ac505d089b210f05398eb249b7f3065fef3921be727978b70df4c11955da8d8`  
		Last Modified: Tue, 11 Oct 2022 23:50:41 GMT  
		Size: 7.3 MB (7300810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:45afd9c11672161333d5775564d46f19d15ba48f4a1bbd188da2e79c5d7b4a07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7288898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8f3428876076d61520fde190b5fc4f479e3f80a5d6c914c210470635215bd6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 10 Nov 2022 21:12:17 GMT
COPY file:bf11e23254626a7629546dd0e7e134984e019132c260d1733b972d9775ff8160 in /nats-streaming-server 
# Thu, 10 Nov 2022 21:12:18 GMT
EXPOSE 4222 8222
# Thu, 10 Nov 2022 21:12:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 10 Nov 2022 21:12:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2d5acf820909de2ff213199833cde1d52214f332d026d6f0b3807d819e2f657d`  
		Last Modified: Wed, 12 Oct 2022 01:12:22 GMT  
		Size: 7.3 MB (7288898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bdfae072b67d1ab734914a443796e974f5a7d73caa19aa5ba1a7abb335155705
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6994195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e5a4af7852aeaf241bd9103b8dcf4f7a1e9bd382a49dcfadf25aa83a1c404a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 08:57:36 GMT
COPY file:215fac5233cbc7ee50e4033b703c84c22a4b219b4ab4c43d7317bc92b89f206c in /nats-streaming-server 
# Fri, 11 Nov 2022 08:57:36 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 08:57:36 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 08:57:36 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:921e27ff4fbea0ffa1980a0bb3e13d378b150d7a7167d0dae7a3efbdc4408e37`  
		Last Modified: Tue, 11 Oct 2022 23:41:25 GMT  
		Size: 7.0 MB (6994195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore`

```console
$ docker pull nats-streaming@sha256:fc9f3a4493f401deed6acdcadaff40c596751f6fc9b5cd6fd3a5597e876c4841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `nats-streaming:0.25-windowsservercore` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats-streaming@sha256:e432cca2b1fb2af40ca299e80a02579387266d13a256bf7a23dfd7125a0ae4a1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2787076749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13f247cbd55632a872bae42021882364e6678b369692b701f6ebb8e9b0ddc4d`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Wed, 09 Nov 2022 14:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Nov 2022 16:44:45 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 18:16:17 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Wed, 09 Nov 2022 18:16:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.2/nats-streaming-server-v0.25.2-windows-amd64.zip
# Wed, 09 Nov 2022 18:16:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=554b083bb17f8f2e9a875b888dbe74454648f86c6e02bc489d88713431025d9d
# Wed, 09 Nov 2022 18:17:30 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Nov 2022 18:19:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Nov 2022 18:19:40 GMT
EXPOSE 4222 8222
# Wed, 09 Nov 2022 18:19:41 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Nov 2022 18:19:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99941fb33972e616b231a8aadd93463fdfd5de6aece4aa6c470d2feec31839be`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f3d8a87f0a1540850986ff94131286dfa42ca116f04779e02f60b3a724641b`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe863d992e0c58c9cf1632767e37ade6556903b1bb890c2a4dc02dffeaed78ef`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71a5994065b88d8a198293e12ac4530e9342de0f4d53860ee2743bd2d569013`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8e674abd79efbd197e128d166729af96bcf66ffb1646f10fb80dde56503f83`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec5f49fc868f6f3b72e2f76461f16e59f80e92a4186383b3baf71c06d3d2b21`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 359.2 KB (359194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0897e7aebc234f59c04916a3b53b2a9b5ac2bda1415cddcb71ddf1966d20bdfc`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 8.1 MB (8119591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ea295c4d678432a3afecc78785a990244c290159cc0851aa868efc70979b97`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a938d3ad7b90133750f1d10713db202d85b54f492cb2aef146e304f77b66f49`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b500e39240181724cbcb1a40781d36fae94a34eef9f926a5c612644211b67f`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:fc9f3a4493f401deed6acdcadaff40c596751f6fc9b5cd6fd3a5597e876c4841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `nats-streaming:0.25-windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats-streaming@sha256:e432cca2b1fb2af40ca299e80a02579387266d13a256bf7a23dfd7125a0ae4a1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2787076749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13f247cbd55632a872bae42021882364e6678b369692b701f6ebb8e9b0ddc4d`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Wed, 09 Nov 2022 14:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Nov 2022 16:44:45 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 18:16:17 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Wed, 09 Nov 2022 18:16:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.2/nats-streaming-server-v0.25.2-windows-amd64.zip
# Wed, 09 Nov 2022 18:16:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=554b083bb17f8f2e9a875b888dbe74454648f86c6e02bc489d88713431025d9d
# Wed, 09 Nov 2022 18:17:30 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Nov 2022 18:19:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Nov 2022 18:19:40 GMT
EXPOSE 4222 8222
# Wed, 09 Nov 2022 18:19:41 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Nov 2022 18:19:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99941fb33972e616b231a8aadd93463fdfd5de6aece4aa6c470d2feec31839be`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f3d8a87f0a1540850986ff94131286dfa42ca116f04779e02f60b3a724641b`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe863d992e0c58c9cf1632767e37ade6556903b1bb890c2a4dc02dffeaed78ef`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71a5994065b88d8a198293e12ac4530e9342de0f4d53860ee2743bd2d569013`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8e674abd79efbd197e128d166729af96bcf66ffb1646f10fb80dde56503f83`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec5f49fc868f6f3b72e2f76461f16e59f80e92a4186383b3baf71c06d3d2b21`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 359.2 KB (359194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0897e7aebc234f59c04916a3b53b2a9b5ac2bda1415cddcb71ddf1966d20bdfc`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 8.1 MB (8119591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ea295c4d678432a3afecc78785a990244c290159cc0851aa868efc70979b97`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a938d3ad7b90133750f1d10713db202d85b54f492cb2aef146e304f77b66f49`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b500e39240181724cbcb1a40781d36fae94a34eef9f926a5c612644211b67f`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.2`

```console
$ docker pull nats-streaming@sha256:053a9fea38f67d1360c7e9b80ccf85f0539c78fc8a8d916fec83f6316422ca3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3650; amd64

### `nats-streaming:0.25.2` - linux; amd64

```console
$ docker pull nats-streaming@sha256:287d05564c4c6750f56fdda41f05e552d88ddf386a6e44e1cc834e0a65c0eb49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7637811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f455b7760d72d079088195f9cc0441f3fe22e1b46ecc2b8f49b3cda5ec483adf`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 11 Oct 2022 23:20:21 GMT
COPY file:89087473017a2e985e9741a8aa3ec73c208da928bb57f2f24e30c00a31eafa8a in /nats-streaming-server 
# Tue, 11 Oct 2022 23:20:21 GMT
EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:20:21 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 11 Oct 2022 23:20:21 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:66e24392f842ad35144e78bc3adad500757ab527859ee38957e527487ef8b47a`  
		Last Modified: Tue, 11 Oct 2022 23:21:01 GMT  
		Size: 7.6 MB (7637811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.2` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7a9e727242f052ad7f1aef67b29982a8d3f8bd6ea7e8cc8c76f3c7d2b044c667
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7300810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fad641972f0ff8f1dab2e34dca1f8e4011c5d32c7607c5bff6949a6a86d90b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 11:34:26 GMT
COPY file:f7568230fc06888b50a5f3da0004bb7dc7a70b1defec143315a57570b4b91602 in /nats-streaming-server 
# Fri, 11 Nov 2022 11:34:26 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 11:34:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 11:34:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ac505d089b210f05398eb249b7f3065fef3921be727978b70df4c11955da8d8`  
		Last Modified: Tue, 11 Oct 2022 23:50:41 GMT  
		Size: 7.3 MB (7300810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.2` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:45afd9c11672161333d5775564d46f19d15ba48f4a1bbd188da2e79c5d7b4a07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7288898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8f3428876076d61520fde190b5fc4f479e3f80a5d6c914c210470635215bd6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 10 Nov 2022 21:12:17 GMT
COPY file:bf11e23254626a7629546dd0e7e134984e019132c260d1733b972d9775ff8160 in /nats-streaming-server 
# Thu, 10 Nov 2022 21:12:18 GMT
EXPOSE 4222 8222
# Thu, 10 Nov 2022 21:12:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 10 Nov 2022 21:12:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2d5acf820909de2ff213199833cde1d52214f332d026d6f0b3807d819e2f657d`  
		Last Modified: Wed, 12 Oct 2022 01:12:22 GMT  
		Size: 7.3 MB (7288898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.2` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bdfae072b67d1ab734914a443796e974f5a7d73caa19aa5ba1a7abb335155705
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6994195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e5a4af7852aeaf241bd9103b8dcf4f7a1e9bd382a49dcfadf25aa83a1c404a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 08:57:36 GMT
COPY file:215fac5233cbc7ee50e4033b703c84c22a4b219b4ab4c43d7317bc92b89f206c in /nats-streaming-server 
# Fri, 11 Nov 2022 08:57:36 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 08:57:36 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 08:57:36 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:921e27ff4fbea0ffa1980a0bb3e13d378b150d7a7167d0dae7a3efbdc4408e37`  
		Last Modified: Tue, 11 Oct 2022 23:41:25 GMT  
		Size: 7.0 MB (6994195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.2` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats-streaming@sha256:1f1e6264687708ba147bbd17d4d8c0dbe98259726ffc9bb6ea485fa585064a96
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114490570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9db05f817ddff2380c6c06c5f0710aafb45b503d2b38a4e3c8cf28e6ea5268`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Wed, 09 Nov 2022 16:47:43 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 18:20:03 GMT
RUN cmd /S /C #(nop) COPY file:8231e132ceae2f5beb184edb8fd6927d5df2cb8a2774f0cb9b809b1a9176fa02 in C:\nats-streaming-server.exe 
# Wed, 09 Nov 2022 18:20:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6708525607bc7a2985c6a423e6cb63d6175e3ad60d997873c4519fab371772fe`  
		Last Modified: Wed, 09 Nov 2022 16:48:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99f48e4ed4473a894a45d73f972fe18df0a98679b3c4301c3ef4c106a4c90fc`  
		Last Modified: Wed, 09 Nov 2022 18:20:52 GMT  
		Size: 7.8 MB (7762375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df1a9be4b1efdbcb89bb3b190b84cfbec9ab0eea4729cc2b7e3750a8e24df18`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de08e4620648f95dc56478f2e325a786fd136adf51e18bd16695a4ae85df6a2c`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69d1ba207c958d270c4c71a6ccc34821c6bf32eb74a6239578be3ef5209c824`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.2-alpine`

```console
$ docker pull nats-streaming@sha256:e81914ab4fe7447eaa19609b3d97ef06705e727c3781f93123cc46682dff5278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.2-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:817810dde65bec1eddf00bb911b5b98c5cd4bf022348d3e0f89f161c46840da7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10727161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2559fccd4f8c32253c08492a5fe5845131c30326428dc5e5fce026196e9082f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:35:13 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 08:35:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 08:35:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 08:35:17 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 08:35:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:35:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecf7a1f53c2673094ef2477f3b0962290b95401bc815aa48e9168d95dcb4b25`  
		Last Modified: Sat, 12 Nov 2022 08:35:46 GMT  
		Size: 7.9 MB (7920469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d99aeab13b93df1ce70cbbefbd4432ca2dd64687d78a9503cbbd3ffbbaffea5`  
		Last Modified: Sat, 12 Nov 2022 08:35:44 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.2-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9a84378f6b3a668fedf7d1908766712692a0427b503266badbfab6df61a983a4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10199935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdb717a997ff33a2c27c4e733da6080a7f1e6a30a5b470972fd6b5c6de78af9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:31:01 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 08:31:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 08:31:04 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 08:31:04 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 08:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:31:05 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a7266d1a66f2ea5b801d7764a52c8ee1d5693f9a6476b22dc66f3d99b171a7`  
		Last Modified: Sat, 12 Nov 2022 08:32:07 GMT  
		Size: 7.6 MB (7584409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628b93aaed041cd2ed4718e5e62302bf5ab47b44d537da490b4fa040ee70e1b`  
		Last Modified: Sat, 12 Nov 2022 08:32:06 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.2-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b2b3ec423704edec471faf6d4c57d892812027757fb8c4aa97255537a70004fd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9995817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc32f0df9620c827713e111965cf77d4bd6eff53fe4a56562d4534d8351f552a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 16:04:11 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 16:04:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 16:04:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 16:04:14 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 16:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 16:04:14 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180214698f74077e0eb6b8658703ee6ae21d61b258f469176c194359241e8b41`  
		Last Modified: Sat, 12 Nov 2022 16:05:19 GMT  
		Size: 7.6 MB (7576609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4021d0b15354056e35afae8cd207d047215bb1ea39c0ca58f51e1d19240b2420`  
		Last Modified: Sat, 12 Nov 2022 16:05:17 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ca778943e5f90ed98acff12f9648ae2c3a21578623afef9bfebf2a79b49f8404
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc0a84c9f36fd674923539f491f501c0d857b0223c3c3c56cac515342227db3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:35:47 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 04:35:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 04:35:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 04:35:50 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 04:35:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 04:35:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63798248065feda710b4713523655c77febcbb996582363fe8c7f3409f4ff5f6`  
		Last Modified: Sat, 12 Nov 2022 04:36:20 GMT  
		Size: 7.3 MB (7277445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e07236f67dbbb6a2886398ef3bcbccf3a5872498eec2846d9e1daea137bc54f`  
		Last Modified: Sat, 12 Nov 2022 04:36:18 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.2-alpine3.16`

```console
$ docker pull nats-streaming@sha256:e81914ab4fe7447eaa19609b3d97ef06705e727c3781f93123cc46682dff5278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.2-alpine3.16` - linux; amd64

```console
$ docker pull nats-streaming@sha256:817810dde65bec1eddf00bb911b5b98c5cd4bf022348d3e0f89f161c46840da7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10727161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2559fccd4f8c32253c08492a5fe5845131c30326428dc5e5fce026196e9082f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:35:13 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 08:35:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 08:35:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 08:35:17 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 08:35:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:35:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecf7a1f53c2673094ef2477f3b0962290b95401bc815aa48e9168d95dcb4b25`  
		Last Modified: Sat, 12 Nov 2022 08:35:46 GMT  
		Size: 7.9 MB (7920469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d99aeab13b93df1ce70cbbefbd4432ca2dd64687d78a9503cbbd3ffbbaffea5`  
		Last Modified: Sat, 12 Nov 2022 08:35:44 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.2-alpine3.16` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9a84378f6b3a668fedf7d1908766712692a0427b503266badbfab6df61a983a4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10199935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdb717a997ff33a2c27c4e733da6080a7f1e6a30a5b470972fd6b5c6de78af9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:31:01 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 08:31:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 08:31:04 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 08:31:04 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 08:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:31:05 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a7266d1a66f2ea5b801d7764a52c8ee1d5693f9a6476b22dc66f3d99b171a7`  
		Last Modified: Sat, 12 Nov 2022 08:32:07 GMT  
		Size: 7.6 MB (7584409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628b93aaed041cd2ed4718e5e62302bf5ab47b44d537da490b4fa040ee70e1b`  
		Last Modified: Sat, 12 Nov 2022 08:32:06 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.2-alpine3.16` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b2b3ec423704edec471faf6d4c57d892812027757fb8c4aa97255537a70004fd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9995817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc32f0df9620c827713e111965cf77d4bd6eff53fe4a56562d4534d8351f552a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 16:04:11 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 16:04:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 16:04:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 16:04:14 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 16:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 16:04:14 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180214698f74077e0eb6b8658703ee6ae21d61b258f469176c194359241e8b41`  
		Last Modified: Sat, 12 Nov 2022 16:05:19 GMT  
		Size: 7.6 MB (7576609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4021d0b15354056e35afae8cd207d047215bb1ea39c0ca58f51e1d19240b2420`  
		Last Modified: Sat, 12 Nov 2022 16:05:17 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.2-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ca778943e5f90ed98acff12f9648ae2c3a21578623afef9bfebf2a79b49f8404
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc0a84c9f36fd674923539f491f501c0d857b0223c3c3c56cac515342227db3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:35:47 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 04:35:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 04:35:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 04:35:50 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 04:35:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 04:35:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63798248065feda710b4713523655c77febcbb996582363fe8c7f3409f4ff5f6`  
		Last Modified: Sat, 12 Nov 2022 04:36:20 GMT  
		Size: 7.3 MB (7277445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e07236f67dbbb6a2886398ef3bcbccf3a5872498eec2846d9e1daea137bc54f`  
		Last Modified: Sat, 12 Nov 2022 04:36:18 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.2-linux`

```console
$ docker pull nats-streaming@sha256:4ddb50b6f43dfb76ba44400dac36a4998155db22c3fa4b7ae513a65e6afda1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.2-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:287d05564c4c6750f56fdda41f05e552d88ddf386a6e44e1cc834e0a65c0eb49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7637811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f455b7760d72d079088195f9cc0441f3fe22e1b46ecc2b8f49b3cda5ec483adf`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 11 Oct 2022 23:20:21 GMT
COPY file:89087473017a2e985e9741a8aa3ec73c208da928bb57f2f24e30c00a31eafa8a in /nats-streaming-server 
# Tue, 11 Oct 2022 23:20:21 GMT
EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:20:21 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 11 Oct 2022 23:20:21 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:66e24392f842ad35144e78bc3adad500757ab527859ee38957e527487ef8b47a`  
		Last Modified: Tue, 11 Oct 2022 23:21:01 GMT  
		Size: 7.6 MB (7637811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.2-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7a9e727242f052ad7f1aef67b29982a8d3f8bd6ea7e8cc8c76f3c7d2b044c667
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7300810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fad641972f0ff8f1dab2e34dca1f8e4011c5d32c7607c5bff6949a6a86d90b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 11:34:26 GMT
COPY file:f7568230fc06888b50a5f3da0004bb7dc7a70b1defec143315a57570b4b91602 in /nats-streaming-server 
# Fri, 11 Nov 2022 11:34:26 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 11:34:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 11:34:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ac505d089b210f05398eb249b7f3065fef3921be727978b70df4c11955da8d8`  
		Last Modified: Tue, 11 Oct 2022 23:50:41 GMT  
		Size: 7.3 MB (7300810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.2-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:45afd9c11672161333d5775564d46f19d15ba48f4a1bbd188da2e79c5d7b4a07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7288898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8f3428876076d61520fde190b5fc4f479e3f80a5d6c914c210470635215bd6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 10 Nov 2022 21:12:17 GMT
COPY file:bf11e23254626a7629546dd0e7e134984e019132c260d1733b972d9775ff8160 in /nats-streaming-server 
# Thu, 10 Nov 2022 21:12:18 GMT
EXPOSE 4222 8222
# Thu, 10 Nov 2022 21:12:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 10 Nov 2022 21:12:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2d5acf820909de2ff213199833cde1d52214f332d026d6f0b3807d819e2f657d`  
		Last Modified: Wed, 12 Oct 2022 01:12:22 GMT  
		Size: 7.3 MB (7288898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.2-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bdfae072b67d1ab734914a443796e974f5a7d73caa19aa5ba1a7abb335155705
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6994195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e5a4af7852aeaf241bd9103b8dcf4f7a1e9bd382a49dcfadf25aa83a1c404a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 08:57:36 GMT
COPY file:215fac5233cbc7ee50e4033b703c84c22a4b219b4ab4c43d7317bc92b89f206c in /nats-streaming-server 
# Fri, 11 Nov 2022 08:57:36 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 08:57:36 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 08:57:36 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:921e27ff4fbea0ffa1980a0bb3e13d378b150d7a7167d0dae7a3efbdc4408e37`  
		Last Modified: Tue, 11 Oct 2022 23:41:25 GMT  
		Size: 7.0 MB (6994195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.2-nanoserver`

```console
$ docker pull nats-streaming@sha256:b33b9d9cf97a3d87b8b1247410c6fa1c444f8b5713ac91bfc1c4c812186ee7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `nats-streaming:0.25.2-nanoserver` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats-streaming@sha256:1f1e6264687708ba147bbd17d4d8c0dbe98259726ffc9bb6ea485fa585064a96
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114490570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9db05f817ddff2380c6c06c5f0710aafb45b503d2b38a4e3c8cf28e6ea5268`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Wed, 09 Nov 2022 16:47:43 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 18:20:03 GMT
RUN cmd /S /C #(nop) COPY file:8231e132ceae2f5beb184edb8fd6927d5df2cb8a2774f0cb9b809b1a9176fa02 in C:\nats-streaming-server.exe 
# Wed, 09 Nov 2022 18:20:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6708525607bc7a2985c6a423e6cb63d6175e3ad60d997873c4519fab371772fe`  
		Last Modified: Wed, 09 Nov 2022 16:48:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99f48e4ed4473a894a45d73f972fe18df0a98679b3c4301c3ef4c106a4c90fc`  
		Last Modified: Wed, 09 Nov 2022 18:20:52 GMT  
		Size: 7.8 MB (7762375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df1a9be4b1efdbcb89bb3b190b84cfbec9ab0eea4729cc2b7e3750a8e24df18`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de08e4620648f95dc56478f2e325a786fd136adf51e18bd16695a4ae85df6a2c`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69d1ba207c958d270c4c71a6ccc34821c6bf32eb74a6239578be3ef5209c824`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.2-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:b33b9d9cf97a3d87b8b1247410c6fa1c444f8b5713ac91bfc1c4c812186ee7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `nats-streaming:0.25.2-nanoserver-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats-streaming@sha256:1f1e6264687708ba147bbd17d4d8c0dbe98259726ffc9bb6ea485fa585064a96
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114490570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9db05f817ddff2380c6c06c5f0710aafb45b503d2b38a4e3c8cf28e6ea5268`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Wed, 09 Nov 2022 16:47:43 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 18:20:03 GMT
RUN cmd /S /C #(nop) COPY file:8231e132ceae2f5beb184edb8fd6927d5df2cb8a2774f0cb9b809b1a9176fa02 in C:\nats-streaming-server.exe 
# Wed, 09 Nov 2022 18:20:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6708525607bc7a2985c6a423e6cb63d6175e3ad60d997873c4519fab371772fe`  
		Last Modified: Wed, 09 Nov 2022 16:48:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99f48e4ed4473a894a45d73f972fe18df0a98679b3c4301c3ef4c106a4c90fc`  
		Last Modified: Wed, 09 Nov 2022 18:20:52 GMT  
		Size: 7.8 MB (7762375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df1a9be4b1efdbcb89bb3b190b84cfbec9ab0eea4729cc2b7e3750a8e24df18`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de08e4620648f95dc56478f2e325a786fd136adf51e18bd16695a4ae85df6a2c`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69d1ba207c958d270c4c71a6ccc34821c6bf32eb74a6239578be3ef5209c824`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.2-scratch`

```console
$ docker pull nats-streaming@sha256:4ddb50b6f43dfb76ba44400dac36a4998155db22c3fa4b7ae513a65e6afda1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.2-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:287d05564c4c6750f56fdda41f05e552d88ddf386a6e44e1cc834e0a65c0eb49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7637811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f455b7760d72d079088195f9cc0441f3fe22e1b46ecc2b8f49b3cda5ec483adf`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 11 Oct 2022 23:20:21 GMT
COPY file:89087473017a2e985e9741a8aa3ec73c208da928bb57f2f24e30c00a31eafa8a in /nats-streaming-server 
# Tue, 11 Oct 2022 23:20:21 GMT
EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:20:21 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 11 Oct 2022 23:20:21 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:66e24392f842ad35144e78bc3adad500757ab527859ee38957e527487ef8b47a`  
		Last Modified: Tue, 11 Oct 2022 23:21:01 GMT  
		Size: 7.6 MB (7637811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.2-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7a9e727242f052ad7f1aef67b29982a8d3f8bd6ea7e8cc8c76f3c7d2b044c667
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7300810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fad641972f0ff8f1dab2e34dca1f8e4011c5d32c7607c5bff6949a6a86d90b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 11:34:26 GMT
COPY file:f7568230fc06888b50a5f3da0004bb7dc7a70b1defec143315a57570b4b91602 in /nats-streaming-server 
# Fri, 11 Nov 2022 11:34:26 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 11:34:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 11:34:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ac505d089b210f05398eb249b7f3065fef3921be727978b70df4c11955da8d8`  
		Last Modified: Tue, 11 Oct 2022 23:50:41 GMT  
		Size: 7.3 MB (7300810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.2-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:45afd9c11672161333d5775564d46f19d15ba48f4a1bbd188da2e79c5d7b4a07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7288898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8f3428876076d61520fde190b5fc4f479e3f80a5d6c914c210470635215bd6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 10 Nov 2022 21:12:17 GMT
COPY file:bf11e23254626a7629546dd0e7e134984e019132c260d1733b972d9775ff8160 in /nats-streaming-server 
# Thu, 10 Nov 2022 21:12:18 GMT
EXPOSE 4222 8222
# Thu, 10 Nov 2022 21:12:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 10 Nov 2022 21:12:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2d5acf820909de2ff213199833cde1d52214f332d026d6f0b3807d819e2f657d`  
		Last Modified: Wed, 12 Oct 2022 01:12:22 GMT  
		Size: 7.3 MB (7288898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bdfae072b67d1ab734914a443796e974f5a7d73caa19aa5ba1a7abb335155705
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6994195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e5a4af7852aeaf241bd9103b8dcf4f7a1e9bd382a49dcfadf25aa83a1c404a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 08:57:36 GMT
COPY file:215fac5233cbc7ee50e4033b703c84c22a4b219b4ab4c43d7317bc92b89f206c in /nats-streaming-server 
# Fri, 11 Nov 2022 08:57:36 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 08:57:36 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 08:57:36 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:921e27ff4fbea0ffa1980a0bb3e13d378b150d7a7167d0dae7a3efbdc4408e37`  
		Last Modified: Tue, 11 Oct 2022 23:41:25 GMT  
		Size: 7.0 MB (6994195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.2-windowsservercore`

```console
$ docker pull nats-streaming@sha256:fc9f3a4493f401deed6acdcadaff40c596751f6fc9b5cd6fd3a5597e876c4841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `nats-streaming:0.25.2-windowsservercore` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats-streaming@sha256:e432cca2b1fb2af40ca299e80a02579387266d13a256bf7a23dfd7125a0ae4a1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2787076749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13f247cbd55632a872bae42021882364e6678b369692b701f6ebb8e9b0ddc4d`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Wed, 09 Nov 2022 14:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Nov 2022 16:44:45 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 18:16:17 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Wed, 09 Nov 2022 18:16:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.2/nats-streaming-server-v0.25.2-windows-amd64.zip
# Wed, 09 Nov 2022 18:16:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=554b083bb17f8f2e9a875b888dbe74454648f86c6e02bc489d88713431025d9d
# Wed, 09 Nov 2022 18:17:30 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Nov 2022 18:19:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Nov 2022 18:19:40 GMT
EXPOSE 4222 8222
# Wed, 09 Nov 2022 18:19:41 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Nov 2022 18:19:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99941fb33972e616b231a8aadd93463fdfd5de6aece4aa6c470d2feec31839be`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f3d8a87f0a1540850986ff94131286dfa42ca116f04779e02f60b3a724641b`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe863d992e0c58c9cf1632767e37ade6556903b1bb890c2a4dc02dffeaed78ef`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71a5994065b88d8a198293e12ac4530e9342de0f4d53860ee2743bd2d569013`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8e674abd79efbd197e128d166729af96bcf66ffb1646f10fb80dde56503f83`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec5f49fc868f6f3b72e2f76461f16e59f80e92a4186383b3baf71c06d3d2b21`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 359.2 KB (359194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0897e7aebc234f59c04916a3b53b2a9b5ac2bda1415cddcb71ddf1966d20bdfc`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 8.1 MB (8119591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ea295c4d678432a3afecc78785a990244c290159cc0851aa868efc70979b97`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a938d3ad7b90133750f1d10713db202d85b54f492cb2aef146e304f77b66f49`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b500e39240181724cbcb1a40781d36fae94a34eef9f926a5c612644211b67f`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.2-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:fc9f3a4493f401deed6acdcadaff40c596751f6fc9b5cd6fd3a5597e876c4841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `nats-streaming:0.25.2-windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats-streaming@sha256:e432cca2b1fb2af40ca299e80a02579387266d13a256bf7a23dfd7125a0ae4a1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2787076749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13f247cbd55632a872bae42021882364e6678b369692b701f6ebb8e9b0ddc4d`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Wed, 09 Nov 2022 14:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Nov 2022 16:44:45 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 18:16:17 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Wed, 09 Nov 2022 18:16:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.2/nats-streaming-server-v0.25.2-windows-amd64.zip
# Wed, 09 Nov 2022 18:16:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=554b083bb17f8f2e9a875b888dbe74454648f86c6e02bc489d88713431025d9d
# Wed, 09 Nov 2022 18:17:30 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Nov 2022 18:19:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Nov 2022 18:19:40 GMT
EXPOSE 4222 8222
# Wed, 09 Nov 2022 18:19:41 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Nov 2022 18:19:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99941fb33972e616b231a8aadd93463fdfd5de6aece4aa6c470d2feec31839be`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f3d8a87f0a1540850986ff94131286dfa42ca116f04779e02f60b3a724641b`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe863d992e0c58c9cf1632767e37ade6556903b1bb890c2a4dc02dffeaed78ef`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71a5994065b88d8a198293e12ac4530e9342de0f4d53860ee2743bd2d569013`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8e674abd79efbd197e128d166729af96bcf66ffb1646f10fb80dde56503f83`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec5f49fc868f6f3b72e2f76461f16e59f80e92a4186383b3baf71c06d3d2b21`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 359.2 KB (359194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0897e7aebc234f59c04916a3b53b2a9b5ac2bda1415cddcb71ddf1966d20bdfc`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 8.1 MB (8119591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ea295c4d678432a3afecc78785a990244c290159cc0851aa868efc70979b97`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a938d3ad7b90133750f1d10713db202d85b54f492cb2aef146e304f77b66f49`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b500e39240181724cbcb1a40781d36fae94a34eef9f926a5c612644211b67f`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:e81914ab4fe7447eaa19609b3d97ef06705e727c3781f93123cc46682dff5278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:817810dde65bec1eddf00bb911b5b98c5cd4bf022348d3e0f89f161c46840da7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10727161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2559fccd4f8c32253c08492a5fe5845131c30326428dc5e5fce026196e9082f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:35:13 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 08:35:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 08:35:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 08:35:17 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 08:35:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:35:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecf7a1f53c2673094ef2477f3b0962290b95401bc815aa48e9168d95dcb4b25`  
		Last Modified: Sat, 12 Nov 2022 08:35:46 GMT  
		Size: 7.9 MB (7920469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d99aeab13b93df1ce70cbbefbd4432ca2dd64687d78a9503cbbd3ffbbaffea5`  
		Last Modified: Sat, 12 Nov 2022 08:35:44 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9a84378f6b3a668fedf7d1908766712692a0427b503266badbfab6df61a983a4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10199935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdb717a997ff33a2c27c4e733da6080a7f1e6a30a5b470972fd6b5c6de78af9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:31:01 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 08:31:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 08:31:04 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 08:31:04 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 08:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:31:05 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a7266d1a66f2ea5b801d7764a52c8ee1d5693f9a6476b22dc66f3d99b171a7`  
		Last Modified: Sat, 12 Nov 2022 08:32:07 GMT  
		Size: 7.6 MB (7584409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628b93aaed041cd2ed4718e5e62302bf5ab47b44d537da490b4fa040ee70e1b`  
		Last Modified: Sat, 12 Nov 2022 08:32:06 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b2b3ec423704edec471faf6d4c57d892812027757fb8c4aa97255537a70004fd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9995817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc32f0df9620c827713e111965cf77d4bd6eff53fe4a56562d4534d8351f552a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 16:04:11 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 16:04:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 16:04:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 16:04:14 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 16:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 16:04:14 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180214698f74077e0eb6b8658703ee6ae21d61b258f469176c194359241e8b41`  
		Last Modified: Sat, 12 Nov 2022 16:05:19 GMT  
		Size: 7.6 MB (7576609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4021d0b15354056e35afae8cd207d047215bb1ea39c0ca58f51e1d19240b2420`  
		Last Modified: Sat, 12 Nov 2022 16:05:17 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ca778943e5f90ed98acff12f9648ae2c3a21578623afef9bfebf2a79b49f8404
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc0a84c9f36fd674923539f491f501c0d857b0223c3c3c56cac515342227db3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:35:47 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 04:35:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 04:35:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 04:35:50 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 04:35:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 04:35:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63798248065feda710b4713523655c77febcbb996582363fe8c7f3409f4ff5f6`  
		Last Modified: Sat, 12 Nov 2022 04:36:20 GMT  
		Size: 7.3 MB (7277445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e07236f67dbbb6a2886398ef3bcbccf3a5872498eec2846d9e1daea137bc54f`  
		Last Modified: Sat, 12 Nov 2022 04:36:18 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.16`

```console
$ docker pull nats-streaming@sha256:e81914ab4fe7447eaa19609b3d97ef06705e727c3781f93123cc46682dff5278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.16` - linux; amd64

```console
$ docker pull nats-streaming@sha256:817810dde65bec1eddf00bb911b5b98c5cd4bf022348d3e0f89f161c46840da7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10727161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2559fccd4f8c32253c08492a5fe5845131c30326428dc5e5fce026196e9082f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:35:13 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 08:35:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 08:35:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 08:35:17 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 08:35:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:35:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecf7a1f53c2673094ef2477f3b0962290b95401bc815aa48e9168d95dcb4b25`  
		Last Modified: Sat, 12 Nov 2022 08:35:46 GMT  
		Size: 7.9 MB (7920469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d99aeab13b93df1ce70cbbefbd4432ca2dd64687d78a9503cbbd3ffbbaffea5`  
		Last Modified: Sat, 12 Nov 2022 08:35:44 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.16` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9a84378f6b3a668fedf7d1908766712692a0427b503266badbfab6df61a983a4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10199935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdb717a997ff33a2c27c4e733da6080a7f1e6a30a5b470972fd6b5c6de78af9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:31:01 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 08:31:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 08:31:04 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 08:31:04 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 08:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:31:05 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a7266d1a66f2ea5b801d7764a52c8ee1d5693f9a6476b22dc66f3d99b171a7`  
		Last Modified: Sat, 12 Nov 2022 08:32:07 GMT  
		Size: 7.6 MB (7584409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1628b93aaed041cd2ed4718e5e62302bf5ab47b44d537da490b4fa040ee70e1b`  
		Last Modified: Sat, 12 Nov 2022 08:32:06 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.16` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b2b3ec423704edec471faf6d4c57d892812027757fb8c4aa97255537a70004fd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9995817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc32f0df9620c827713e111965cf77d4bd6eff53fe4a56562d4534d8351f552a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 16:04:11 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 16:04:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 16:04:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 16:04:14 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 16:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 16:04:14 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180214698f74077e0eb6b8658703ee6ae21d61b258f469176c194359241e8b41`  
		Last Modified: Sat, 12 Nov 2022 16:05:19 GMT  
		Size: 7.6 MB (7576609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4021d0b15354056e35afae8cd207d047215bb1ea39c0ca58f51e1d19240b2420`  
		Last Modified: Sat, 12 Nov 2022 16:05:17 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:ca778943e5f90ed98acff12f9648ae2c3a21578623afef9bfebf2a79b49f8404
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc0a84c9f36fd674923539f491f501c0d857b0223c3c3c56cac515342227db3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:35:47 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Sat, 12 Nov 2022 04:35:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 12 Nov 2022 04:35:50 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 12 Nov 2022 04:35:50 GMT
EXPOSE 4222 8222
# Sat, 12 Nov 2022 04:35:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 04:35:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63798248065feda710b4713523655c77febcbb996582363fe8c7f3409f4ff5f6`  
		Last Modified: Sat, 12 Nov 2022 04:36:20 GMT  
		Size: 7.3 MB (7277445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e07236f67dbbb6a2886398ef3bcbccf3a5872498eec2846d9e1daea137bc54f`  
		Last Modified: Sat, 12 Nov 2022 04:36:18 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:053a9fea38f67d1360c7e9b80ccf85f0539c78fc8a8d916fec83f6316422ca3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3650; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:287d05564c4c6750f56fdda41f05e552d88ddf386a6e44e1cc834e0a65c0eb49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7637811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f455b7760d72d079088195f9cc0441f3fe22e1b46ecc2b8f49b3cda5ec483adf`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 11 Oct 2022 23:20:21 GMT
COPY file:89087473017a2e985e9741a8aa3ec73c208da928bb57f2f24e30c00a31eafa8a in /nats-streaming-server 
# Tue, 11 Oct 2022 23:20:21 GMT
EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:20:21 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 11 Oct 2022 23:20:21 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:66e24392f842ad35144e78bc3adad500757ab527859ee38957e527487ef8b47a`  
		Last Modified: Tue, 11 Oct 2022 23:21:01 GMT  
		Size: 7.6 MB (7637811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7a9e727242f052ad7f1aef67b29982a8d3f8bd6ea7e8cc8c76f3c7d2b044c667
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7300810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fad641972f0ff8f1dab2e34dca1f8e4011c5d32c7607c5bff6949a6a86d90b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 11:34:26 GMT
COPY file:f7568230fc06888b50a5f3da0004bb7dc7a70b1defec143315a57570b4b91602 in /nats-streaming-server 
# Fri, 11 Nov 2022 11:34:26 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 11:34:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 11:34:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ac505d089b210f05398eb249b7f3065fef3921be727978b70df4c11955da8d8`  
		Last Modified: Tue, 11 Oct 2022 23:50:41 GMT  
		Size: 7.3 MB (7300810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:45afd9c11672161333d5775564d46f19d15ba48f4a1bbd188da2e79c5d7b4a07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7288898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8f3428876076d61520fde190b5fc4f479e3f80a5d6c914c210470635215bd6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 10 Nov 2022 21:12:17 GMT
COPY file:bf11e23254626a7629546dd0e7e134984e019132c260d1733b972d9775ff8160 in /nats-streaming-server 
# Thu, 10 Nov 2022 21:12:18 GMT
EXPOSE 4222 8222
# Thu, 10 Nov 2022 21:12:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 10 Nov 2022 21:12:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2d5acf820909de2ff213199833cde1d52214f332d026d6f0b3807d819e2f657d`  
		Last Modified: Wed, 12 Oct 2022 01:12:22 GMT  
		Size: 7.3 MB (7288898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bdfae072b67d1ab734914a443796e974f5a7d73caa19aa5ba1a7abb335155705
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6994195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e5a4af7852aeaf241bd9103b8dcf4f7a1e9bd382a49dcfadf25aa83a1c404a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 08:57:36 GMT
COPY file:215fac5233cbc7ee50e4033b703c84c22a4b219b4ab4c43d7317bc92b89f206c in /nats-streaming-server 
# Fri, 11 Nov 2022 08:57:36 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 08:57:36 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 08:57:36 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:921e27ff4fbea0ffa1980a0bb3e13d378b150d7a7167d0dae7a3efbdc4408e37`  
		Last Modified: Tue, 11 Oct 2022 23:41:25 GMT  
		Size: 7.0 MB (6994195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats-streaming@sha256:1f1e6264687708ba147bbd17d4d8c0dbe98259726ffc9bb6ea485fa585064a96
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114490570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9db05f817ddff2380c6c06c5f0710aafb45b503d2b38a4e3c8cf28e6ea5268`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Wed, 09 Nov 2022 16:47:43 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 18:20:03 GMT
RUN cmd /S /C #(nop) COPY file:8231e132ceae2f5beb184edb8fd6927d5df2cb8a2774f0cb9b809b1a9176fa02 in C:\nats-streaming-server.exe 
# Wed, 09 Nov 2022 18:20:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6708525607bc7a2985c6a423e6cb63d6175e3ad60d997873c4519fab371772fe`  
		Last Modified: Wed, 09 Nov 2022 16:48:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99f48e4ed4473a894a45d73f972fe18df0a98679b3c4301c3ef4c106a4c90fc`  
		Last Modified: Wed, 09 Nov 2022 18:20:52 GMT  
		Size: 7.8 MB (7762375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df1a9be4b1efdbcb89bb3b190b84cfbec9ab0eea4729cc2b7e3750a8e24df18`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de08e4620648f95dc56478f2e325a786fd136adf51e18bd16695a4ae85df6a2c`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69d1ba207c958d270c4c71a6ccc34821c6bf32eb74a6239578be3ef5209c824`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:4ddb50b6f43dfb76ba44400dac36a4998155db22c3fa4b7ae513a65e6afda1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:287d05564c4c6750f56fdda41f05e552d88ddf386a6e44e1cc834e0a65c0eb49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7637811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f455b7760d72d079088195f9cc0441f3fe22e1b46ecc2b8f49b3cda5ec483adf`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 11 Oct 2022 23:20:21 GMT
COPY file:89087473017a2e985e9741a8aa3ec73c208da928bb57f2f24e30c00a31eafa8a in /nats-streaming-server 
# Tue, 11 Oct 2022 23:20:21 GMT
EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:20:21 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 11 Oct 2022 23:20:21 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:66e24392f842ad35144e78bc3adad500757ab527859ee38957e527487ef8b47a`  
		Last Modified: Tue, 11 Oct 2022 23:21:01 GMT  
		Size: 7.6 MB (7637811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7a9e727242f052ad7f1aef67b29982a8d3f8bd6ea7e8cc8c76f3c7d2b044c667
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7300810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fad641972f0ff8f1dab2e34dca1f8e4011c5d32c7607c5bff6949a6a86d90b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 11:34:26 GMT
COPY file:f7568230fc06888b50a5f3da0004bb7dc7a70b1defec143315a57570b4b91602 in /nats-streaming-server 
# Fri, 11 Nov 2022 11:34:26 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 11:34:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 11:34:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ac505d089b210f05398eb249b7f3065fef3921be727978b70df4c11955da8d8`  
		Last Modified: Tue, 11 Oct 2022 23:50:41 GMT  
		Size: 7.3 MB (7300810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:45afd9c11672161333d5775564d46f19d15ba48f4a1bbd188da2e79c5d7b4a07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7288898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8f3428876076d61520fde190b5fc4f479e3f80a5d6c914c210470635215bd6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 10 Nov 2022 21:12:17 GMT
COPY file:bf11e23254626a7629546dd0e7e134984e019132c260d1733b972d9775ff8160 in /nats-streaming-server 
# Thu, 10 Nov 2022 21:12:18 GMT
EXPOSE 4222 8222
# Thu, 10 Nov 2022 21:12:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 10 Nov 2022 21:12:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2d5acf820909de2ff213199833cde1d52214f332d026d6f0b3807d819e2f657d`  
		Last Modified: Wed, 12 Oct 2022 01:12:22 GMT  
		Size: 7.3 MB (7288898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bdfae072b67d1ab734914a443796e974f5a7d73caa19aa5ba1a7abb335155705
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6994195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e5a4af7852aeaf241bd9103b8dcf4f7a1e9bd382a49dcfadf25aa83a1c404a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 08:57:36 GMT
COPY file:215fac5233cbc7ee50e4033b703c84c22a4b219b4ab4c43d7317bc92b89f206c in /nats-streaming-server 
# Fri, 11 Nov 2022 08:57:36 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 08:57:36 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 08:57:36 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:921e27ff4fbea0ffa1980a0bb3e13d378b150d7a7167d0dae7a3efbdc4408e37`  
		Last Modified: Tue, 11 Oct 2022 23:41:25 GMT  
		Size: 7.0 MB (6994195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:b33b9d9cf97a3d87b8b1247410c6fa1c444f8b5713ac91bfc1c4c812186ee7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats-streaming@sha256:1f1e6264687708ba147bbd17d4d8c0dbe98259726ffc9bb6ea485fa585064a96
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114490570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9db05f817ddff2380c6c06c5f0710aafb45b503d2b38a4e3c8cf28e6ea5268`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Wed, 09 Nov 2022 16:47:43 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 18:20:03 GMT
RUN cmd /S /C #(nop) COPY file:8231e132ceae2f5beb184edb8fd6927d5df2cb8a2774f0cb9b809b1a9176fa02 in C:\nats-streaming-server.exe 
# Wed, 09 Nov 2022 18:20:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6708525607bc7a2985c6a423e6cb63d6175e3ad60d997873c4519fab371772fe`  
		Last Modified: Wed, 09 Nov 2022 16:48:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99f48e4ed4473a894a45d73f972fe18df0a98679b3c4301c3ef4c106a4c90fc`  
		Last Modified: Wed, 09 Nov 2022 18:20:52 GMT  
		Size: 7.8 MB (7762375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df1a9be4b1efdbcb89bb3b190b84cfbec9ab0eea4729cc2b7e3750a8e24df18`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de08e4620648f95dc56478f2e325a786fd136adf51e18bd16695a4ae85df6a2c`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69d1ba207c958d270c4c71a6ccc34821c6bf32eb74a6239578be3ef5209c824`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:b33b9d9cf97a3d87b8b1247410c6fa1c444f8b5713ac91bfc1c4c812186ee7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats-streaming@sha256:1f1e6264687708ba147bbd17d4d8c0dbe98259726ffc9bb6ea485fa585064a96
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114490570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9db05f817ddff2380c6c06c5f0710aafb45b503d2b38a4e3c8cf28e6ea5268`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Wed, 09 Nov 2022 16:47:43 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 18:20:03 GMT
RUN cmd /S /C #(nop) COPY file:8231e132ceae2f5beb184edb8fd6927d5df2cb8a2774f0cb9b809b1a9176fa02 in C:\nats-streaming-server.exe 
# Wed, 09 Nov 2022 18:20:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Nov 2022 18:20:05 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6708525607bc7a2985c6a423e6cb63d6175e3ad60d997873c4519fab371772fe`  
		Last Modified: Wed, 09 Nov 2022 16:48:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99f48e4ed4473a894a45d73f972fe18df0a98679b3c4301c3ef4c106a4c90fc`  
		Last Modified: Wed, 09 Nov 2022 18:20:52 GMT  
		Size: 7.8 MB (7762375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df1a9be4b1efdbcb89bb3b190b84cfbec9ab0eea4729cc2b7e3750a8e24df18`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de08e4620648f95dc56478f2e325a786fd136adf51e18bd16695a4ae85df6a2c`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69d1ba207c958d270c4c71a6ccc34821c6bf32eb74a6239578be3ef5209c824`  
		Last Modified: Wed, 09 Nov 2022 18:20:50 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:4ddb50b6f43dfb76ba44400dac36a4998155db22c3fa4b7ae513a65e6afda1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:287d05564c4c6750f56fdda41f05e552d88ddf386a6e44e1cc834e0a65c0eb49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7637811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f455b7760d72d079088195f9cc0441f3fe22e1b46ecc2b8f49b3cda5ec483adf`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 11 Oct 2022 23:20:21 GMT
COPY file:89087473017a2e985e9741a8aa3ec73c208da928bb57f2f24e30c00a31eafa8a in /nats-streaming-server 
# Tue, 11 Oct 2022 23:20:21 GMT
EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:20:21 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 11 Oct 2022 23:20:21 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:66e24392f842ad35144e78bc3adad500757ab527859ee38957e527487ef8b47a`  
		Last Modified: Tue, 11 Oct 2022 23:21:01 GMT  
		Size: 7.6 MB (7637811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7a9e727242f052ad7f1aef67b29982a8d3f8bd6ea7e8cc8c76f3c7d2b044c667
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7300810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fad641972f0ff8f1dab2e34dca1f8e4011c5d32c7607c5bff6949a6a86d90b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 11:34:26 GMT
COPY file:f7568230fc06888b50a5f3da0004bb7dc7a70b1defec143315a57570b4b91602 in /nats-streaming-server 
# Fri, 11 Nov 2022 11:34:26 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 11:34:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 11:34:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:8ac505d089b210f05398eb249b7f3065fef3921be727978b70df4c11955da8d8`  
		Last Modified: Tue, 11 Oct 2022 23:50:41 GMT  
		Size: 7.3 MB (7300810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:45afd9c11672161333d5775564d46f19d15ba48f4a1bbd188da2e79c5d7b4a07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7288898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8f3428876076d61520fde190b5fc4f479e3f80a5d6c914c210470635215bd6`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 10 Nov 2022 21:12:17 GMT
COPY file:bf11e23254626a7629546dd0e7e134984e019132c260d1733b972d9775ff8160 in /nats-streaming-server 
# Thu, 10 Nov 2022 21:12:18 GMT
EXPOSE 4222 8222
# Thu, 10 Nov 2022 21:12:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 10 Nov 2022 21:12:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2d5acf820909de2ff213199833cde1d52214f332d026d6f0b3807d819e2f657d`  
		Last Modified: Wed, 12 Oct 2022 01:12:22 GMT  
		Size: 7.3 MB (7288898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:bdfae072b67d1ab734914a443796e974f5a7d73caa19aa5ba1a7abb335155705
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6994195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e5a4af7852aeaf241bd9103b8dcf4f7a1e9bd382a49dcfadf25aa83a1c404a`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 11 Nov 2022 08:57:36 GMT
COPY file:215fac5233cbc7ee50e4033b703c84c22a4b219b4ab4c43d7317bc92b89f206c in /nats-streaming-server 
# Fri, 11 Nov 2022 08:57:36 GMT
EXPOSE 4222 8222
# Fri, 11 Nov 2022 08:57:36 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 11 Nov 2022 08:57:36 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:921e27ff4fbea0ffa1980a0bb3e13d378b150d7a7167d0dae7a3efbdc4408e37`  
		Last Modified: Tue, 11 Oct 2022 23:41:25 GMT  
		Size: 7.0 MB (6994195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:fc9f3a4493f401deed6acdcadaff40c596751f6fc9b5cd6fd3a5597e876c4841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats-streaming@sha256:e432cca2b1fb2af40ca299e80a02579387266d13a256bf7a23dfd7125a0ae4a1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2787076749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13f247cbd55632a872bae42021882364e6678b369692b701f6ebb8e9b0ddc4d`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Wed, 09 Nov 2022 14:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Nov 2022 16:44:45 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 18:16:17 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Wed, 09 Nov 2022 18:16:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.2/nats-streaming-server-v0.25.2-windows-amd64.zip
# Wed, 09 Nov 2022 18:16:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=554b083bb17f8f2e9a875b888dbe74454648f86c6e02bc489d88713431025d9d
# Wed, 09 Nov 2022 18:17:30 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Nov 2022 18:19:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Nov 2022 18:19:40 GMT
EXPOSE 4222 8222
# Wed, 09 Nov 2022 18:19:41 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Nov 2022 18:19:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99941fb33972e616b231a8aadd93463fdfd5de6aece4aa6c470d2feec31839be`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f3d8a87f0a1540850986ff94131286dfa42ca116f04779e02f60b3a724641b`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe863d992e0c58c9cf1632767e37ade6556903b1bb890c2a4dc02dffeaed78ef`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71a5994065b88d8a198293e12ac4530e9342de0f4d53860ee2743bd2d569013`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8e674abd79efbd197e128d166729af96bcf66ffb1646f10fb80dde56503f83`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec5f49fc868f6f3b72e2f76461f16e59f80e92a4186383b3baf71c06d3d2b21`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 359.2 KB (359194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0897e7aebc234f59c04916a3b53b2a9b5ac2bda1415cddcb71ddf1966d20bdfc`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 8.1 MB (8119591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ea295c4d678432a3afecc78785a990244c290159cc0851aa868efc70979b97`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a938d3ad7b90133750f1d10713db202d85b54f492cb2aef146e304f77b66f49`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b500e39240181724cbcb1a40781d36fae94a34eef9f926a5c612644211b67f`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:fc9f3a4493f401deed6acdcadaff40c596751f6fc9b5cd6fd3a5597e876c4841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull nats-streaming@sha256:e432cca2b1fb2af40ca299e80a02579387266d13a256bf7a23dfd7125a0ae4a1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2787076749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13f247cbd55632a872bae42021882364e6678b369692b701f6ebb8e9b0ddc4d`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Wed, 09 Nov 2022 14:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Nov 2022 16:44:45 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Nov 2022 18:16:17 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Wed, 09 Nov 2022 18:16:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.2/nats-streaming-server-v0.25.2-windows-amd64.zip
# Wed, 09 Nov 2022 18:16:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=554b083bb17f8f2e9a875b888dbe74454648f86c6e02bc489d88713431025d9d
# Wed, 09 Nov 2022 18:17:30 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Nov 2022 18:19:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 09 Nov 2022 18:19:40 GMT
EXPOSE 4222 8222
# Wed, 09 Nov 2022 18:19:41 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Nov 2022 18:19:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99941fb33972e616b231a8aadd93463fdfd5de6aece4aa6c470d2feec31839be`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f3d8a87f0a1540850986ff94131286dfa42ca116f04779e02f60b3a724641b`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe863d992e0c58c9cf1632767e37ade6556903b1bb890c2a4dc02dffeaed78ef`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71a5994065b88d8a198293e12ac4530e9342de0f4d53860ee2743bd2d569013`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8e674abd79efbd197e128d166729af96bcf66ffb1646f10fb80dde56503f83`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec5f49fc868f6f3b72e2f76461f16e59f80e92a4186383b3baf71c06d3d2b21`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 359.2 KB (359194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0897e7aebc234f59c04916a3b53b2a9b5ac2bda1415cddcb71ddf1966d20bdfc`  
		Last Modified: Wed, 09 Nov 2022 18:20:35 GMT  
		Size: 8.1 MB (8119591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ea295c4d678432a3afecc78785a990244c290159cc0851aa868efc70979b97`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a938d3ad7b90133750f1d10713db202d85b54f492cb2aef146e304f77b66f49`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b500e39240181724cbcb1a40781d36fae94a34eef9f926a5c612644211b67f`  
		Last Modified: Wed, 09 Nov 2022 18:20:33 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
