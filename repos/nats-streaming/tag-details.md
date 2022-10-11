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
$ docker pull nats-streaming@sha256:24ca00f95f09f253a277590a2d3206e82b1c0600b834340a9b3fd725cbce72e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	windows version 10.0.17763.3532; amd64

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

### `nats-streaming:0.25` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats-streaming@sha256:cfd77a52c292b4041cbb0a76a55f488d022224bb85271d9f92a8a4fc5c8f5fa4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111143785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f200df236cb835ed205e49e6d4fbcccf4922bb86621a3b84212afe6637b10b7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 23:18:05 GMT
RUN cmd /S /C #(nop) COPY file:8231e132ceae2f5beb184edb8fd6927d5df2cb8a2774f0cb9b809b1a9176fa02 in C:\nats-streaming-server.exe 
# Tue, 11 Oct 2022 23:18:06 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:18:06 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Oct 2022 23:18:07 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3d4d61d6915ceca5246fbd620385fae02dbdc535a097c3aaf0350da86042b9`  
		Last Modified: Tue, 11 Oct 2022 23:18:51 GMT  
		Size: 7.8 MB (7762223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86779f9773546ae6441977745f02c8b15acce03afb229aeb57dac89c93b90b4f`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6af5e059014bb8bacfed4a8002178e0b114a4e4a7ee13f910188094e20e3b8`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb940ae6eabc5c3bd86a4b8566e1788bf84fb2687dd0fb027ce5b9cbb73fe80`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine`

```console
$ docker pull nats-streaming@sha256:21fd82509fac952a0d062bef49083bf7e294ae0a71ac5e05e74fd96f1fe3b3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `nats-streaming:0.25-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:994809a2a1c9823c5498a571c38d3bf773ebc702b10749983dce45b7a42cf712
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10726919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a408e43ce29cd045b46218f708c6a8c44050248220f5db8e8f837b94e82972`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 23:20:12 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Tue, 11 Oct 2022 23:20:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 11 Oct 2022 23:20:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 11 Oct 2022 23:20:15 GMT
EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:20:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 23:20:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1169afb18c1b6bb90747fac0f8a05090272062e2e2d120fb1dacfe825d8838a`  
		Last Modified: Tue, 11 Oct 2022 23:20:42 GMT  
		Size: 7.9 MB (7920443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba67a538f93cdd3f5fd299df6156a9825e518c36aea1fb2ec60c068ba8b96a4`  
		Last Modified: Tue, 11 Oct 2022 23:20:41 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine3.16`

```console
$ docker pull nats-streaming@sha256:21fd82509fac952a0d062bef49083bf7e294ae0a71ac5e05e74fd96f1fe3b3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `nats-streaming:0.25-alpine3.16` - linux; amd64

```console
$ docker pull nats-streaming@sha256:994809a2a1c9823c5498a571c38d3bf773ebc702b10749983dce45b7a42cf712
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10726919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a408e43ce29cd045b46218f708c6a8c44050248220f5db8e8f837b94e82972`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 23:20:12 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Tue, 11 Oct 2022 23:20:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 11 Oct 2022 23:20:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 11 Oct 2022 23:20:15 GMT
EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:20:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 23:20:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1169afb18c1b6bb90747fac0f8a05090272062e2e2d120fb1dacfe825d8838a`  
		Last Modified: Tue, 11 Oct 2022 23:20:42 GMT  
		Size: 7.9 MB (7920443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba67a538f93cdd3f5fd299df6156a9825e518c36aea1fb2ec60c068ba8b96a4`  
		Last Modified: Tue, 11 Oct 2022 23:20:41 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-linux`

```console
$ docker pull nats-streaming@sha256:f883f9cd7e5bbcff70428de4a18390498931c621bd5aae062ffa7edb13dcc519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

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

## `nats-streaming:0.25-nanoserver`

```console
$ docker pull nats-streaming@sha256:0b9646472a3d88906cae4468e64aa579ecc702b1abc87fbb09f9bbf4a8712665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats-streaming:0.25-nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats-streaming@sha256:cfd77a52c292b4041cbb0a76a55f488d022224bb85271d9f92a8a4fc5c8f5fa4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111143785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f200df236cb835ed205e49e6d4fbcccf4922bb86621a3b84212afe6637b10b7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 23:18:05 GMT
RUN cmd /S /C #(nop) COPY file:8231e132ceae2f5beb184edb8fd6927d5df2cb8a2774f0cb9b809b1a9176fa02 in C:\nats-streaming-server.exe 
# Tue, 11 Oct 2022 23:18:06 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:18:06 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Oct 2022 23:18:07 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3d4d61d6915ceca5246fbd620385fae02dbdc535a097c3aaf0350da86042b9`  
		Last Modified: Tue, 11 Oct 2022 23:18:51 GMT  
		Size: 7.8 MB (7762223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86779f9773546ae6441977745f02c8b15acce03afb229aeb57dac89c93b90b4f`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6af5e059014bb8bacfed4a8002178e0b114a4e4a7ee13f910188094e20e3b8`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb940ae6eabc5c3bd86a4b8566e1788bf84fb2687dd0fb027ce5b9cbb73fe80`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:0b9646472a3d88906cae4468e64aa579ecc702b1abc87fbb09f9bbf4a8712665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats-streaming:0.25-nanoserver-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats-streaming@sha256:cfd77a52c292b4041cbb0a76a55f488d022224bb85271d9f92a8a4fc5c8f5fa4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111143785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f200df236cb835ed205e49e6d4fbcccf4922bb86621a3b84212afe6637b10b7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 23:18:05 GMT
RUN cmd /S /C #(nop) COPY file:8231e132ceae2f5beb184edb8fd6927d5df2cb8a2774f0cb9b809b1a9176fa02 in C:\nats-streaming-server.exe 
# Tue, 11 Oct 2022 23:18:06 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:18:06 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Oct 2022 23:18:07 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3d4d61d6915ceca5246fbd620385fae02dbdc535a097c3aaf0350da86042b9`  
		Last Modified: Tue, 11 Oct 2022 23:18:51 GMT  
		Size: 7.8 MB (7762223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86779f9773546ae6441977745f02c8b15acce03afb229aeb57dac89c93b90b4f`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6af5e059014bb8bacfed4a8002178e0b114a4e4a7ee13f910188094e20e3b8`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb940ae6eabc5c3bd86a4b8566e1788bf84fb2687dd0fb027ce5b9cbb73fe80`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-scratch`

```console
$ docker pull nats-streaming@sha256:f883f9cd7e5bbcff70428de4a18390498931c621bd5aae062ffa7edb13dcc519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

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

## `nats-streaming:0.25-windowsservercore`

```console
$ docker pull nats-streaming@sha256:08add9377344ece93773593595d067ff6213a1fd8f3aeadaced3a416a0f1e862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats-streaming:0.25-windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats-streaming@sha256:561ff40c97b72993e865a9d1e67bf2efc98b56f26203a614f09a98871c56341a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2719604919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12526adef9358767115ed18a3796f537913045dbf9cd4aa5b19b8ea165a3ba28`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 17:22:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Oct 2022 17:22:08 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 23:14:50 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Tue, 11 Oct 2022 23:14:51 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.2/nats-streaming-server-v0.25.2-windows-amd64.zip
# Tue, 11 Oct 2022 23:14:52 GMT
ENV NATS_STREAMING_SERVER_SHASUM=554b083bb17f8f2e9a875b888dbe74454648f86c6e02bc489d88713431025d9d
# Tue, 11 Oct 2022 23:16:04 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Oct 2022 23:17:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 11 Oct 2022 23:17:43 GMT
EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:17:44 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Oct 2022 23:17:46 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621a26d6741b8fa07e8537ea294beb808bdc2abc7a6b90edfff87b6d0c705254`  
		Last Modified: Tue, 11 Oct 2022 23:18:37 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36da726d389d81cd01a9a5b0748eb247c729557c616b01b0a370d70f9c0de8c3`  
		Last Modified: Tue, 11 Oct 2022 23:18:37 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07060f1fab2dbea3f212e1d66c928e0f9d6147a24a3bc50b20dd1ffee31456d`  
		Last Modified: Tue, 11 Oct 2022 23:18:36 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590f82b28b084905a277ad23b3c0e61e6f330cff276155c04f12de3fd476a33a`  
		Last Modified: Tue, 11 Oct 2022 23:18:34 GMT  
		Size: 341.6 KB (341576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6448bcae93c7f339866a8b88ff6727d6f4e074bba71ba54510e5dd7e9ff6b04`  
		Last Modified: Tue, 11 Oct 2022 23:18:36 GMT  
		Size: 8.1 MB (8088612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521d3c4a416fb1416120f7ddfe1a3f6de35768dbc7e36ada0e2bb2f11ceb3d82`  
		Last Modified: Tue, 11 Oct 2022 23:18:34 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9449836b32bff9b1fd5d0b26e4444aa6a795a2aedd2fc54d8b4b0073cde475ba`  
		Last Modified: Tue, 11 Oct 2022 23:18:34 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de3d6bb5af97684faff67c22b54a83aa99044e48f9c8417d94718bf8091b0a9`  
		Last Modified: Tue, 11 Oct 2022 23:18:34 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:08add9377344ece93773593595d067ff6213a1fd8f3aeadaced3a416a0f1e862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats-streaming:0.25-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats-streaming@sha256:561ff40c97b72993e865a9d1e67bf2efc98b56f26203a614f09a98871c56341a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2719604919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12526adef9358767115ed18a3796f537913045dbf9cd4aa5b19b8ea165a3ba28`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 17:22:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Oct 2022 17:22:08 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 23:14:50 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Tue, 11 Oct 2022 23:14:51 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.2/nats-streaming-server-v0.25.2-windows-amd64.zip
# Tue, 11 Oct 2022 23:14:52 GMT
ENV NATS_STREAMING_SERVER_SHASUM=554b083bb17f8f2e9a875b888dbe74454648f86c6e02bc489d88713431025d9d
# Tue, 11 Oct 2022 23:16:04 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Oct 2022 23:17:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 11 Oct 2022 23:17:43 GMT
EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:17:44 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Oct 2022 23:17:46 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621a26d6741b8fa07e8537ea294beb808bdc2abc7a6b90edfff87b6d0c705254`  
		Last Modified: Tue, 11 Oct 2022 23:18:37 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36da726d389d81cd01a9a5b0748eb247c729557c616b01b0a370d70f9c0de8c3`  
		Last Modified: Tue, 11 Oct 2022 23:18:37 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07060f1fab2dbea3f212e1d66c928e0f9d6147a24a3bc50b20dd1ffee31456d`  
		Last Modified: Tue, 11 Oct 2022 23:18:36 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590f82b28b084905a277ad23b3c0e61e6f330cff276155c04f12de3fd476a33a`  
		Last Modified: Tue, 11 Oct 2022 23:18:34 GMT  
		Size: 341.6 KB (341576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6448bcae93c7f339866a8b88ff6727d6f4e074bba71ba54510e5dd7e9ff6b04`  
		Last Modified: Tue, 11 Oct 2022 23:18:36 GMT  
		Size: 8.1 MB (8088612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521d3c4a416fb1416120f7ddfe1a3f6de35768dbc7e36ada0e2bb2f11ceb3d82`  
		Last Modified: Tue, 11 Oct 2022 23:18:34 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9449836b32bff9b1fd5d0b26e4444aa6a795a2aedd2fc54d8b4b0073cde475ba`  
		Last Modified: Tue, 11 Oct 2022 23:18:34 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de3d6bb5af97684faff67c22b54a83aa99044e48f9c8417d94718bf8091b0a9`  
		Last Modified: Tue, 11 Oct 2022 23:18:34 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.2`

```console
$ docker pull nats-streaming@sha256:24ca00f95f09f253a277590a2d3206e82b1c0600b834340a9b3fd725cbce72e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	windows version 10.0.17763.3532; amd64

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

### `nats-streaming:0.25.2` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats-streaming@sha256:cfd77a52c292b4041cbb0a76a55f488d022224bb85271d9f92a8a4fc5c8f5fa4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111143785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f200df236cb835ed205e49e6d4fbcccf4922bb86621a3b84212afe6637b10b7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 23:18:05 GMT
RUN cmd /S /C #(nop) COPY file:8231e132ceae2f5beb184edb8fd6927d5df2cb8a2774f0cb9b809b1a9176fa02 in C:\nats-streaming-server.exe 
# Tue, 11 Oct 2022 23:18:06 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:18:06 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Oct 2022 23:18:07 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3d4d61d6915ceca5246fbd620385fae02dbdc535a097c3aaf0350da86042b9`  
		Last Modified: Tue, 11 Oct 2022 23:18:51 GMT  
		Size: 7.8 MB (7762223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86779f9773546ae6441977745f02c8b15acce03afb229aeb57dac89c93b90b4f`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6af5e059014bb8bacfed4a8002178e0b114a4e4a7ee13f910188094e20e3b8`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb940ae6eabc5c3bd86a4b8566e1788bf84fb2687dd0fb027ce5b9cbb73fe80`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.2-alpine`

```console
$ docker pull nats-streaming@sha256:21fd82509fac952a0d062bef49083bf7e294ae0a71ac5e05e74fd96f1fe3b3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `nats-streaming:0.25.2-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:994809a2a1c9823c5498a571c38d3bf773ebc702b10749983dce45b7a42cf712
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10726919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a408e43ce29cd045b46218f708c6a8c44050248220f5db8e8f837b94e82972`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 23:20:12 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Tue, 11 Oct 2022 23:20:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 11 Oct 2022 23:20:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 11 Oct 2022 23:20:15 GMT
EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:20:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 23:20:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1169afb18c1b6bb90747fac0f8a05090272062e2e2d120fb1dacfe825d8838a`  
		Last Modified: Tue, 11 Oct 2022 23:20:42 GMT  
		Size: 7.9 MB (7920443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba67a538f93cdd3f5fd299df6156a9825e518c36aea1fb2ec60c068ba8b96a4`  
		Last Modified: Tue, 11 Oct 2022 23:20:41 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.2-alpine3.16`

```console
$ docker pull nats-streaming@sha256:21fd82509fac952a0d062bef49083bf7e294ae0a71ac5e05e74fd96f1fe3b3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `nats-streaming:0.25.2-alpine3.16` - linux; amd64

```console
$ docker pull nats-streaming@sha256:994809a2a1c9823c5498a571c38d3bf773ebc702b10749983dce45b7a42cf712
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10726919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a408e43ce29cd045b46218f708c6a8c44050248220f5db8e8f837b94e82972`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 11 Oct 2022 23:20:12 GMT
ENV NATS_STREAMING_SERVER=0.25.2
# Tue, 11 Oct 2022 23:20:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f5b9d00190a19a1cc67ace91ce6ad0b3f80db60689f13d24e9918ab9257d9a57' ;; 		armhf) natsArch='arm6'; sha256='46b7d196fd7fa48499c4ab273349ff1ce69d67b973904f2e9c5dd4cc39ef7796' ;; 		armv7) natsArch='arm7'; sha256='b0f33c99e8e8a8c7f715cdc7ab8c307711f52debf9895e0bbd33f68cbec05fb5' ;; 		x86_64) natsArch='amd64'; sha256='55789d3b4c4b5d6ddf0045a42e48f2d1fd2d220a2f4b13f561576bbd00d57154' ;; 		x86) natsArch='386'; sha256='f3ed9e878748154faeea488110a5332678a956a4959da958d30232503ffeec88' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 11 Oct 2022 23:20:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 11 Oct 2022 23:20:15 GMT
EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:20:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Oct 2022 23:20:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1169afb18c1b6bb90747fac0f8a05090272062e2e2d120fb1dacfe825d8838a`  
		Last Modified: Tue, 11 Oct 2022 23:20:42 GMT  
		Size: 7.9 MB (7920443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba67a538f93cdd3f5fd299df6156a9825e518c36aea1fb2ec60c068ba8b96a4`  
		Last Modified: Tue, 11 Oct 2022 23:20:41 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.2-linux`

```console
$ docker pull nats-streaming@sha256:f883f9cd7e5bbcff70428de4a18390498931c621bd5aae062ffa7edb13dcc519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

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

## `nats-streaming:0.25.2-nanoserver`

```console
$ docker pull nats-streaming@sha256:0b9646472a3d88906cae4468e64aa579ecc702b1abc87fbb09f9bbf4a8712665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats-streaming:0.25.2-nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats-streaming@sha256:cfd77a52c292b4041cbb0a76a55f488d022224bb85271d9f92a8a4fc5c8f5fa4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111143785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f200df236cb835ed205e49e6d4fbcccf4922bb86621a3b84212afe6637b10b7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 23:18:05 GMT
RUN cmd /S /C #(nop) COPY file:8231e132ceae2f5beb184edb8fd6927d5df2cb8a2774f0cb9b809b1a9176fa02 in C:\nats-streaming-server.exe 
# Tue, 11 Oct 2022 23:18:06 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:18:06 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Oct 2022 23:18:07 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3d4d61d6915ceca5246fbd620385fae02dbdc535a097c3aaf0350da86042b9`  
		Last Modified: Tue, 11 Oct 2022 23:18:51 GMT  
		Size: 7.8 MB (7762223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86779f9773546ae6441977745f02c8b15acce03afb229aeb57dac89c93b90b4f`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6af5e059014bb8bacfed4a8002178e0b114a4e4a7ee13f910188094e20e3b8`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb940ae6eabc5c3bd86a4b8566e1788bf84fb2687dd0fb027ce5b9cbb73fe80`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.2-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:0b9646472a3d88906cae4468e64aa579ecc702b1abc87fbb09f9bbf4a8712665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats-streaming:0.25.2-nanoserver-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats-streaming@sha256:cfd77a52c292b4041cbb0a76a55f488d022224bb85271d9f92a8a4fc5c8f5fa4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111143785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f200df236cb835ed205e49e6d4fbcccf4922bb86621a3b84212afe6637b10b7`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 11 Oct 2022 23:18:05 GMT
RUN cmd /S /C #(nop) COPY file:8231e132ceae2f5beb184edb8fd6927d5df2cb8a2774f0cb9b809b1a9176fa02 in C:\nats-streaming-server.exe 
# Tue, 11 Oct 2022 23:18:06 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Tue, 11 Oct 2022 23:18:06 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Oct 2022 23:18:07 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3d4d61d6915ceca5246fbd620385fae02dbdc535a097c3aaf0350da86042b9`  
		Last Modified: Tue, 11 Oct 2022 23:18:51 GMT  
		Size: 7.8 MB (7762223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86779f9773546ae6441977745f02c8b15acce03afb229aeb57dac89c93b90b4f`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6af5e059014bb8bacfed4a8002178e0b114a4e4a7ee13f910188094e20e3b8`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb940ae6eabc5c3bd86a4b8566e1788bf84fb2687dd0fb027ce5b9cbb73fe80`  
		Last Modified: Tue, 11 Oct 2022 23:18:49 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.2-scratch`

```console
$ docker pull nats-streaming@sha256:f883f9cd7e5bbcff70428de4a18390498931c621bd5aae062ffa7edb13dcc519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

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

## `nats-streaming:0.25.2-windowsservercore`

**does not exist** (yet?)

## `nats-streaming:0.25.2-windowsservercore-1809`

**does not exist** (yet?)

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:62c3884f8c1deac8ac9ba03dc1f01bfb779e8327cef5a4cfa041687e5a15f474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:4606fd578d27479825b289999963e68e4e250657335370a84a1037a2c4456d06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10277305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c0290694fd7675b3435bfd6d143aff63988ce53738b657c865583d82eb2a1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:09:42 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 06 Oct 2022 23:09:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 06 Oct 2022 23:09:44 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 06 Oct 2022 23:09:44 GMT
EXPOSE 4222 8222
# Thu, 06 Oct 2022 23:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Oct 2022 23:09:44 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2f30546ffdbb094f0af26e92ee193b4f2c294abd35fbdaac4f9555173b58d2`  
		Last Modified: Thu, 06 Oct 2022 23:10:11 GMT  
		Size: 7.5 MB (7453370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0545d39a4271ad475f2b86eaac24ee8e46401d84a01dd2b14d3ace87afdbff14`  
		Last Modified: Thu, 06 Oct 2022 23:10:10 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:b084f8c5ff48658ff81585bcf7f39900feeb3c1f3f816a10eb9a1858979b7076
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9590911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e456fa41b07822591e7e6ab14c348f0e7e441d10b22e23da933d39837b01e26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 21:02:09 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 06 Oct 2022 21:02:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 06 Oct 2022 21:02:12 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 06 Oct 2022 21:02:12 GMT
EXPOSE 4222 8222
# Thu, 06 Oct 2022 21:02:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Oct 2022 21:02:12 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab085ce446a4b3cf65020761cb994575fa3431ff24d32e6318ad34ad7f0218dd`  
		Last Modified: Thu, 06 Oct 2022 21:03:09 GMT  
		Size: 7.0 MB (6959362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edeb6958b3d8bb9739728ee19456bed4e1dd287e5b20ef34e54e5e7c665d01e`  
		Last Modified: Thu, 06 Oct 2022 21:03:07 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:fe5069691f3b4b97744805faf4c92ae030c70cc0b014940cbe9995214e9a0353
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9384581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5bbe06ce450a631982b5e2640e60986946c8d9793694342b77c15f3d294f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:52 GMT
ADD file:0bd18306f21937a9572e68c768f05f4a9d8341b40c2379a7bfcb857c77734a14 in / 
# Tue, 09 Aug 2022 16:57:52 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 13:51:02 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Fri, 07 Oct 2022 13:51:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 07 Oct 2022 13:51:05 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 07 Oct 2022 13:51:05 GMT
EXPOSE 4222 8222
# Fri, 07 Oct 2022 13:51:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 13:51:06 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:59775c20a906b1a49edcdc41a700a795998979d6ecf8f8d9cd7cbdf45e686d81`  
		Last Modified: Tue, 09 Aug 2022 16:59:12 GMT  
		Size: 2.4 MB (2435092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5bf79bf6710a418648bf7a9dbb87055ef8fdc616eae8fe4e812c7fd71080bf`  
		Last Modified: Fri, 07 Oct 2022 13:52:11 GMT  
		Size: 6.9 MB (6949066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d037cf2958e5997a7625104510346bf136e3e961acbd2989c9745345decf6de`  
		Last Modified: Fri, 07 Oct 2022 13:52:09 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:36ac67f49b22a24ea03062d6e9deef84fe62ce1fd8817f5ef150a9ad7532ac84
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9586414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66eed6e93633d0a99e20b9dbe8e9c93a175a7a57fd0478f5e74244cd4f7a00c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:36:26 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 06 Oct 2022 22:36:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 06 Oct 2022 22:36:30 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 06 Oct 2022 22:36:30 GMT
EXPOSE 4222 8222
# Thu, 06 Oct 2022 22:36:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Oct 2022 22:36:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0d3e515f6aa1f01cfcfdabe1234f8629a06ebb309d1082914f0c6a0e564b55`  
		Last Modified: Thu, 06 Oct 2022 22:37:20 GMT  
		Size: 6.9 MB (6867553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0810e40a2ef88b89904dca1e4c93d5ee3c1e3662aac2a3ecab27fa37e5fab7bf`  
		Last Modified: Thu, 06 Oct 2022 22:37:19 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.16`

**does not exist** (yet?)

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:6bb33eb53bb8f05095ea579b2bacdaa036e6ef7435d8f55d46788eae58ce709e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3406; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:36d7f62a66f2627e4b043a86e4015c7c7803bd502f7b60592eb099a6eae4a018
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7163528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d52822f6f0fd8c47b75a856325af9d754a8321030f39c208f5423db612de66`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Oct 2022 23:09:49 GMT
COPY file:af99aecf0be2bf06fd4ff3bdc596084c5f5b9148b321dce7ba96abc44cef84e4 in /nats-streaming-server 
# Thu, 06 Oct 2022 23:09:49 GMT
EXPOSE 4222 8222
# Thu, 06 Oct 2022 23:09:49 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 06 Oct 2022 23:09:50 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:86332753e6d2e6b137051bf8ad5c8d26bd40197ba63a859e7bb995b16e64d585`  
		Last Modified: Thu, 05 May 2022 01:30:31 GMT  
		Size: 7.2 MB (7163528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:1ed5e5c82d96d13524b899e8093815ff3c0f9e8b80143e73d92beede42b87355
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8704c35b3de78eee8f701487d54823aafa2c93a5f0c315162c7888e7ff0705`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Oct 2022 21:02:21 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Thu, 06 Oct 2022 21:02:21 GMT
EXPOSE 4222 8222
# Thu, 06 Oct 2022 21:02:21 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 06 Oct 2022 21:02:21 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:4cb2c6828785b28de1eb6d3cc4a3203ee6dbfafa28d5caa3aaa64cf3edeff468
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c4e90285c31e6c900d074499795cc476a5b4927b487bcd84fccaeb61987b4f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Oct 2022 13:51:17 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Fri, 07 Oct 2022 13:51:18 GMT
EXPOSE 4222 8222
# Fri, 07 Oct 2022 13:51:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 07 Oct 2022 13:51:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7a2960da85bfc4ed3ab05fd7f800679b3d8b9fb0109e72928f073e22b189272`  
		Last Modified: Thu, 05 May 2022 01:17:11 GMT  
		Size: 6.7 MB (6662010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:9d21c069fcfde10700ea9558b1c759a26509f7c12c5d2c52230fdcc319f3eed9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137ed08a18964f6d5ddb7feadd89c9829b063185cccbf09347e76e218801f2f9`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Oct 2022 22:36:41 GMT
COPY file:8c668f30364968805c5e68fa1df8dd1896541062cbb6f11a30bc0f7b4f154f91 in /nats-streaming-server 
# Thu, 06 Oct 2022 22:36:41 GMT
EXPOSE 4222 8222
# Thu, 06 Oct 2022 22:36:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 06 Oct 2022 22:36:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f3a5ffa8526605d52a17c89ac2550f3d06ebb996569a816e8a2faab246f37f1b`  
		Last Modified: Thu, 05 May 2022 00:48:35 GMT  
		Size: 6.6 MB (6581373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats-streaming@sha256:61c56326491ab7b5905a65f74f06b11e0afe20c5f09e19311da1fa5af970ae94
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110614622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57743fe3efe1b8d8b8aeb521ae41fe2f5e5cb29f0ae7dc64abff01c71760f37f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Sep 2022 18:09:32 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 14 Sep 2022 18:09:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Sep 2022 18:09:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Sep 2022 18:09:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b6bda313a93b8c355d5adf6e15f4b805f705c3741b235a7e4644bbffe6a6af3d`  
		Last Modified: Wed, 14 Sep 2022 15:42:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8866517ab4f48601d6e1dbe483345abf66a1ceb7e2afa20b0b4762a48a46aa6f`  
		Last Modified: Wed, 14 Sep 2022 18:10:17 GMT  
		Size: 7.3 MB (7275802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc2852853b0f2b1704e261cc782c6ab808e1d584514d38a432b94f51e54e367`  
		Last Modified: Wed, 14 Sep 2022 18:10:14 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415b5859ce395e5792ef5854dcfe6dc5119dc7243ca6fb44ef456139b0083239`  
		Last Modified: Wed, 14 Sep 2022 18:10:14 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f460870f5f3e0029b4f2600eaf0a017159962d4bd9c29cd82b3dcaf6c8618bb`  
		Last Modified: Wed, 14 Sep 2022 18:10:14 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:9a0534459d941bed9da1977aa17b63893ff64b9bd021448008f533d6042f99aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:36d7f62a66f2627e4b043a86e4015c7c7803bd502f7b60592eb099a6eae4a018
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7163528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d52822f6f0fd8c47b75a856325af9d754a8321030f39c208f5423db612de66`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Oct 2022 23:09:49 GMT
COPY file:af99aecf0be2bf06fd4ff3bdc596084c5f5b9148b321dce7ba96abc44cef84e4 in /nats-streaming-server 
# Thu, 06 Oct 2022 23:09:49 GMT
EXPOSE 4222 8222
# Thu, 06 Oct 2022 23:09:49 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 06 Oct 2022 23:09:50 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:86332753e6d2e6b137051bf8ad5c8d26bd40197ba63a859e7bb995b16e64d585`  
		Last Modified: Thu, 05 May 2022 01:30:31 GMT  
		Size: 7.2 MB (7163528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:1ed5e5c82d96d13524b899e8093815ff3c0f9e8b80143e73d92beede42b87355
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8704c35b3de78eee8f701487d54823aafa2c93a5f0c315162c7888e7ff0705`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Oct 2022 21:02:21 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Thu, 06 Oct 2022 21:02:21 GMT
EXPOSE 4222 8222
# Thu, 06 Oct 2022 21:02:21 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 06 Oct 2022 21:02:21 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:4cb2c6828785b28de1eb6d3cc4a3203ee6dbfafa28d5caa3aaa64cf3edeff468
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c4e90285c31e6c900d074499795cc476a5b4927b487bcd84fccaeb61987b4f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Oct 2022 13:51:17 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Fri, 07 Oct 2022 13:51:18 GMT
EXPOSE 4222 8222
# Fri, 07 Oct 2022 13:51:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 07 Oct 2022 13:51:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7a2960da85bfc4ed3ab05fd7f800679b3d8b9fb0109e72928f073e22b189272`  
		Last Modified: Thu, 05 May 2022 01:17:11 GMT  
		Size: 6.7 MB (6662010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:9d21c069fcfde10700ea9558b1c759a26509f7c12c5d2c52230fdcc319f3eed9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137ed08a18964f6d5ddb7feadd89c9829b063185cccbf09347e76e218801f2f9`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Oct 2022 22:36:41 GMT
COPY file:8c668f30364968805c5e68fa1df8dd1896541062cbb6f11a30bc0f7b4f154f91 in /nats-streaming-server 
# Thu, 06 Oct 2022 22:36:41 GMT
EXPOSE 4222 8222
# Thu, 06 Oct 2022 22:36:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 06 Oct 2022 22:36:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f3a5ffa8526605d52a17c89ac2550f3d06ebb996569a816e8a2faab246f37f1b`  
		Last Modified: Thu, 05 May 2022 00:48:35 GMT  
		Size: 6.6 MB (6581373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:dc5e96f0da0313518c66499b9c22bb73e62d29756cab39a39e708a47230f3c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats-streaming@sha256:61c56326491ab7b5905a65f74f06b11e0afe20c5f09e19311da1fa5af970ae94
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110614622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57743fe3efe1b8d8b8aeb521ae41fe2f5e5cb29f0ae7dc64abff01c71760f37f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Sep 2022 18:09:32 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 14 Sep 2022 18:09:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Sep 2022 18:09:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Sep 2022 18:09:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b6bda313a93b8c355d5adf6e15f4b805f705c3741b235a7e4644bbffe6a6af3d`  
		Last Modified: Wed, 14 Sep 2022 15:42:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8866517ab4f48601d6e1dbe483345abf66a1ceb7e2afa20b0b4762a48a46aa6f`  
		Last Modified: Wed, 14 Sep 2022 18:10:17 GMT  
		Size: 7.3 MB (7275802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc2852853b0f2b1704e261cc782c6ab808e1d584514d38a432b94f51e54e367`  
		Last Modified: Wed, 14 Sep 2022 18:10:14 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415b5859ce395e5792ef5854dcfe6dc5119dc7243ca6fb44ef456139b0083239`  
		Last Modified: Wed, 14 Sep 2022 18:10:14 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f460870f5f3e0029b4f2600eaf0a017159962d4bd9c29cd82b3dcaf6c8618bb`  
		Last Modified: Wed, 14 Sep 2022 18:10:14 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:dc5e96f0da0313518c66499b9c22bb73e62d29756cab39a39e708a47230f3c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats-streaming@sha256:61c56326491ab7b5905a65f74f06b11e0afe20c5f09e19311da1fa5af970ae94
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110614622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57743fe3efe1b8d8b8aeb521ae41fe2f5e5cb29f0ae7dc64abff01c71760f37f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Sep 2022 18:09:32 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 14 Sep 2022 18:09:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Sep 2022 18:09:34 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Sep 2022 18:09:35 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b6bda313a93b8c355d5adf6e15f4b805f705c3741b235a7e4644bbffe6a6af3d`  
		Last Modified: Wed, 14 Sep 2022 15:42:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8866517ab4f48601d6e1dbe483345abf66a1ceb7e2afa20b0b4762a48a46aa6f`  
		Last Modified: Wed, 14 Sep 2022 18:10:17 GMT  
		Size: 7.3 MB (7275802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc2852853b0f2b1704e261cc782c6ab808e1d584514d38a432b94f51e54e367`  
		Last Modified: Wed, 14 Sep 2022 18:10:14 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415b5859ce395e5792ef5854dcfe6dc5119dc7243ca6fb44ef456139b0083239`  
		Last Modified: Wed, 14 Sep 2022 18:10:14 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f460870f5f3e0029b4f2600eaf0a017159962d4bd9c29cd82b3dcaf6c8618bb`  
		Last Modified: Wed, 14 Sep 2022 18:10:14 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:9a0534459d941bed9da1977aa17b63893ff64b9bd021448008f533d6042f99aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:36d7f62a66f2627e4b043a86e4015c7c7803bd502f7b60592eb099a6eae4a018
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7163528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d52822f6f0fd8c47b75a856325af9d754a8321030f39c208f5423db612de66`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Oct 2022 23:09:49 GMT
COPY file:af99aecf0be2bf06fd4ff3bdc596084c5f5b9148b321dce7ba96abc44cef84e4 in /nats-streaming-server 
# Thu, 06 Oct 2022 23:09:49 GMT
EXPOSE 4222 8222
# Thu, 06 Oct 2022 23:09:49 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 06 Oct 2022 23:09:50 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:86332753e6d2e6b137051bf8ad5c8d26bd40197ba63a859e7bb995b16e64d585`  
		Last Modified: Thu, 05 May 2022 01:30:31 GMT  
		Size: 7.2 MB (7163528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:1ed5e5c82d96d13524b899e8093815ff3c0f9e8b80143e73d92beede42b87355
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8704c35b3de78eee8f701487d54823aafa2c93a5f0c315162c7888e7ff0705`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Oct 2022 21:02:21 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Thu, 06 Oct 2022 21:02:21 GMT
EXPOSE 4222 8222
# Thu, 06 Oct 2022 21:02:21 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 06 Oct 2022 21:02:21 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:4cb2c6828785b28de1eb6d3cc4a3203ee6dbfafa28d5caa3aaa64cf3edeff468
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c4e90285c31e6c900d074499795cc476a5b4927b487bcd84fccaeb61987b4f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Oct 2022 13:51:17 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Fri, 07 Oct 2022 13:51:18 GMT
EXPOSE 4222 8222
# Fri, 07 Oct 2022 13:51:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Fri, 07 Oct 2022 13:51:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7a2960da85bfc4ed3ab05fd7f800679b3d8b9fb0109e72928f073e22b189272`  
		Last Modified: Thu, 05 May 2022 01:17:11 GMT  
		Size: 6.7 MB (6662010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:9d21c069fcfde10700ea9558b1c759a26509f7c12c5d2c52230fdcc319f3eed9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137ed08a18964f6d5ddb7feadd89c9829b063185cccbf09347e76e218801f2f9`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 06 Oct 2022 22:36:41 GMT
COPY file:8c668f30364968805c5e68fa1df8dd1896541062cbb6f11a30bc0f7b4f154f91 in /nats-streaming-server 
# Thu, 06 Oct 2022 22:36:41 GMT
EXPOSE 4222 8222
# Thu, 06 Oct 2022 22:36:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 06 Oct 2022 22:36:43 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f3a5ffa8526605d52a17c89ac2550f3d06ebb996569a816e8a2faab246f37f1b`  
		Last Modified: Thu, 05 May 2022 00:48:35 GMT  
		Size: 6.6 MB (6581373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:4ca29413df64d05cc76a0ea649d9fefd07aeb760f3b7c3002b9f2d0ea1d22d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats-streaming@sha256:98828ca9a184fb9342036ed77ebba12a5f65e5602e773d2c20becb5c0248c0b6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711520133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f832dc04d554cf305878be3ed1b61add5a21c11c95b71b773a7bf185a480c5c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Wed, 14 Sep 2022 13:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Sep 2022 15:38:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Sep 2022 18:06:34 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 14 Sep 2022 18:06:35 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Wed, 14 Sep 2022 18:06:36 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Wed, 14 Sep 2022 18:07:35 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Sep 2022 18:09:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Sep 2022 18:09:18 GMT
EXPOSE 4222 8222
# Wed, 14 Sep 2022 18:09:18 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Sep 2022 18:09:19 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3c428406510f0a47ed60f28060a7d625d42344a95fdcb7c4f5746fb8857c3328`  
		Last Modified: Wed, 14 Sep 2022 15:42:13 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4bba85c5cc970a66b01ed6f4cabffa7705a0bdbc18907894f94c09b5ee2618`  
		Last Modified: Wed, 14 Sep 2022 15:42:12 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67824f2567144e6b28aeb7225a24846998f795300cd92c6f662b3bb6c03c4f01`  
		Last Modified: Wed, 14 Sep 2022 18:10:02 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef68b21bc96bf832500601ee1d1b12e3499e73f420d67f903571445001fb350`  
		Last Modified: Wed, 14 Sep 2022 18:10:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a80e1cbc772a83e6e56d7a9c90614947b35abdf84d0d15c324b546b13d2320`  
		Last Modified: Wed, 14 Sep 2022 18:10:01 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df968f78f66084fb4ea0412190e3d2de99b31c90c77a3dea0b1f784bdc45d977`  
		Last Modified: Wed, 14 Sep 2022 18:09:59 GMT  
		Size: 342.8 KB (342785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d540f8f1a6078ae5690854d9cb42cd9e836f0d9872123981c1374553a05ade`  
		Last Modified: Wed, 14 Sep 2022 18:10:01 GMT  
		Size: 7.6 MB (7601350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97853bca363b3a934ed361bc771ea9de61f7dc2d274a22a3af0cf5710b29e98`  
		Last Modified: Wed, 14 Sep 2022 18:09:59 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da37b79427a6aa90a9461635fdd56de664b77e23c00a345195256b9f66b81dd`  
		Last Modified: Wed, 14 Sep 2022 18:09:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dbaae31134e17f93d12829d6cc2837daa630dce477c7278b2ccd03f769ad7e`  
		Last Modified: Wed, 14 Sep 2022 18:09:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:4ca29413df64d05cc76a0ea649d9fefd07aeb760f3b7c3002b9f2d0ea1d22d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats-streaming@sha256:98828ca9a184fb9342036ed77ebba12a5f65e5602e773d2c20becb5c0248c0b6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711520133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f832dc04d554cf305878be3ed1b61add5a21c11c95b71b773a7bf185a480c5c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Wed, 14 Sep 2022 13:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Sep 2022 15:38:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Sep 2022 18:06:34 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 14 Sep 2022 18:06:35 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Wed, 14 Sep 2022 18:06:36 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Wed, 14 Sep 2022 18:07:35 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Sep 2022 18:09:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Sep 2022 18:09:18 GMT
EXPOSE 4222 8222
# Wed, 14 Sep 2022 18:09:18 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Sep 2022 18:09:19 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3c428406510f0a47ed60f28060a7d625d42344a95fdcb7c4f5746fb8857c3328`  
		Last Modified: Wed, 14 Sep 2022 15:42:13 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4bba85c5cc970a66b01ed6f4cabffa7705a0bdbc18907894f94c09b5ee2618`  
		Last Modified: Wed, 14 Sep 2022 15:42:12 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67824f2567144e6b28aeb7225a24846998f795300cd92c6f662b3bb6c03c4f01`  
		Last Modified: Wed, 14 Sep 2022 18:10:02 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef68b21bc96bf832500601ee1d1b12e3499e73f420d67f903571445001fb350`  
		Last Modified: Wed, 14 Sep 2022 18:10:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a80e1cbc772a83e6e56d7a9c90614947b35abdf84d0d15c324b546b13d2320`  
		Last Modified: Wed, 14 Sep 2022 18:10:01 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df968f78f66084fb4ea0412190e3d2de99b31c90c77a3dea0b1f784bdc45d977`  
		Last Modified: Wed, 14 Sep 2022 18:09:59 GMT  
		Size: 342.8 KB (342785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d540f8f1a6078ae5690854d9cb42cd9e836f0d9872123981c1374553a05ade`  
		Last Modified: Wed, 14 Sep 2022 18:10:01 GMT  
		Size: 7.6 MB (7601350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97853bca363b3a934ed361bc771ea9de61f7dc2d274a22a3af0cf5710b29e98`  
		Last Modified: Wed, 14 Sep 2022 18:09:59 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da37b79427a6aa90a9461635fdd56de664b77e23c00a345195256b9f66b81dd`  
		Last Modified: Wed, 14 Sep 2022 18:09:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dbaae31134e17f93d12829d6cc2837daa630dce477c7278b2ccd03f769ad7e`  
		Last Modified: Wed, 14 Sep 2022 18:09:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
