<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.15`](#nats2-alpine315)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.7`](#nats27)
-	[`nats:2.7-alpine`](#nats27-alpine)
-	[`nats:2.7-alpine3.15`](#nats27-alpine315)
-	[`nats:2.7-linux`](#nats27-linux)
-	[`nats:2.7-nanoserver`](#nats27-nanoserver)
-	[`nats:2.7-nanoserver-1809`](#nats27-nanoserver-1809)
-	[`nats:2.7-scratch`](#nats27-scratch)
-	[`nats:2.7-windowsservercore`](#nats27-windowsservercore)
-	[`nats:2.7-windowsservercore-1809`](#nats27-windowsservercore-1809)
-	[`nats:2.7.3`](#nats273)
-	[`nats:2.7.3-alpine`](#nats273-alpine)
-	[`nats:2.7.3-alpine3.15`](#nats273-alpine315)
-	[`nats:2.7.3-linux`](#nats273-linux)
-	[`nats:2.7.3-nanoserver`](#nats273-nanoserver)
-	[`nats:2.7.3-nanoserver-1809`](#nats273-nanoserver-1809)
-	[`nats:2.7.3-scratch`](#nats273-scratch)
-	[`nats:2.7.3-windowsservercore`](#nats273-windowsservercore)
-	[`nats:2.7.3-windowsservercore-1809`](#nats273-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.15`](#natsalpine315)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:a66bd53bc5fa8c23dc87b2d366d4e5d3987b75ad479a1c53e7f1dcfdf418d942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2686; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:5fd249efa75cf3eb595342175207fdbb390eee3034f7fe49355d7a479fa3ffe2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84de17b17b3458d2b6e6d4264ea6186c82bab718ca058f5d7738e53ca2759ac`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:8a814b0c66a47e63e5a7f4287478948812fe6e03c224d539f37ce3f950d2b6c6 in /nats-server 
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:21:14 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:21:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:277fae1baf41821774f7a2e1c3f465b28aa8693ee0cd77e0ad0bace55d9c616e`  
		Last Modified: Fri, 25 Feb 2022 02:22:04 GMT  
		Size: 4.5 MB (4498900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb932b4b3fbc873b56e996c6357055bb7700c701d17d7d87cdec31211142b49a`  
		Last Modified: Fri, 25 Feb 2022 02:22:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:2e3339e7e8d98e7bbab0613c7b7c3dd6f51fcf33ed3910a2e65e62fba7049337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc7bcc78dd550ace4def82e3db227e618d77e136274749f3bf55869e64be264`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:3a951d885f7bcec693f6fbf26a9ffd82b0c6218b6834fc6053e5812f7451b63e in /nats-server 
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:50:07 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:50:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:50:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6de87b4530f922b11edc08be8edeebc6ce0cb666907013348d4e1b9f5d51809`  
		Last Modified: Fri, 25 Feb 2022 02:52:29 GMT  
		Size: 4.2 MB (4165468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fa68b52226484e5870677184cdc47c93a7d453f334c144b5cb631346bc8111`  
		Last Modified: Fri, 25 Feb 2022 02:52:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:87cf3f8e33ebf28f35575ea083f8feb460d19fa9380d2622c82567ff3fa9d840
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eef99b95e572b23f90d60e6e157be90b05ab2f35dbcb10f83f96ece551945a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:3ee879939ad264e803dd4d6072181d968c4dd0fe076115159f70479c6309ef45 in /nats-server 
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:58:35 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:58:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67a3d8907097b9caffd9d1720b4fb2b1d2ac9dfda60a1d169abbf5494323d50a`  
		Last Modified: Fri, 25 Feb 2022 03:00:58 GMT  
		Size: 4.2 MB (4157409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5577f4846f032b281220b897161962481198ead0a1b9ad1d7c76cdd989747`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e970861a260709ae1e8c892eb36758c14323e81959ff4aaa1e9b7327b91d3e70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4414e48026697a15338f28dcb8e46ace9627ea7332559e1708f36ce62a5e327`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 03:01:42 GMT
COPY file:acd11e9a3a86f6f3da079c5155851337e747c3b31481ec05e2dd1e48e23becb2 in /nats-server 
# Fri, 25 Feb 2022 03:01:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 03:01:43 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 03:01:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6ad9fd47af885b43442590ad2c8171e4b4899caef84921ec73ba0540b9c03284`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 4.1 MB (4143299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7667f81936503f26a5ed657cfffdc9add626da8ae5bb78d691054cd3af7c3`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:90209bda1cad3ec772bc2677672f501958ee7d62c33edfa857dc1716bda9220b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107602854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07847f304e7f8ec4f2b589a503ef48b8ec40f915777bb525440734cb80354bfe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:d5609a37f534b519fa4326428362ea5398f7165ee90493fb7bdc8b810da33b0e in C:\nats-server.exe 
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:40:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:40:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:40:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faa5157704c1d4e58658a58ee4a6c9c9311a1d1fad5bed72177cbe21cf41dcb`  
		Last Modified: Wed, 09 Mar 2022 16:41:04 GMT  
		Size: 4.5 MB (4541860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa65daf1bc9817f903056d7a32becb96a3c4ae626707c391c115f9672dd19f9`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ca210f6c322c3169919cabf4b4814ab663aa766949d78aa18e5e52bbc9c7b7`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa906eba8a8100c8da6161e182387637cb7d3e7272ba27fb859f8c511abc7ba4`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a943f384f132c325e714fb870d67abbfbde1e4ffb1379784d990e39e0e3913`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:6944283c7d430ef4d5e23afb87b2a2d9faf963793bcd94b0461bc12def6c74c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:6f8d631c068a9d37845ebee434d2c37606757634b9d8950e8de1035dc68842b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7591453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775ec723ebf4c964b880457f54f66782e850e7121d3264c851da7d58cddb64bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:21:01 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:21:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:21:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:21:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:21:04 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:21:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfad251bce41e482876302125c33ef603e0ca99f33d1d274a09af07e1acd1be6`  
		Last Modified: Fri, 25 Feb 2022 02:21:40 GMT  
		Size: 4.8 MB (4772040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c6f8e0dbab2106f703f51433a684cef43840e5e7443402b474f3c09144a4fe`  
		Last Modified: Fri, 25 Feb 2022 02:21:39 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d8341c3c348e685617552e338228d15dd937ca0708bd7ab85c3c1b273ed88c`  
		Last Modified: Fri, 25 Feb 2022 02:21:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d6f43ae04309c6115c32d1c71469973712b3e817088a449ce37a9e8cb6b86bf9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846b4c8922b69a90d198633a7b622da89348aa9e3f7f11f58a294e2c4b112a33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:49:34 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:49:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:49:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:49:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:49:39 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:49:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:49:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecb484648e454aaf42c41938db64a0715cb509a90811b5912192d2e66a2f7fb`  
		Last Modified: Fri, 25 Feb 2022 02:51:52 GMT  
		Size: 4.4 MB (4439176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd675987846849cf3247fbc41b25505410823bffd30e841e7f663936458e553`  
		Last Modified: Fri, 25 Feb 2022 02:51:49 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae450e4bdcdcad0dc3e04a43f8855409627f6c7fdecd22f661dbfe3a99530d2`  
		Last Modified: Fri, 25 Feb 2022 02:51:49 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:665c6221a3c009747c340953834a8e1c6e38008d728f3a9d4d4eaab76e8e640d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6865015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23f21c3235ba9d61b53aeb161021b62412dc690dd81727439de14a1f9b902eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:57:52 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:57:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:57:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:57:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:57:58 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:57:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:57:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fafd4ba596baa033665a46ce765df0c4a928784832ecc5645944032cfcd9295`  
		Last Modified: Fri, 25 Feb 2022 03:00:20 GMT  
		Size: 4.4 MB (4429250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb2edff52bc9250fdec4032d39728784d4495539ef65cceed401a8968ec2df5`  
		Last Modified: Fri, 25 Feb 2022 03:00:18 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1047f2aa448d4163e2995aed662d6890fdd3954289a1ff2908edc894450b3d78`  
		Last Modified: Fri, 25 Feb 2022 03:00:18 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8f79d8af0b084884d2cc9641a33a1274022fc51b99e955d3f13d9c45f47cf6b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7132810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50bb490b2ac0a89152a29fc28e269300b6b83d2a85c0ce5ebe74635c34cdb0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:01:24 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 03:01:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 03:01:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 03:01:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 03:01:29 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:01:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c75ed4d21bde940c8f5b4d0d82b44c31489bd5a37d46b1f197b7d1baed0b6e8`  
		Last Modified: Fri, 25 Feb 2022 03:02:31 GMT  
		Size: 4.4 MB (4416403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7dd0d82f2c731b21df156c69326c651274a35eb010b23b5150397309110717`  
		Last Modified: Fri, 25 Feb 2022 03:02:30 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f29d0f81d7bbfb90bc5607be41aabbd3e970b1e74e19a069c23e863092772ba`  
		Last Modified: Fri, 25 Feb 2022 03:02:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.15`

```console
$ docker pull nats@sha256:6944283c7d430ef4d5e23afb87b2a2d9faf963793bcd94b0461bc12def6c74c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:6f8d631c068a9d37845ebee434d2c37606757634b9d8950e8de1035dc68842b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7591453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775ec723ebf4c964b880457f54f66782e850e7121d3264c851da7d58cddb64bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:21:01 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:21:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:21:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:21:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:21:04 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:21:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfad251bce41e482876302125c33ef603e0ca99f33d1d274a09af07e1acd1be6`  
		Last Modified: Fri, 25 Feb 2022 02:21:40 GMT  
		Size: 4.8 MB (4772040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c6f8e0dbab2106f703f51433a684cef43840e5e7443402b474f3c09144a4fe`  
		Last Modified: Fri, 25 Feb 2022 02:21:39 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d8341c3c348e685617552e338228d15dd937ca0708bd7ab85c3c1b273ed88c`  
		Last Modified: Fri, 25 Feb 2022 02:21:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:d6f43ae04309c6115c32d1c71469973712b3e817088a449ce37a9e8cb6b86bf9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846b4c8922b69a90d198633a7b622da89348aa9e3f7f11f58a294e2c4b112a33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:49:34 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:49:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:49:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:49:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:49:39 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:49:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:49:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecb484648e454aaf42c41938db64a0715cb509a90811b5912192d2e66a2f7fb`  
		Last Modified: Fri, 25 Feb 2022 02:51:52 GMT  
		Size: 4.4 MB (4439176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd675987846849cf3247fbc41b25505410823bffd30e841e7f663936458e553`  
		Last Modified: Fri, 25 Feb 2022 02:51:49 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae450e4bdcdcad0dc3e04a43f8855409627f6c7fdecd22f661dbfe3a99530d2`  
		Last Modified: Fri, 25 Feb 2022 02:51:49 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:665c6221a3c009747c340953834a8e1c6e38008d728f3a9d4d4eaab76e8e640d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6865015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23f21c3235ba9d61b53aeb161021b62412dc690dd81727439de14a1f9b902eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:57:52 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:57:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:57:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:57:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:57:58 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:57:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:57:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fafd4ba596baa033665a46ce765df0c4a928784832ecc5645944032cfcd9295`  
		Last Modified: Fri, 25 Feb 2022 03:00:20 GMT  
		Size: 4.4 MB (4429250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb2edff52bc9250fdec4032d39728784d4495539ef65cceed401a8968ec2df5`  
		Last Modified: Fri, 25 Feb 2022 03:00:18 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1047f2aa448d4163e2995aed662d6890fdd3954289a1ff2908edc894450b3d78`  
		Last Modified: Fri, 25 Feb 2022 03:00:18 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8f79d8af0b084884d2cc9641a33a1274022fc51b99e955d3f13d9c45f47cf6b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7132810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50bb490b2ac0a89152a29fc28e269300b6b83d2a85c0ce5ebe74635c34cdb0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:01:24 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 03:01:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 03:01:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 03:01:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 03:01:29 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:01:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c75ed4d21bde940c8f5b4d0d82b44c31489bd5a37d46b1f197b7d1baed0b6e8`  
		Last Modified: Fri, 25 Feb 2022 03:02:31 GMT  
		Size: 4.4 MB (4416403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7dd0d82f2c731b21df156c69326c651274a35eb010b23b5150397309110717`  
		Last Modified: Fri, 25 Feb 2022 03:02:30 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f29d0f81d7bbfb90bc5607be41aabbd3e970b1e74e19a069c23e863092772ba`  
		Last Modified: Fri, 25 Feb 2022 03:02:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:4fe2c16e211795858e7e7538197ec57f67ed6e9ca5d91d06d925e09ec6724d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:5fd249efa75cf3eb595342175207fdbb390eee3034f7fe49355d7a479fa3ffe2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84de17b17b3458d2b6e6d4264ea6186c82bab718ca058f5d7738e53ca2759ac`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:8a814b0c66a47e63e5a7f4287478948812fe6e03c224d539f37ce3f950d2b6c6 in /nats-server 
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:21:14 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:21:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:277fae1baf41821774f7a2e1c3f465b28aa8693ee0cd77e0ad0bace55d9c616e`  
		Last Modified: Fri, 25 Feb 2022 02:22:04 GMT  
		Size: 4.5 MB (4498900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb932b4b3fbc873b56e996c6357055bb7700c701d17d7d87cdec31211142b49a`  
		Last Modified: Fri, 25 Feb 2022 02:22:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:2e3339e7e8d98e7bbab0613c7b7c3dd6f51fcf33ed3910a2e65e62fba7049337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc7bcc78dd550ace4def82e3db227e618d77e136274749f3bf55869e64be264`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:3a951d885f7bcec693f6fbf26a9ffd82b0c6218b6834fc6053e5812f7451b63e in /nats-server 
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:50:07 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:50:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:50:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6de87b4530f922b11edc08be8edeebc6ce0cb666907013348d4e1b9f5d51809`  
		Last Modified: Fri, 25 Feb 2022 02:52:29 GMT  
		Size: 4.2 MB (4165468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fa68b52226484e5870677184cdc47c93a7d453f334c144b5cb631346bc8111`  
		Last Modified: Fri, 25 Feb 2022 02:52:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:87cf3f8e33ebf28f35575ea083f8feb460d19fa9380d2622c82567ff3fa9d840
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eef99b95e572b23f90d60e6e157be90b05ab2f35dbcb10f83f96ece551945a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:3ee879939ad264e803dd4d6072181d968c4dd0fe076115159f70479c6309ef45 in /nats-server 
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:58:35 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:58:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67a3d8907097b9caffd9d1720b4fb2b1d2ac9dfda60a1d169abbf5494323d50a`  
		Last Modified: Fri, 25 Feb 2022 03:00:58 GMT  
		Size: 4.2 MB (4157409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5577f4846f032b281220b897161962481198ead0a1b9ad1d7c76cdd989747`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e970861a260709ae1e8c892eb36758c14323e81959ff4aaa1e9b7327b91d3e70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4414e48026697a15338f28dcb8e46ace9627ea7332559e1708f36ce62a5e327`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 03:01:42 GMT
COPY file:acd11e9a3a86f6f3da079c5155851337e747c3b31481ec05e2dd1e48e23becb2 in /nats-server 
# Fri, 25 Feb 2022 03:01:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 03:01:43 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 03:01:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6ad9fd47af885b43442590ad2c8171e4b4899caef84921ec73ba0540b9c03284`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 4.1 MB (4143299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7667f81936503f26a5ed657cfffdc9add626da8ae5bb78d691054cd3af7c3`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:17a7ba92d7d9e30b2ade1940d64a5f64ea45274342f23bce8aec50f7c7c0079a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:90209bda1cad3ec772bc2677672f501958ee7d62c33edfa857dc1716bda9220b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107602854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07847f304e7f8ec4f2b589a503ef48b8ec40f915777bb525440734cb80354bfe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:d5609a37f534b519fa4326428362ea5398f7165ee90493fb7bdc8b810da33b0e in C:\nats-server.exe 
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:40:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:40:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:40:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faa5157704c1d4e58658a58ee4a6c9c9311a1d1fad5bed72177cbe21cf41dcb`  
		Last Modified: Wed, 09 Mar 2022 16:41:04 GMT  
		Size: 4.5 MB (4541860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa65daf1bc9817f903056d7a32becb96a3c4ae626707c391c115f9672dd19f9`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ca210f6c322c3169919cabf4b4814ab663aa766949d78aa18e5e52bbc9c7b7`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa906eba8a8100c8da6161e182387637cb7d3e7272ba27fb859f8c511abc7ba4`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a943f384f132c325e714fb870d67abbfbde1e4ffb1379784d990e39e0e3913`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:17a7ba92d7d9e30b2ade1940d64a5f64ea45274342f23bce8aec50f7c7c0079a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:90209bda1cad3ec772bc2677672f501958ee7d62c33edfa857dc1716bda9220b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107602854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07847f304e7f8ec4f2b589a503ef48b8ec40f915777bb525440734cb80354bfe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:d5609a37f534b519fa4326428362ea5398f7165ee90493fb7bdc8b810da33b0e in C:\nats-server.exe 
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:40:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:40:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:40:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faa5157704c1d4e58658a58ee4a6c9c9311a1d1fad5bed72177cbe21cf41dcb`  
		Last Modified: Wed, 09 Mar 2022 16:41:04 GMT  
		Size: 4.5 MB (4541860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa65daf1bc9817f903056d7a32becb96a3c4ae626707c391c115f9672dd19f9`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ca210f6c322c3169919cabf4b4814ab663aa766949d78aa18e5e52bbc9c7b7`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa906eba8a8100c8da6161e182387637cb7d3e7272ba27fb859f8c511abc7ba4`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a943f384f132c325e714fb870d67abbfbde1e4ffb1379784d990e39e0e3913`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:4fe2c16e211795858e7e7538197ec57f67ed6e9ca5d91d06d925e09ec6724d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:5fd249efa75cf3eb595342175207fdbb390eee3034f7fe49355d7a479fa3ffe2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84de17b17b3458d2b6e6d4264ea6186c82bab718ca058f5d7738e53ca2759ac`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:8a814b0c66a47e63e5a7f4287478948812fe6e03c224d539f37ce3f950d2b6c6 in /nats-server 
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:21:14 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:21:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:277fae1baf41821774f7a2e1c3f465b28aa8693ee0cd77e0ad0bace55d9c616e`  
		Last Modified: Fri, 25 Feb 2022 02:22:04 GMT  
		Size: 4.5 MB (4498900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb932b4b3fbc873b56e996c6357055bb7700c701d17d7d87cdec31211142b49a`  
		Last Modified: Fri, 25 Feb 2022 02:22:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:2e3339e7e8d98e7bbab0613c7b7c3dd6f51fcf33ed3910a2e65e62fba7049337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc7bcc78dd550ace4def82e3db227e618d77e136274749f3bf55869e64be264`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:3a951d885f7bcec693f6fbf26a9ffd82b0c6218b6834fc6053e5812f7451b63e in /nats-server 
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:50:07 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:50:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:50:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6de87b4530f922b11edc08be8edeebc6ce0cb666907013348d4e1b9f5d51809`  
		Last Modified: Fri, 25 Feb 2022 02:52:29 GMT  
		Size: 4.2 MB (4165468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fa68b52226484e5870677184cdc47c93a7d453f334c144b5cb631346bc8111`  
		Last Modified: Fri, 25 Feb 2022 02:52:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:87cf3f8e33ebf28f35575ea083f8feb460d19fa9380d2622c82567ff3fa9d840
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eef99b95e572b23f90d60e6e157be90b05ab2f35dbcb10f83f96ece551945a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:3ee879939ad264e803dd4d6072181d968c4dd0fe076115159f70479c6309ef45 in /nats-server 
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:58:35 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:58:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67a3d8907097b9caffd9d1720b4fb2b1d2ac9dfda60a1d169abbf5494323d50a`  
		Last Modified: Fri, 25 Feb 2022 03:00:58 GMT  
		Size: 4.2 MB (4157409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5577f4846f032b281220b897161962481198ead0a1b9ad1d7c76cdd989747`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e970861a260709ae1e8c892eb36758c14323e81959ff4aaa1e9b7327b91d3e70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4414e48026697a15338f28dcb8e46ace9627ea7332559e1708f36ce62a5e327`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 03:01:42 GMT
COPY file:acd11e9a3a86f6f3da079c5155851337e747c3b31481ec05e2dd1e48e23becb2 in /nats-server 
# Fri, 25 Feb 2022 03:01:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 03:01:43 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 03:01:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6ad9fd47af885b43442590ad2c8171e4b4899caef84921ec73ba0540b9c03284`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 4.1 MB (4143299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7667f81936503f26a5ed657cfffdc9add626da8ae5bb78d691054cd3af7c3`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:73e27c192194143e9b62c4f2ded2984b5675129b8657d9736845bcce6621cfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:e1ff01e9229d5c7bec881c29fbeb094ef95b03e54a80f66f0e65fbe41a33bb4f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720683253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd5fd97f45903baa3340c5695af50b2d1ed687b8a10e52d1f64d26c98161a5f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:36:40 GMT
ENV NATS_SERVER=2.7.3
# Wed, 09 Mar 2022 16:36:41 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.3/nats-server-v2.7.3-windows-amd64.zip
# Wed, 09 Mar 2022 16:36:42 GMT
ENV NATS_SERVER_SHASUM=ddb372da68741d897006c8d4b160c7f4788603cbaacb3fa105ddf7baada04428
# Wed, 09 Mar 2022 16:38:04 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 16:39:51 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 16:39:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:39:53 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:39:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:39:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e42c5b8ce3d2860dee66c1b5a94f8984a7164e8821a7730b2a2f3ae2ab3574`  
		Last Modified: Wed, 09 Mar 2022 16:40:42 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf812b1cfcec29602d107bef7e05f2c42661e6de68d06f42a6a50444bdfe0cb`  
		Last Modified: Wed, 09 Mar 2022 16:40:42 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4408e08c023d4b1c45f075bfdf96f67d7f0e09376be774314dd45c56ab1bd01d`  
		Last Modified: Wed, 09 Mar 2022 16:40:43 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d548cdcfc93bc734d4de576e696a2cdd3088415d58fedc3b9888e2a8a8c9e4b`  
		Last Modified: Wed, 09 Mar 2022 16:40:43 GMT  
		Size: 349.8 KB (349760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd44951b18faf73d172b09675cbb05b8f9da0d304fa69141e9c317015e2126a6`  
		Last Modified: Wed, 09 Mar 2022 16:40:41 GMT  
		Size: 4.9 MB (4867494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc91fe37c5dfe9f191cd5f4612758e1dd9320b570ab236f45b76afa49a16b7b`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c93c11781e7cd21ad6b3b0eec7bc6a86e0c9076512fe83fb39f3c9eab62a05`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b639b85df7a056548a52711dfe322991b5fe92f311037f385e9788ffe8ae1aa4`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8667684816445549d2ee046f4686fd6e753de7ecebcedb42f8e517fff3989fbd`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:73e27c192194143e9b62c4f2ded2984b5675129b8657d9736845bcce6621cfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:e1ff01e9229d5c7bec881c29fbeb094ef95b03e54a80f66f0e65fbe41a33bb4f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720683253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd5fd97f45903baa3340c5695af50b2d1ed687b8a10e52d1f64d26c98161a5f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:36:40 GMT
ENV NATS_SERVER=2.7.3
# Wed, 09 Mar 2022 16:36:41 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.3/nats-server-v2.7.3-windows-amd64.zip
# Wed, 09 Mar 2022 16:36:42 GMT
ENV NATS_SERVER_SHASUM=ddb372da68741d897006c8d4b160c7f4788603cbaacb3fa105ddf7baada04428
# Wed, 09 Mar 2022 16:38:04 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 16:39:51 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 16:39:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:39:53 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:39:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:39:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e42c5b8ce3d2860dee66c1b5a94f8984a7164e8821a7730b2a2f3ae2ab3574`  
		Last Modified: Wed, 09 Mar 2022 16:40:42 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf812b1cfcec29602d107bef7e05f2c42661e6de68d06f42a6a50444bdfe0cb`  
		Last Modified: Wed, 09 Mar 2022 16:40:42 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4408e08c023d4b1c45f075bfdf96f67d7f0e09376be774314dd45c56ab1bd01d`  
		Last Modified: Wed, 09 Mar 2022 16:40:43 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d548cdcfc93bc734d4de576e696a2cdd3088415d58fedc3b9888e2a8a8c9e4b`  
		Last Modified: Wed, 09 Mar 2022 16:40:43 GMT  
		Size: 349.8 KB (349760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd44951b18faf73d172b09675cbb05b8f9da0d304fa69141e9c317015e2126a6`  
		Last Modified: Wed, 09 Mar 2022 16:40:41 GMT  
		Size: 4.9 MB (4867494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc91fe37c5dfe9f191cd5f4612758e1dd9320b570ab236f45b76afa49a16b7b`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c93c11781e7cd21ad6b3b0eec7bc6a86e0c9076512fe83fb39f3c9eab62a05`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b639b85df7a056548a52711dfe322991b5fe92f311037f385e9788ffe8ae1aa4`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8667684816445549d2ee046f4686fd6e753de7ecebcedb42f8e517fff3989fbd`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7`

```console
$ docker pull nats@sha256:a66bd53bc5fa8c23dc87b2d366d4e5d3987b75ad479a1c53e7f1dcfdf418d942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7` - linux; amd64

```console
$ docker pull nats@sha256:5fd249efa75cf3eb595342175207fdbb390eee3034f7fe49355d7a479fa3ffe2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84de17b17b3458d2b6e6d4264ea6186c82bab718ca058f5d7738e53ca2759ac`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:8a814b0c66a47e63e5a7f4287478948812fe6e03c224d539f37ce3f950d2b6c6 in /nats-server 
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:21:14 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:21:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:277fae1baf41821774f7a2e1c3f465b28aa8693ee0cd77e0ad0bace55d9c616e`  
		Last Modified: Fri, 25 Feb 2022 02:22:04 GMT  
		Size: 4.5 MB (4498900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb932b4b3fbc873b56e996c6357055bb7700c701d17d7d87cdec31211142b49a`  
		Last Modified: Fri, 25 Feb 2022 02:22:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - linux; arm variant v6

```console
$ docker pull nats@sha256:2e3339e7e8d98e7bbab0613c7b7c3dd6f51fcf33ed3910a2e65e62fba7049337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc7bcc78dd550ace4def82e3db227e618d77e136274749f3bf55869e64be264`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:3a951d885f7bcec693f6fbf26a9ffd82b0c6218b6834fc6053e5812f7451b63e in /nats-server 
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:50:07 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:50:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:50:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6de87b4530f922b11edc08be8edeebc6ce0cb666907013348d4e1b9f5d51809`  
		Last Modified: Fri, 25 Feb 2022 02:52:29 GMT  
		Size: 4.2 MB (4165468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fa68b52226484e5870677184cdc47c93a7d453f334c144b5cb631346bc8111`  
		Last Modified: Fri, 25 Feb 2022 02:52:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - linux; arm variant v7

```console
$ docker pull nats@sha256:87cf3f8e33ebf28f35575ea083f8feb460d19fa9380d2622c82567ff3fa9d840
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eef99b95e572b23f90d60e6e157be90b05ab2f35dbcb10f83f96ece551945a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:3ee879939ad264e803dd4d6072181d968c4dd0fe076115159f70479c6309ef45 in /nats-server 
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:58:35 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:58:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67a3d8907097b9caffd9d1720b4fb2b1d2ac9dfda60a1d169abbf5494323d50a`  
		Last Modified: Fri, 25 Feb 2022 03:00:58 GMT  
		Size: 4.2 MB (4157409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5577f4846f032b281220b897161962481198ead0a1b9ad1d7c76cdd989747`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e970861a260709ae1e8c892eb36758c14323e81959ff4aaa1e9b7327b91d3e70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4414e48026697a15338f28dcb8e46ace9627ea7332559e1708f36ce62a5e327`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 03:01:42 GMT
COPY file:acd11e9a3a86f6f3da079c5155851337e747c3b31481ec05e2dd1e48e23becb2 in /nats-server 
# Fri, 25 Feb 2022 03:01:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 03:01:43 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 03:01:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6ad9fd47af885b43442590ad2c8171e4b4899caef84921ec73ba0540b9c03284`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 4.1 MB (4143299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7667f81936503f26a5ed657cfffdc9add626da8ae5bb78d691054cd3af7c3`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:90209bda1cad3ec772bc2677672f501958ee7d62c33edfa857dc1716bda9220b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107602854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07847f304e7f8ec4f2b589a503ef48b8ec40f915777bb525440734cb80354bfe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:d5609a37f534b519fa4326428362ea5398f7165ee90493fb7bdc8b810da33b0e in C:\nats-server.exe 
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:40:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:40:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:40:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faa5157704c1d4e58658a58ee4a6c9c9311a1d1fad5bed72177cbe21cf41dcb`  
		Last Modified: Wed, 09 Mar 2022 16:41:04 GMT  
		Size: 4.5 MB (4541860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa65daf1bc9817f903056d7a32becb96a3c4ae626707c391c115f9672dd19f9`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ca210f6c322c3169919cabf4b4814ab663aa766949d78aa18e5e52bbc9c7b7`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa906eba8a8100c8da6161e182387637cb7d3e7272ba27fb859f8c511abc7ba4`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a943f384f132c325e714fb870d67abbfbde1e4ffb1379784d990e39e0e3913`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-alpine`

```console
$ docker pull nats@sha256:6944283c7d430ef4d5e23afb87b2a2d9faf963793bcd94b0461bc12def6c74c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-alpine` - linux; amd64

```console
$ docker pull nats@sha256:6f8d631c068a9d37845ebee434d2c37606757634b9d8950e8de1035dc68842b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7591453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775ec723ebf4c964b880457f54f66782e850e7121d3264c851da7d58cddb64bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:21:01 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:21:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:21:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:21:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:21:04 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:21:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfad251bce41e482876302125c33ef603e0ca99f33d1d274a09af07e1acd1be6`  
		Last Modified: Fri, 25 Feb 2022 02:21:40 GMT  
		Size: 4.8 MB (4772040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c6f8e0dbab2106f703f51433a684cef43840e5e7443402b474f3c09144a4fe`  
		Last Modified: Fri, 25 Feb 2022 02:21:39 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d8341c3c348e685617552e338228d15dd937ca0708bd7ab85c3c1b273ed88c`  
		Last Modified: Fri, 25 Feb 2022 02:21:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d6f43ae04309c6115c32d1c71469973712b3e817088a449ce37a9e8cb6b86bf9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846b4c8922b69a90d198633a7b622da89348aa9e3f7f11f58a294e2c4b112a33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:49:34 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:49:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:49:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:49:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:49:39 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:49:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:49:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecb484648e454aaf42c41938db64a0715cb509a90811b5912192d2e66a2f7fb`  
		Last Modified: Fri, 25 Feb 2022 02:51:52 GMT  
		Size: 4.4 MB (4439176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd675987846849cf3247fbc41b25505410823bffd30e841e7f663936458e553`  
		Last Modified: Fri, 25 Feb 2022 02:51:49 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae450e4bdcdcad0dc3e04a43f8855409627f6c7fdecd22f661dbfe3a99530d2`  
		Last Modified: Fri, 25 Feb 2022 02:51:49 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:665c6221a3c009747c340953834a8e1c6e38008d728f3a9d4d4eaab76e8e640d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6865015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23f21c3235ba9d61b53aeb161021b62412dc690dd81727439de14a1f9b902eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:57:52 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:57:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:57:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:57:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:57:58 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:57:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:57:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fafd4ba596baa033665a46ce765df0c4a928784832ecc5645944032cfcd9295`  
		Last Modified: Fri, 25 Feb 2022 03:00:20 GMT  
		Size: 4.4 MB (4429250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb2edff52bc9250fdec4032d39728784d4495539ef65cceed401a8968ec2df5`  
		Last Modified: Fri, 25 Feb 2022 03:00:18 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1047f2aa448d4163e2995aed662d6890fdd3954289a1ff2908edc894450b3d78`  
		Last Modified: Fri, 25 Feb 2022 03:00:18 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8f79d8af0b084884d2cc9641a33a1274022fc51b99e955d3f13d9c45f47cf6b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7132810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50bb490b2ac0a89152a29fc28e269300b6b83d2a85c0ce5ebe74635c34cdb0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:01:24 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 03:01:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 03:01:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 03:01:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 03:01:29 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:01:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c75ed4d21bde940c8f5b4d0d82b44c31489bd5a37d46b1f197b7d1baed0b6e8`  
		Last Modified: Fri, 25 Feb 2022 03:02:31 GMT  
		Size: 4.4 MB (4416403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7dd0d82f2c731b21df156c69326c651274a35eb010b23b5150397309110717`  
		Last Modified: Fri, 25 Feb 2022 03:02:30 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f29d0f81d7bbfb90bc5607be41aabbd3e970b1e74e19a069c23e863092772ba`  
		Last Modified: Fri, 25 Feb 2022 03:02:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-alpine3.15`

```console
$ docker pull nats@sha256:6944283c7d430ef4d5e23afb87b2a2d9faf963793bcd94b0461bc12def6c74c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:6f8d631c068a9d37845ebee434d2c37606757634b9d8950e8de1035dc68842b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7591453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775ec723ebf4c964b880457f54f66782e850e7121d3264c851da7d58cddb64bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:21:01 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:21:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:21:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:21:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:21:04 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:21:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfad251bce41e482876302125c33ef603e0ca99f33d1d274a09af07e1acd1be6`  
		Last Modified: Fri, 25 Feb 2022 02:21:40 GMT  
		Size: 4.8 MB (4772040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c6f8e0dbab2106f703f51433a684cef43840e5e7443402b474f3c09144a4fe`  
		Last Modified: Fri, 25 Feb 2022 02:21:39 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d8341c3c348e685617552e338228d15dd937ca0708bd7ab85c3c1b273ed88c`  
		Last Modified: Fri, 25 Feb 2022 02:21:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:d6f43ae04309c6115c32d1c71469973712b3e817088a449ce37a9e8cb6b86bf9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846b4c8922b69a90d198633a7b622da89348aa9e3f7f11f58a294e2c4b112a33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:49:34 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:49:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:49:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:49:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:49:39 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:49:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:49:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecb484648e454aaf42c41938db64a0715cb509a90811b5912192d2e66a2f7fb`  
		Last Modified: Fri, 25 Feb 2022 02:51:52 GMT  
		Size: 4.4 MB (4439176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd675987846849cf3247fbc41b25505410823bffd30e841e7f663936458e553`  
		Last Modified: Fri, 25 Feb 2022 02:51:49 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae450e4bdcdcad0dc3e04a43f8855409627f6c7fdecd22f661dbfe3a99530d2`  
		Last Modified: Fri, 25 Feb 2022 02:51:49 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:665c6221a3c009747c340953834a8e1c6e38008d728f3a9d4d4eaab76e8e640d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6865015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23f21c3235ba9d61b53aeb161021b62412dc690dd81727439de14a1f9b902eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:57:52 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:57:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:57:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:57:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:57:58 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:57:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:57:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fafd4ba596baa033665a46ce765df0c4a928784832ecc5645944032cfcd9295`  
		Last Modified: Fri, 25 Feb 2022 03:00:20 GMT  
		Size: 4.4 MB (4429250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb2edff52bc9250fdec4032d39728784d4495539ef65cceed401a8968ec2df5`  
		Last Modified: Fri, 25 Feb 2022 03:00:18 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1047f2aa448d4163e2995aed662d6890fdd3954289a1ff2908edc894450b3d78`  
		Last Modified: Fri, 25 Feb 2022 03:00:18 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8f79d8af0b084884d2cc9641a33a1274022fc51b99e955d3f13d9c45f47cf6b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7132810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50bb490b2ac0a89152a29fc28e269300b6b83d2a85c0ce5ebe74635c34cdb0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:01:24 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 03:01:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 03:01:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 03:01:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 03:01:29 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:01:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c75ed4d21bde940c8f5b4d0d82b44c31489bd5a37d46b1f197b7d1baed0b6e8`  
		Last Modified: Fri, 25 Feb 2022 03:02:31 GMT  
		Size: 4.4 MB (4416403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7dd0d82f2c731b21df156c69326c651274a35eb010b23b5150397309110717`  
		Last Modified: Fri, 25 Feb 2022 03:02:30 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f29d0f81d7bbfb90bc5607be41aabbd3e970b1e74e19a069c23e863092772ba`  
		Last Modified: Fri, 25 Feb 2022 03:02:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-linux`

```console
$ docker pull nats@sha256:4fe2c16e211795858e7e7538197ec57f67ed6e9ca5d91d06d925e09ec6724d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-linux` - linux; amd64

```console
$ docker pull nats@sha256:5fd249efa75cf3eb595342175207fdbb390eee3034f7fe49355d7a479fa3ffe2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84de17b17b3458d2b6e6d4264ea6186c82bab718ca058f5d7738e53ca2759ac`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:8a814b0c66a47e63e5a7f4287478948812fe6e03c224d539f37ce3f950d2b6c6 in /nats-server 
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:21:14 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:21:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:277fae1baf41821774f7a2e1c3f465b28aa8693ee0cd77e0ad0bace55d9c616e`  
		Last Modified: Fri, 25 Feb 2022 02:22:04 GMT  
		Size: 4.5 MB (4498900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb932b4b3fbc873b56e996c6357055bb7700c701d17d7d87cdec31211142b49a`  
		Last Modified: Fri, 25 Feb 2022 02:22:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:2e3339e7e8d98e7bbab0613c7b7c3dd6f51fcf33ed3910a2e65e62fba7049337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc7bcc78dd550ace4def82e3db227e618d77e136274749f3bf55869e64be264`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:3a951d885f7bcec693f6fbf26a9ffd82b0c6218b6834fc6053e5812f7451b63e in /nats-server 
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:50:07 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:50:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:50:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6de87b4530f922b11edc08be8edeebc6ce0cb666907013348d4e1b9f5d51809`  
		Last Modified: Fri, 25 Feb 2022 02:52:29 GMT  
		Size: 4.2 MB (4165468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fa68b52226484e5870677184cdc47c93a7d453f334c144b5cb631346bc8111`  
		Last Modified: Fri, 25 Feb 2022 02:52:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:87cf3f8e33ebf28f35575ea083f8feb460d19fa9380d2622c82567ff3fa9d840
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eef99b95e572b23f90d60e6e157be90b05ab2f35dbcb10f83f96ece551945a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:3ee879939ad264e803dd4d6072181d968c4dd0fe076115159f70479c6309ef45 in /nats-server 
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:58:35 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:58:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67a3d8907097b9caffd9d1720b4fb2b1d2ac9dfda60a1d169abbf5494323d50a`  
		Last Modified: Fri, 25 Feb 2022 03:00:58 GMT  
		Size: 4.2 MB (4157409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5577f4846f032b281220b897161962481198ead0a1b9ad1d7c76cdd989747`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e970861a260709ae1e8c892eb36758c14323e81959ff4aaa1e9b7327b91d3e70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4414e48026697a15338f28dcb8e46ace9627ea7332559e1708f36ce62a5e327`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 03:01:42 GMT
COPY file:acd11e9a3a86f6f3da079c5155851337e747c3b31481ec05e2dd1e48e23becb2 in /nats-server 
# Fri, 25 Feb 2022 03:01:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 03:01:43 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 03:01:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6ad9fd47af885b43442590ad2c8171e4b4899caef84921ec73ba0540b9c03284`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 4.1 MB (4143299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7667f81936503f26a5ed657cfffdc9add626da8ae5bb78d691054cd3af7c3`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-nanoserver`

```console
$ docker pull nats@sha256:17a7ba92d7d9e30b2ade1940d64a5f64ea45274342f23bce8aec50f7c7c0079a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7-nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:90209bda1cad3ec772bc2677672f501958ee7d62c33edfa857dc1716bda9220b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107602854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07847f304e7f8ec4f2b589a503ef48b8ec40f915777bb525440734cb80354bfe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:d5609a37f534b519fa4326428362ea5398f7165ee90493fb7bdc8b810da33b0e in C:\nats-server.exe 
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:40:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:40:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:40:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faa5157704c1d4e58658a58ee4a6c9c9311a1d1fad5bed72177cbe21cf41dcb`  
		Last Modified: Wed, 09 Mar 2022 16:41:04 GMT  
		Size: 4.5 MB (4541860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa65daf1bc9817f903056d7a32becb96a3c4ae626707c391c115f9672dd19f9`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ca210f6c322c3169919cabf4b4814ab663aa766949d78aa18e5e52bbc9c7b7`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa906eba8a8100c8da6161e182387637cb7d3e7272ba27fb859f8c511abc7ba4`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a943f384f132c325e714fb870d67abbfbde1e4ffb1379784d990e39e0e3913`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-nanoserver-1809`

```console
$ docker pull nats@sha256:17a7ba92d7d9e30b2ade1940d64a5f64ea45274342f23bce8aec50f7c7c0079a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:90209bda1cad3ec772bc2677672f501958ee7d62c33edfa857dc1716bda9220b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107602854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07847f304e7f8ec4f2b589a503ef48b8ec40f915777bb525440734cb80354bfe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:d5609a37f534b519fa4326428362ea5398f7165ee90493fb7bdc8b810da33b0e in C:\nats-server.exe 
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:40:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:40:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:40:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faa5157704c1d4e58658a58ee4a6c9c9311a1d1fad5bed72177cbe21cf41dcb`  
		Last Modified: Wed, 09 Mar 2022 16:41:04 GMT  
		Size: 4.5 MB (4541860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa65daf1bc9817f903056d7a32becb96a3c4ae626707c391c115f9672dd19f9`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ca210f6c322c3169919cabf4b4814ab663aa766949d78aa18e5e52bbc9c7b7`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa906eba8a8100c8da6161e182387637cb7d3e7272ba27fb859f8c511abc7ba4`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a943f384f132c325e714fb870d67abbfbde1e4ffb1379784d990e39e0e3913`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-scratch`

```console
$ docker pull nats@sha256:4fe2c16e211795858e7e7538197ec57f67ed6e9ca5d91d06d925e09ec6724d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-scratch` - linux; amd64

```console
$ docker pull nats@sha256:5fd249efa75cf3eb595342175207fdbb390eee3034f7fe49355d7a479fa3ffe2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84de17b17b3458d2b6e6d4264ea6186c82bab718ca058f5d7738e53ca2759ac`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:8a814b0c66a47e63e5a7f4287478948812fe6e03c224d539f37ce3f950d2b6c6 in /nats-server 
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:21:14 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:21:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:277fae1baf41821774f7a2e1c3f465b28aa8693ee0cd77e0ad0bace55d9c616e`  
		Last Modified: Fri, 25 Feb 2022 02:22:04 GMT  
		Size: 4.5 MB (4498900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb932b4b3fbc873b56e996c6357055bb7700c701d17d7d87cdec31211142b49a`  
		Last Modified: Fri, 25 Feb 2022 02:22:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:2e3339e7e8d98e7bbab0613c7b7c3dd6f51fcf33ed3910a2e65e62fba7049337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc7bcc78dd550ace4def82e3db227e618d77e136274749f3bf55869e64be264`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:3a951d885f7bcec693f6fbf26a9ffd82b0c6218b6834fc6053e5812f7451b63e in /nats-server 
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:50:07 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:50:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:50:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6de87b4530f922b11edc08be8edeebc6ce0cb666907013348d4e1b9f5d51809`  
		Last Modified: Fri, 25 Feb 2022 02:52:29 GMT  
		Size: 4.2 MB (4165468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fa68b52226484e5870677184cdc47c93a7d453f334c144b5cb631346bc8111`  
		Last Modified: Fri, 25 Feb 2022 02:52:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:87cf3f8e33ebf28f35575ea083f8feb460d19fa9380d2622c82567ff3fa9d840
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eef99b95e572b23f90d60e6e157be90b05ab2f35dbcb10f83f96ece551945a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:3ee879939ad264e803dd4d6072181d968c4dd0fe076115159f70479c6309ef45 in /nats-server 
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:58:35 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:58:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67a3d8907097b9caffd9d1720b4fb2b1d2ac9dfda60a1d169abbf5494323d50a`  
		Last Modified: Fri, 25 Feb 2022 03:00:58 GMT  
		Size: 4.2 MB (4157409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5577f4846f032b281220b897161962481198ead0a1b9ad1d7c76cdd989747`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e970861a260709ae1e8c892eb36758c14323e81959ff4aaa1e9b7327b91d3e70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4414e48026697a15338f28dcb8e46ace9627ea7332559e1708f36ce62a5e327`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 03:01:42 GMT
COPY file:acd11e9a3a86f6f3da079c5155851337e747c3b31481ec05e2dd1e48e23becb2 in /nats-server 
# Fri, 25 Feb 2022 03:01:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 03:01:43 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 03:01:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6ad9fd47af885b43442590ad2c8171e4b4899caef84921ec73ba0540b9c03284`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 4.1 MB (4143299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7667f81936503f26a5ed657cfffdc9add626da8ae5bb78d691054cd3af7c3`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-windowsservercore`

```console
$ docker pull nats@sha256:73e27c192194143e9b62c4f2ded2984b5675129b8657d9736845bcce6621cfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:e1ff01e9229d5c7bec881c29fbeb094ef95b03e54a80f66f0e65fbe41a33bb4f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720683253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd5fd97f45903baa3340c5695af50b2d1ed687b8a10e52d1f64d26c98161a5f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:36:40 GMT
ENV NATS_SERVER=2.7.3
# Wed, 09 Mar 2022 16:36:41 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.3/nats-server-v2.7.3-windows-amd64.zip
# Wed, 09 Mar 2022 16:36:42 GMT
ENV NATS_SERVER_SHASUM=ddb372da68741d897006c8d4b160c7f4788603cbaacb3fa105ddf7baada04428
# Wed, 09 Mar 2022 16:38:04 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 16:39:51 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 16:39:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:39:53 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:39:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:39:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e42c5b8ce3d2860dee66c1b5a94f8984a7164e8821a7730b2a2f3ae2ab3574`  
		Last Modified: Wed, 09 Mar 2022 16:40:42 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf812b1cfcec29602d107bef7e05f2c42661e6de68d06f42a6a50444bdfe0cb`  
		Last Modified: Wed, 09 Mar 2022 16:40:42 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4408e08c023d4b1c45f075bfdf96f67d7f0e09376be774314dd45c56ab1bd01d`  
		Last Modified: Wed, 09 Mar 2022 16:40:43 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d548cdcfc93bc734d4de576e696a2cdd3088415d58fedc3b9888e2a8a8c9e4b`  
		Last Modified: Wed, 09 Mar 2022 16:40:43 GMT  
		Size: 349.8 KB (349760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd44951b18faf73d172b09675cbb05b8f9da0d304fa69141e9c317015e2126a6`  
		Last Modified: Wed, 09 Mar 2022 16:40:41 GMT  
		Size: 4.9 MB (4867494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc91fe37c5dfe9f191cd5f4612758e1dd9320b570ab236f45b76afa49a16b7b`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c93c11781e7cd21ad6b3b0eec7bc6a86e0c9076512fe83fb39f3c9eab62a05`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b639b85df7a056548a52711dfe322991b5fe92f311037f385e9788ffe8ae1aa4`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8667684816445549d2ee046f4686fd6e753de7ecebcedb42f8e517fff3989fbd`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-windowsservercore-1809`

```console
$ docker pull nats@sha256:73e27c192194143e9b62c4f2ded2984b5675129b8657d9736845bcce6621cfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:e1ff01e9229d5c7bec881c29fbeb094ef95b03e54a80f66f0e65fbe41a33bb4f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720683253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd5fd97f45903baa3340c5695af50b2d1ed687b8a10e52d1f64d26c98161a5f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:36:40 GMT
ENV NATS_SERVER=2.7.3
# Wed, 09 Mar 2022 16:36:41 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.3/nats-server-v2.7.3-windows-amd64.zip
# Wed, 09 Mar 2022 16:36:42 GMT
ENV NATS_SERVER_SHASUM=ddb372da68741d897006c8d4b160c7f4788603cbaacb3fa105ddf7baada04428
# Wed, 09 Mar 2022 16:38:04 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 16:39:51 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 16:39:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:39:53 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:39:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:39:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e42c5b8ce3d2860dee66c1b5a94f8984a7164e8821a7730b2a2f3ae2ab3574`  
		Last Modified: Wed, 09 Mar 2022 16:40:42 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf812b1cfcec29602d107bef7e05f2c42661e6de68d06f42a6a50444bdfe0cb`  
		Last Modified: Wed, 09 Mar 2022 16:40:42 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4408e08c023d4b1c45f075bfdf96f67d7f0e09376be774314dd45c56ab1bd01d`  
		Last Modified: Wed, 09 Mar 2022 16:40:43 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d548cdcfc93bc734d4de576e696a2cdd3088415d58fedc3b9888e2a8a8c9e4b`  
		Last Modified: Wed, 09 Mar 2022 16:40:43 GMT  
		Size: 349.8 KB (349760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd44951b18faf73d172b09675cbb05b8f9da0d304fa69141e9c317015e2126a6`  
		Last Modified: Wed, 09 Mar 2022 16:40:41 GMT  
		Size: 4.9 MB (4867494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc91fe37c5dfe9f191cd5f4612758e1dd9320b570ab236f45b76afa49a16b7b`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c93c11781e7cd21ad6b3b0eec7bc6a86e0c9076512fe83fb39f3c9eab62a05`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b639b85df7a056548a52711dfe322991b5fe92f311037f385e9788ffe8ae1aa4`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8667684816445549d2ee046f4686fd6e753de7ecebcedb42f8e517fff3989fbd`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.3`

```console
$ docker pull nats@sha256:a66bd53bc5fa8c23dc87b2d366d4e5d3987b75ad479a1c53e7f1dcfdf418d942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7.3` - linux; amd64

```console
$ docker pull nats@sha256:5fd249efa75cf3eb595342175207fdbb390eee3034f7fe49355d7a479fa3ffe2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84de17b17b3458d2b6e6d4264ea6186c82bab718ca058f5d7738e53ca2759ac`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:8a814b0c66a47e63e5a7f4287478948812fe6e03c224d539f37ce3f950d2b6c6 in /nats-server 
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:21:14 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:21:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:277fae1baf41821774f7a2e1c3f465b28aa8693ee0cd77e0ad0bace55d9c616e`  
		Last Modified: Fri, 25 Feb 2022 02:22:04 GMT  
		Size: 4.5 MB (4498900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb932b4b3fbc873b56e996c6357055bb7700c701d17d7d87cdec31211142b49a`  
		Last Modified: Fri, 25 Feb 2022 02:22:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.3` - linux; arm variant v6

```console
$ docker pull nats@sha256:2e3339e7e8d98e7bbab0613c7b7c3dd6f51fcf33ed3910a2e65e62fba7049337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc7bcc78dd550ace4def82e3db227e618d77e136274749f3bf55869e64be264`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:3a951d885f7bcec693f6fbf26a9ffd82b0c6218b6834fc6053e5812f7451b63e in /nats-server 
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:50:07 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:50:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:50:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6de87b4530f922b11edc08be8edeebc6ce0cb666907013348d4e1b9f5d51809`  
		Last Modified: Fri, 25 Feb 2022 02:52:29 GMT  
		Size: 4.2 MB (4165468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fa68b52226484e5870677184cdc47c93a7d453f334c144b5cb631346bc8111`  
		Last Modified: Fri, 25 Feb 2022 02:52:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.3` - linux; arm variant v7

```console
$ docker pull nats@sha256:87cf3f8e33ebf28f35575ea083f8feb460d19fa9380d2622c82567ff3fa9d840
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eef99b95e572b23f90d60e6e157be90b05ab2f35dbcb10f83f96ece551945a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:3ee879939ad264e803dd4d6072181d968c4dd0fe076115159f70479c6309ef45 in /nats-server 
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:58:35 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:58:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67a3d8907097b9caffd9d1720b4fb2b1d2ac9dfda60a1d169abbf5494323d50a`  
		Last Modified: Fri, 25 Feb 2022 03:00:58 GMT  
		Size: 4.2 MB (4157409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5577f4846f032b281220b897161962481198ead0a1b9ad1d7c76cdd989747`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.3` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e970861a260709ae1e8c892eb36758c14323e81959ff4aaa1e9b7327b91d3e70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4414e48026697a15338f28dcb8e46ace9627ea7332559e1708f36ce62a5e327`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 03:01:42 GMT
COPY file:acd11e9a3a86f6f3da079c5155851337e747c3b31481ec05e2dd1e48e23becb2 in /nats-server 
# Fri, 25 Feb 2022 03:01:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 03:01:43 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 03:01:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6ad9fd47af885b43442590ad2c8171e4b4899caef84921ec73ba0540b9c03284`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 4.1 MB (4143299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7667f81936503f26a5ed657cfffdc9add626da8ae5bb78d691054cd3af7c3`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.3` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:90209bda1cad3ec772bc2677672f501958ee7d62c33edfa857dc1716bda9220b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107602854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07847f304e7f8ec4f2b589a503ef48b8ec40f915777bb525440734cb80354bfe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:d5609a37f534b519fa4326428362ea5398f7165ee90493fb7bdc8b810da33b0e in C:\nats-server.exe 
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:40:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:40:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:40:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faa5157704c1d4e58658a58ee4a6c9c9311a1d1fad5bed72177cbe21cf41dcb`  
		Last Modified: Wed, 09 Mar 2022 16:41:04 GMT  
		Size: 4.5 MB (4541860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa65daf1bc9817f903056d7a32becb96a3c4ae626707c391c115f9672dd19f9`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ca210f6c322c3169919cabf4b4814ab663aa766949d78aa18e5e52bbc9c7b7`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa906eba8a8100c8da6161e182387637cb7d3e7272ba27fb859f8c511abc7ba4`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a943f384f132c325e714fb870d67abbfbde1e4ffb1379784d990e39e0e3913`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.3-alpine`

```console
$ docker pull nats@sha256:6944283c7d430ef4d5e23afb87b2a2d9faf963793bcd94b0461bc12def6c74c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.3-alpine` - linux; amd64

```console
$ docker pull nats@sha256:6f8d631c068a9d37845ebee434d2c37606757634b9d8950e8de1035dc68842b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7591453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775ec723ebf4c964b880457f54f66782e850e7121d3264c851da7d58cddb64bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:21:01 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:21:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:21:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:21:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:21:04 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:21:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfad251bce41e482876302125c33ef603e0ca99f33d1d274a09af07e1acd1be6`  
		Last Modified: Fri, 25 Feb 2022 02:21:40 GMT  
		Size: 4.8 MB (4772040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c6f8e0dbab2106f703f51433a684cef43840e5e7443402b474f3c09144a4fe`  
		Last Modified: Fri, 25 Feb 2022 02:21:39 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d8341c3c348e685617552e338228d15dd937ca0708bd7ab85c3c1b273ed88c`  
		Last Modified: Fri, 25 Feb 2022 02:21:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.3-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d6f43ae04309c6115c32d1c71469973712b3e817088a449ce37a9e8cb6b86bf9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846b4c8922b69a90d198633a7b622da89348aa9e3f7f11f58a294e2c4b112a33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:49:34 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:49:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:49:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:49:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:49:39 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:49:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:49:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecb484648e454aaf42c41938db64a0715cb509a90811b5912192d2e66a2f7fb`  
		Last Modified: Fri, 25 Feb 2022 02:51:52 GMT  
		Size: 4.4 MB (4439176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd675987846849cf3247fbc41b25505410823bffd30e841e7f663936458e553`  
		Last Modified: Fri, 25 Feb 2022 02:51:49 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae450e4bdcdcad0dc3e04a43f8855409627f6c7fdecd22f661dbfe3a99530d2`  
		Last Modified: Fri, 25 Feb 2022 02:51:49 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.3-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:665c6221a3c009747c340953834a8e1c6e38008d728f3a9d4d4eaab76e8e640d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6865015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23f21c3235ba9d61b53aeb161021b62412dc690dd81727439de14a1f9b902eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:57:52 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:57:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:57:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:57:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:57:58 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:57:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:57:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fafd4ba596baa033665a46ce765df0c4a928784832ecc5645944032cfcd9295`  
		Last Modified: Fri, 25 Feb 2022 03:00:20 GMT  
		Size: 4.4 MB (4429250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb2edff52bc9250fdec4032d39728784d4495539ef65cceed401a8968ec2df5`  
		Last Modified: Fri, 25 Feb 2022 03:00:18 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1047f2aa448d4163e2995aed662d6890fdd3954289a1ff2908edc894450b3d78`  
		Last Modified: Fri, 25 Feb 2022 03:00:18 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.3-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8f79d8af0b084884d2cc9641a33a1274022fc51b99e955d3f13d9c45f47cf6b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7132810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50bb490b2ac0a89152a29fc28e269300b6b83d2a85c0ce5ebe74635c34cdb0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:01:24 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 03:01:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 03:01:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 03:01:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 03:01:29 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:01:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c75ed4d21bde940c8f5b4d0d82b44c31489bd5a37d46b1f197b7d1baed0b6e8`  
		Last Modified: Fri, 25 Feb 2022 03:02:31 GMT  
		Size: 4.4 MB (4416403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7dd0d82f2c731b21df156c69326c651274a35eb010b23b5150397309110717`  
		Last Modified: Fri, 25 Feb 2022 03:02:30 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f29d0f81d7bbfb90bc5607be41aabbd3e970b1e74e19a069c23e863092772ba`  
		Last Modified: Fri, 25 Feb 2022 03:02:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.3-alpine3.15`

```console
$ docker pull nats@sha256:6944283c7d430ef4d5e23afb87b2a2d9faf963793bcd94b0461bc12def6c74c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.3-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:6f8d631c068a9d37845ebee434d2c37606757634b9d8950e8de1035dc68842b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7591453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775ec723ebf4c964b880457f54f66782e850e7121d3264c851da7d58cddb64bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:21:01 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:21:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:21:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:21:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:21:04 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:21:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfad251bce41e482876302125c33ef603e0ca99f33d1d274a09af07e1acd1be6`  
		Last Modified: Fri, 25 Feb 2022 02:21:40 GMT  
		Size: 4.8 MB (4772040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c6f8e0dbab2106f703f51433a684cef43840e5e7443402b474f3c09144a4fe`  
		Last Modified: Fri, 25 Feb 2022 02:21:39 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d8341c3c348e685617552e338228d15dd937ca0708bd7ab85c3c1b273ed88c`  
		Last Modified: Fri, 25 Feb 2022 02:21:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.3-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:d6f43ae04309c6115c32d1c71469973712b3e817088a449ce37a9e8cb6b86bf9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846b4c8922b69a90d198633a7b622da89348aa9e3f7f11f58a294e2c4b112a33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:49:34 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:49:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:49:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:49:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:49:39 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:49:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:49:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecb484648e454aaf42c41938db64a0715cb509a90811b5912192d2e66a2f7fb`  
		Last Modified: Fri, 25 Feb 2022 02:51:52 GMT  
		Size: 4.4 MB (4439176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd675987846849cf3247fbc41b25505410823bffd30e841e7f663936458e553`  
		Last Modified: Fri, 25 Feb 2022 02:51:49 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae450e4bdcdcad0dc3e04a43f8855409627f6c7fdecd22f661dbfe3a99530d2`  
		Last Modified: Fri, 25 Feb 2022 02:51:49 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.3-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:665c6221a3c009747c340953834a8e1c6e38008d728f3a9d4d4eaab76e8e640d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6865015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23f21c3235ba9d61b53aeb161021b62412dc690dd81727439de14a1f9b902eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:57:52 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:57:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:57:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:57:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:57:58 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:57:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:57:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fafd4ba596baa033665a46ce765df0c4a928784832ecc5645944032cfcd9295`  
		Last Modified: Fri, 25 Feb 2022 03:00:20 GMT  
		Size: 4.4 MB (4429250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb2edff52bc9250fdec4032d39728784d4495539ef65cceed401a8968ec2df5`  
		Last Modified: Fri, 25 Feb 2022 03:00:18 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1047f2aa448d4163e2995aed662d6890fdd3954289a1ff2908edc894450b3d78`  
		Last Modified: Fri, 25 Feb 2022 03:00:18 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.3-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8f79d8af0b084884d2cc9641a33a1274022fc51b99e955d3f13d9c45f47cf6b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7132810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50bb490b2ac0a89152a29fc28e269300b6b83d2a85c0ce5ebe74635c34cdb0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:01:24 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 03:01:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 03:01:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 03:01:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 03:01:29 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:01:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c75ed4d21bde940c8f5b4d0d82b44c31489bd5a37d46b1f197b7d1baed0b6e8`  
		Last Modified: Fri, 25 Feb 2022 03:02:31 GMT  
		Size: 4.4 MB (4416403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7dd0d82f2c731b21df156c69326c651274a35eb010b23b5150397309110717`  
		Last Modified: Fri, 25 Feb 2022 03:02:30 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f29d0f81d7bbfb90bc5607be41aabbd3e970b1e74e19a069c23e863092772ba`  
		Last Modified: Fri, 25 Feb 2022 03:02:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.3-linux`

```console
$ docker pull nats@sha256:4fe2c16e211795858e7e7538197ec57f67ed6e9ca5d91d06d925e09ec6724d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.3-linux` - linux; amd64

```console
$ docker pull nats@sha256:5fd249efa75cf3eb595342175207fdbb390eee3034f7fe49355d7a479fa3ffe2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84de17b17b3458d2b6e6d4264ea6186c82bab718ca058f5d7738e53ca2759ac`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:8a814b0c66a47e63e5a7f4287478948812fe6e03c224d539f37ce3f950d2b6c6 in /nats-server 
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:21:14 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:21:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:277fae1baf41821774f7a2e1c3f465b28aa8693ee0cd77e0ad0bace55d9c616e`  
		Last Modified: Fri, 25 Feb 2022 02:22:04 GMT  
		Size: 4.5 MB (4498900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb932b4b3fbc873b56e996c6357055bb7700c701d17d7d87cdec31211142b49a`  
		Last Modified: Fri, 25 Feb 2022 02:22:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.3-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:2e3339e7e8d98e7bbab0613c7b7c3dd6f51fcf33ed3910a2e65e62fba7049337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc7bcc78dd550ace4def82e3db227e618d77e136274749f3bf55869e64be264`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:3a951d885f7bcec693f6fbf26a9ffd82b0c6218b6834fc6053e5812f7451b63e in /nats-server 
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:50:07 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:50:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:50:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6de87b4530f922b11edc08be8edeebc6ce0cb666907013348d4e1b9f5d51809`  
		Last Modified: Fri, 25 Feb 2022 02:52:29 GMT  
		Size: 4.2 MB (4165468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fa68b52226484e5870677184cdc47c93a7d453f334c144b5cb631346bc8111`  
		Last Modified: Fri, 25 Feb 2022 02:52:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.3-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:87cf3f8e33ebf28f35575ea083f8feb460d19fa9380d2622c82567ff3fa9d840
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eef99b95e572b23f90d60e6e157be90b05ab2f35dbcb10f83f96ece551945a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:3ee879939ad264e803dd4d6072181d968c4dd0fe076115159f70479c6309ef45 in /nats-server 
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:58:35 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:58:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67a3d8907097b9caffd9d1720b4fb2b1d2ac9dfda60a1d169abbf5494323d50a`  
		Last Modified: Fri, 25 Feb 2022 03:00:58 GMT  
		Size: 4.2 MB (4157409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5577f4846f032b281220b897161962481198ead0a1b9ad1d7c76cdd989747`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.3-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e970861a260709ae1e8c892eb36758c14323e81959ff4aaa1e9b7327b91d3e70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4414e48026697a15338f28dcb8e46ace9627ea7332559e1708f36ce62a5e327`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 03:01:42 GMT
COPY file:acd11e9a3a86f6f3da079c5155851337e747c3b31481ec05e2dd1e48e23becb2 in /nats-server 
# Fri, 25 Feb 2022 03:01:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 03:01:43 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 03:01:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6ad9fd47af885b43442590ad2c8171e4b4899caef84921ec73ba0540b9c03284`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 4.1 MB (4143299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7667f81936503f26a5ed657cfffdc9add626da8ae5bb78d691054cd3af7c3`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.3-nanoserver`

```console
$ docker pull nats@sha256:17a7ba92d7d9e30b2ade1940d64a5f64ea45274342f23bce8aec50f7c7c0079a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7.3-nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:90209bda1cad3ec772bc2677672f501958ee7d62c33edfa857dc1716bda9220b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107602854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07847f304e7f8ec4f2b589a503ef48b8ec40f915777bb525440734cb80354bfe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:d5609a37f534b519fa4326428362ea5398f7165ee90493fb7bdc8b810da33b0e in C:\nats-server.exe 
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:40:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:40:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:40:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faa5157704c1d4e58658a58ee4a6c9c9311a1d1fad5bed72177cbe21cf41dcb`  
		Last Modified: Wed, 09 Mar 2022 16:41:04 GMT  
		Size: 4.5 MB (4541860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa65daf1bc9817f903056d7a32becb96a3c4ae626707c391c115f9672dd19f9`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ca210f6c322c3169919cabf4b4814ab663aa766949d78aa18e5e52bbc9c7b7`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa906eba8a8100c8da6161e182387637cb7d3e7272ba27fb859f8c511abc7ba4`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a943f384f132c325e714fb870d67abbfbde1e4ffb1379784d990e39e0e3913`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.3-nanoserver-1809`

```console
$ docker pull nats@sha256:17a7ba92d7d9e30b2ade1940d64a5f64ea45274342f23bce8aec50f7c7c0079a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7.3-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:90209bda1cad3ec772bc2677672f501958ee7d62c33edfa857dc1716bda9220b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107602854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07847f304e7f8ec4f2b589a503ef48b8ec40f915777bb525440734cb80354bfe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:d5609a37f534b519fa4326428362ea5398f7165ee90493fb7bdc8b810da33b0e in C:\nats-server.exe 
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:40:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:40:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:40:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faa5157704c1d4e58658a58ee4a6c9c9311a1d1fad5bed72177cbe21cf41dcb`  
		Last Modified: Wed, 09 Mar 2022 16:41:04 GMT  
		Size: 4.5 MB (4541860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa65daf1bc9817f903056d7a32becb96a3c4ae626707c391c115f9672dd19f9`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ca210f6c322c3169919cabf4b4814ab663aa766949d78aa18e5e52bbc9c7b7`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa906eba8a8100c8da6161e182387637cb7d3e7272ba27fb859f8c511abc7ba4`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a943f384f132c325e714fb870d67abbfbde1e4ffb1379784d990e39e0e3913`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.3-scratch`

```console
$ docker pull nats@sha256:4fe2c16e211795858e7e7538197ec57f67ed6e9ca5d91d06d925e09ec6724d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.3-scratch` - linux; amd64

```console
$ docker pull nats@sha256:5fd249efa75cf3eb595342175207fdbb390eee3034f7fe49355d7a479fa3ffe2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84de17b17b3458d2b6e6d4264ea6186c82bab718ca058f5d7738e53ca2759ac`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:8a814b0c66a47e63e5a7f4287478948812fe6e03c224d539f37ce3f950d2b6c6 in /nats-server 
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:21:14 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:21:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:277fae1baf41821774f7a2e1c3f465b28aa8693ee0cd77e0ad0bace55d9c616e`  
		Last Modified: Fri, 25 Feb 2022 02:22:04 GMT  
		Size: 4.5 MB (4498900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb932b4b3fbc873b56e996c6357055bb7700c701d17d7d87cdec31211142b49a`  
		Last Modified: Fri, 25 Feb 2022 02:22:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.3-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:2e3339e7e8d98e7bbab0613c7b7c3dd6f51fcf33ed3910a2e65e62fba7049337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc7bcc78dd550ace4def82e3db227e618d77e136274749f3bf55869e64be264`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:3a951d885f7bcec693f6fbf26a9ffd82b0c6218b6834fc6053e5812f7451b63e in /nats-server 
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:50:07 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:50:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:50:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6de87b4530f922b11edc08be8edeebc6ce0cb666907013348d4e1b9f5d51809`  
		Last Modified: Fri, 25 Feb 2022 02:52:29 GMT  
		Size: 4.2 MB (4165468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fa68b52226484e5870677184cdc47c93a7d453f334c144b5cb631346bc8111`  
		Last Modified: Fri, 25 Feb 2022 02:52:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.3-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:87cf3f8e33ebf28f35575ea083f8feb460d19fa9380d2622c82567ff3fa9d840
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eef99b95e572b23f90d60e6e157be90b05ab2f35dbcb10f83f96ece551945a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:3ee879939ad264e803dd4d6072181d968c4dd0fe076115159f70479c6309ef45 in /nats-server 
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:58:35 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:58:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67a3d8907097b9caffd9d1720b4fb2b1d2ac9dfda60a1d169abbf5494323d50a`  
		Last Modified: Fri, 25 Feb 2022 03:00:58 GMT  
		Size: 4.2 MB (4157409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5577f4846f032b281220b897161962481198ead0a1b9ad1d7c76cdd989747`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.3-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e970861a260709ae1e8c892eb36758c14323e81959ff4aaa1e9b7327b91d3e70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4414e48026697a15338f28dcb8e46ace9627ea7332559e1708f36ce62a5e327`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 03:01:42 GMT
COPY file:acd11e9a3a86f6f3da079c5155851337e747c3b31481ec05e2dd1e48e23becb2 in /nats-server 
# Fri, 25 Feb 2022 03:01:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 03:01:43 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 03:01:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6ad9fd47af885b43442590ad2c8171e4b4899caef84921ec73ba0540b9c03284`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 4.1 MB (4143299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7667f81936503f26a5ed657cfffdc9add626da8ae5bb78d691054cd3af7c3`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.3-windowsservercore`

```console
$ docker pull nats@sha256:73e27c192194143e9b62c4f2ded2984b5675129b8657d9736845bcce6621cfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7.3-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:e1ff01e9229d5c7bec881c29fbeb094ef95b03e54a80f66f0e65fbe41a33bb4f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720683253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd5fd97f45903baa3340c5695af50b2d1ed687b8a10e52d1f64d26c98161a5f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:36:40 GMT
ENV NATS_SERVER=2.7.3
# Wed, 09 Mar 2022 16:36:41 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.3/nats-server-v2.7.3-windows-amd64.zip
# Wed, 09 Mar 2022 16:36:42 GMT
ENV NATS_SERVER_SHASUM=ddb372da68741d897006c8d4b160c7f4788603cbaacb3fa105ddf7baada04428
# Wed, 09 Mar 2022 16:38:04 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 16:39:51 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 16:39:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:39:53 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:39:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:39:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e42c5b8ce3d2860dee66c1b5a94f8984a7164e8821a7730b2a2f3ae2ab3574`  
		Last Modified: Wed, 09 Mar 2022 16:40:42 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf812b1cfcec29602d107bef7e05f2c42661e6de68d06f42a6a50444bdfe0cb`  
		Last Modified: Wed, 09 Mar 2022 16:40:42 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4408e08c023d4b1c45f075bfdf96f67d7f0e09376be774314dd45c56ab1bd01d`  
		Last Modified: Wed, 09 Mar 2022 16:40:43 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d548cdcfc93bc734d4de576e696a2cdd3088415d58fedc3b9888e2a8a8c9e4b`  
		Last Modified: Wed, 09 Mar 2022 16:40:43 GMT  
		Size: 349.8 KB (349760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd44951b18faf73d172b09675cbb05b8f9da0d304fa69141e9c317015e2126a6`  
		Last Modified: Wed, 09 Mar 2022 16:40:41 GMT  
		Size: 4.9 MB (4867494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc91fe37c5dfe9f191cd5f4612758e1dd9320b570ab236f45b76afa49a16b7b`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c93c11781e7cd21ad6b3b0eec7bc6a86e0c9076512fe83fb39f3c9eab62a05`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b639b85df7a056548a52711dfe322991b5fe92f311037f385e9788ffe8ae1aa4`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8667684816445549d2ee046f4686fd6e753de7ecebcedb42f8e517fff3989fbd`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.3-windowsservercore-1809`

```console
$ docker pull nats@sha256:73e27c192194143e9b62c4f2ded2984b5675129b8657d9736845bcce6621cfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:2.7.3-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:e1ff01e9229d5c7bec881c29fbeb094ef95b03e54a80f66f0e65fbe41a33bb4f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720683253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd5fd97f45903baa3340c5695af50b2d1ed687b8a10e52d1f64d26c98161a5f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:36:40 GMT
ENV NATS_SERVER=2.7.3
# Wed, 09 Mar 2022 16:36:41 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.3/nats-server-v2.7.3-windows-amd64.zip
# Wed, 09 Mar 2022 16:36:42 GMT
ENV NATS_SERVER_SHASUM=ddb372da68741d897006c8d4b160c7f4788603cbaacb3fa105ddf7baada04428
# Wed, 09 Mar 2022 16:38:04 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 16:39:51 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 16:39:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:39:53 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:39:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:39:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e42c5b8ce3d2860dee66c1b5a94f8984a7164e8821a7730b2a2f3ae2ab3574`  
		Last Modified: Wed, 09 Mar 2022 16:40:42 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf812b1cfcec29602d107bef7e05f2c42661e6de68d06f42a6a50444bdfe0cb`  
		Last Modified: Wed, 09 Mar 2022 16:40:42 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4408e08c023d4b1c45f075bfdf96f67d7f0e09376be774314dd45c56ab1bd01d`  
		Last Modified: Wed, 09 Mar 2022 16:40:43 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d548cdcfc93bc734d4de576e696a2cdd3088415d58fedc3b9888e2a8a8c9e4b`  
		Last Modified: Wed, 09 Mar 2022 16:40:43 GMT  
		Size: 349.8 KB (349760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd44951b18faf73d172b09675cbb05b8f9da0d304fa69141e9c317015e2126a6`  
		Last Modified: Wed, 09 Mar 2022 16:40:41 GMT  
		Size: 4.9 MB (4867494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc91fe37c5dfe9f191cd5f4612758e1dd9320b570ab236f45b76afa49a16b7b`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c93c11781e7cd21ad6b3b0eec7bc6a86e0c9076512fe83fb39f3c9eab62a05`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b639b85df7a056548a52711dfe322991b5fe92f311037f385e9788ffe8ae1aa4`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8667684816445549d2ee046f4686fd6e753de7ecebcedb42f8e517fff3989fbd`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:6944283c7d430ef4d5e23afb87b2a2d9faf963793bcd94b0461bc12def6c74c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:6f8d631c068a9d37845ebee434d2c37606757634b9d8950e8de1035dc68842b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7591453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775ec723ebf4c964b880457f54f66782e850e7121d3264c851da7d58cddb64bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:21:01 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:21:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:21:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:21:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:21:04 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:21:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfad251bce41e482876302125c33ef603e0ca99f33d1d274a09af07e1acd1be6`  
		Last Modified: Fri, 25 Feb 2022 02:21:40 GMT  
		Size: 4.8 MB (4772040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c6f8e0dbab2106f703f51433a684cef43840e5e7443402b474f3c09144a4fe`  
		Last Modified: Fri, 25 Feb 2022 02:21:39 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d8341c3c348e685617552e338228d15dd937ca0708bd7ab85c3c1b273ed88c`  
		Last Modified: Fri, 25 Feb 2022 02:21:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d6f43ae04309c6115c32d1c71469973712b3e817088a449ce37a9e8cb6b86bf9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846b4c8922b69a90d198633a7b622da89348aa9e3f7f11f58a294e2c4b112a33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:49:34 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:49:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:49:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:49:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:49:39 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:49:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:49:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecb484648e454aaf42c41938db64a0715cb509a90811b5912192d2e66a2f7fb`  
		Last Modified: Fri, 25 Feb 2022 02:51:52 GMT  
		Size: 4.4 MB (4439176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd675987846849cf3247fbc41b25505410823bffd30e841e7f663936458e553`  
		Last Modified: Fri, 25 Feb 2022 02:51:49 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae450e4bdcdcad0dc3e04a43f8855409627f6c7fdecd22f661dbfe3a99530d2`  
		Last Modified: Fri, 25 Feb 2022 02:51:49 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:665c6221a3c009747c340953834a8e1c6e38008d728f3a9d4d4eaab76e8e640d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6865015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23f21c3235ba9d61b53aeb161021b62412dc690dd81727439de14a1f9b902eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:57:52 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:57:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:57:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:57:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:57:58 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:57:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:57:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fafd4ba596baa033665a46ce765df0c4a928784832ecc5645944032cfcd9295`  
		Last Modified: Fri, 25 Feb 2022 03:00:20 GMT  
		Size: 4.4 MB (4429250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb2edff52bc9250fdec4032d39728784d4495539ef65cceed401a8968ec2df5`  
		Last Modified: Fri, 25 Feb 2022 03:00:18 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1047f2aa448d4163e2995aed662d6890fdd3954289a1ff2908edc894450b3d78`  
		Last Modified: Fri, 25 Feb 2022 03:00:18 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8f79d8af0b084884d2cc9641a33a1274022fc51b99e955d3f13d9c45f47cf6b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7132810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50bb490b2ac0a89152a29fc28e269300b6b83d2a85c0ce5ebe74635c34cdb0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:01:24 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 03:01:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 03:01:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 03:01:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 03:01:29 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:01:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c75ed4d21bde940c8f5b4d0d82b44c31489bd5a37d46b1f197b7d1baed0b6e8`  
		Last Modified: Fri, 25 Feb 2022 03:02:31 GMT  
		Size: 4.4 MB (4416403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7dd0d82f2c731b21df156c69326c651274a35eb010b23b5150397309110717`  
		Last Modified: Fri, 25 Feb 2022 03:02:30 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f29d0f81d7bbfb90bc5607be41aabbd3e970b1e74e19a069c23e863092772ba`  
		Last Modified: Fri, 25 Feb 2022 03:02:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.15`

```console
$ docker pull nats@sha256:6944283c7d430ef4d5e23afb87b2a2d9faf963793bcd94b0461bc12def6c74c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:6f8d631c068a9d37845ebee434d2c37606757634b9d8950e8de1035dc68842b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7591453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775ec723ebf4c964b880457f54f66782e850e7121d3264c851da7d58cddb64bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:21:01 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:21:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:21:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:21:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:21:04 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:21:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfad251bce41e482876302125c33ef603e0ca99f33d1d274a09af07e1acd1be6`  
		Last Modified: Fri, 25 Feb 2022 02:21:40 GMT  
		Size: 4.8 MB (4772040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c6f8e0dbab2106f703f51433a684cef43840e5e7443402b474f3c09144a4fe`  
		Last Modified: Fri, 25 Feb 2022 02:21:39 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d8341c3c348e685617552e338228d15dd937ca0708bd7ab85c3c1b273ed88c`  
		Last Modified: Fri, 25 Feb 2022 02:21:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:d6f43ae04309c6115c32d1c71469973712b3e817088a449ce37a9e8cb6b86bf9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846b4c8922b69a90d198633a7b622da89348aa9e3f7f11f58a294e2c4b112a33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:49:34 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:49:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:49:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:49:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:49:39 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:49:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:49:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecb484648e454aaf42c41938db64a0715cb509a90811b5912192d2e66a2f7fb`  
		Last Modified: Fri, 25 Feb 2022 02:51:52 GMT  
		Size: 4.4 MB (4439176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd675987846849cf3247fbc41b25505410823bffd30e841e7f663936458e553`  
		Last Modified: Fri, 25 Feb 2022 02:51:49 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae450e4bdcdcad0dc3e04a43f8855409627f6c7fdecd22f661dbfe3a99530d2`  
		Last Modified: Fri, 25 Feb 2022 02:51:49 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:665c6221a3c009747c340953834a8e1c6e38008d728f3a9d4d4eaab76e8e640d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6865015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23f21c3235ba9d61b53aeb161021b62412dc690dd81727439de14a1f9b902eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 02:57:52 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 02:57:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 02:57:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 02:57:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 02:57:58 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:57:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 02:57:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fafd4ba596baa033665a46ce765df0c4a928784832ecc5645944032cfcd9295`  
		Last Modified: Fri, 25 Feb 2022 03:00:20 GMT  
		Size: 4.4 MB (4429250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb2edff52bc9250fdec4032d39728784d4495539ef65cceed401a8968ec2df5`  
		Last Modified: Fri, 25 Feb 2022 03:00:18 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1047f2aa448d4163e2995aed662d6890fdd3954289a1ff2908edc894450b3d78`  
		Last Modified: Fri, 25 Feb 2022 03:00:18 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8f79d8af0b084884d2cc9641a33a1274022fc51b99e955d3f13d9c45f47cf6b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7132810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50bb490b2ac0a89152a29fc28e269300b6b83d2a85c0ce5ebe74635c34cdb0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Fri, 25 Feb 2022 03:01:24 GMT
ENV NATS_SERVER=2.7.3
# Fri, 25 Feb 2022 03:01:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c895169ab34bc21442121f6c885905a254a9351a098402f319b3fbfd1e6225c9' ;; 		armhf) natsArch='arm6'; sha256='1b7e1c5835131825c4007766befd0c96a60edbcc3bc336a6739de5c8affea0c4' ;; 		armv7) natsArch='arm7'; sha256='723290467bc7e95b59ca7238a818932b199b00a21d4e3d7eb0e826b7aba2e0ea' ;; 		x86_64) natsArch='amd64'; sha256='2186c7660cd1d9774421614f6724ad32d7cec2389e39858f227a7991be41b1a7' ;; 		x86) natsArch='386'; sha256='3e8e2841921d555d06c67b1e33fc9bd934e4afec4748f7ddf27c67d707fafea4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 25 Feb 2022 03:01:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 25 Feb 2022 03:01:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 25 Feb 2022 03:01:29 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 03:01:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c75ed4d21bde940c8f5b4d0d82b44c31489bd5a37d46b1f197b7d1baed0b6e8`  
		Last Modified: Fri, 25 Feb 2022 03:02:31 GMT  
		Size: 4.4 MB (4416403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7dd0d82f2c731b21df156c69326c651274a35eb010b23b5150397309110717`  
		Last Modified: Fri, 25 Feb 2022 03:02:30 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f29d0f81d7bbfb90bc5607be41aabbd3e970b1e74e19a069c23e863092772ba`  
		Last Modified: Fri, 25 Feb 2022 03:02:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:a66bd53bc5fa8c23dc87b2d366d4e5d3987b75ad479a1c53e7f1dcfdf418d942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2686; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:5fd249efa75cf3eb595342175207fdbb390eee3034f7fe49355d7a479fa3ffe2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84de17b17b3458d2b6e6d4264ea6186c82bab718ca058f5d7738e53ca2759ac`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:8a814b0c66a47e63e5a7f4287478948812fe6e03c224d539f37ce3f950d2b6c6 in /nats-server 
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:21:14 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:21:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:277fae1baf41821774f7a2e1c3f465b28aa8693ee0cd77e0ad0bace55d9c616e`  
		Last Modified: Fri, 25 Feb 2022 02:22:04 GMT  
		Size: 4.5 MB (4498900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb932b4b3fbc873b56e996c6357055bb7700c701d17d7d87cdec31211142b49a`  
		Last Modified: Fri, 25 Feb 2022 02:22:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:2e3339e7e8d98e7bbab0613c7b7c3dd6f51fcf33ed3910a2e65e62fba7049337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc7bcc78dd550ace4def82e3db227e618d77e136274749f3bf55869e64be264`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:3a951d885f7bcec693f6fbf26a9ffd82b0c6218b6834fc6053e5812f7451b63e in /nats-server 
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:50:07 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:50:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:50:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6de87b4530f922b11edc08be8edeebc6ce0cb666907013348d4e1b9f5d51809`  
		Last Modified: Fri, 25 Feb 2022 02:52:29 GMT  
		Size: 4.2 MB (4165468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fa68b52226484e5870677184cdc47c93a7d453f334c144b5cb631346bc8111`  
		Last Modified: Fri, 25 Feb 2022 02:52:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:87cf3f8e33ebf28f35575ea083f8feb460d19fa9380d2622c82567ff3fa9d840
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eef99b95e572b23f90d60e6e157be90b05ab2f35dbcb10f83f96ece551945a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:3ee879939ad264e803dd4d6072181d968c4dd0fe076115159f70479c6309ef45 in /nats-server 
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:58:35 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:58:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67a3d8907097b9caffd9d1720b4fb2b1d2ac9dfda60a1d169abbf5494323d50a`  
		Last Modified: Fri, 25 Feb 2022 03:00:58 GMT  
		Size: 4.2 MB (4157409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5577f4846f032b281220b897161962481198ead0a1b9ad1d7c76cdd989747`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e970861a260709ae1e8c892eb36758c14323e81959ff4aaa1e9b7327b91d3e70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4414e48026697a15338f28dcb8e46ace9627ea7332559e1708f36ce62a5e327`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 03:01:42 GMT
COPY file:acd11e9a3a86f6f3da079c5155851337e747c3b31481ec05e2dd1e48e23becb2 in /nats-server 
# Fri, 25 Feb 2022 03:01:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 03:01:43 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 03:01:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6ad9fd47af885b43442590ad2c8171e4b4899caef84921ec73ba0540b9c03284`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 4.1 MB (4143299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7667f81936503f26a5ed657cfffdc9add626da8ae5bb78d691054cd3af7c3`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:90209bda1cad3ec772bc2677672f501958ee7d62c33edfa857dc1716bda9220b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107602854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07847f304e7f8ec4f2b589a503ef48b8ec40f915777bb525440734cb80354bfe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:d5609a37f534b519fa4326428362ea5398f7165ee90493fb7bdc8b810da33b0e in C:\nats-server.exe 
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:40:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:40:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:40:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faa5157704c1d4e58658a58ee4a6c9c9311a1d1fad5bed72177cbe21cf41dcb`  
		Last Modified: Wed, 09 Mar 2022 16:41:04 GMT  
		Size: 4.5 MB (4541860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa65daf1bc9817f903056d7a32becb96a3c4ae626707c391c115f9672dd19f9`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ca210f6c322c3169919cabf4b4814ab663aa766949d78aa18e5e52bbc9c7b7`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa906eba8a8100c8da6161e182387637cb7d3e7272ba27fb859f8c511abc7ba4`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a943f384f132c325e714fb870d67abbfbde1e4ffb1379784d990e39e0e3913`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:4fe2c16e211795858e7e7538197ec57f67ed6e9ca5d91d06d925e09ec6724d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:5fd249efa75cf3eb595342175207fdbb390eee3034f7fe49355d7a479fa3ffe2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84de17b17b3458d2b6e6d4264ea6186c82bab718ca058f5d7738e53ca2759ac`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:8a814b0c66a47e63e5a7f4287478948812fe6e03c224d539f37ce3f950d2b6c6 in /nats-server 
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:21:14 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:21:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:277fae1baf41821774f7a2e1c3f465b28aa8693ee0cd77e0ad0bace55d9c616e`  
		Last Modified: Fri, 25 Feb 2022 02:22:04 GMT  
		Size: 4.5 MB (4498900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb932b4b3fbc873b56e996c6357055bb7700c701d17d7d87cdec31211142b49a`  
		Last Modified: Fri, 25 Feb 2022 02:22:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:2e3339e7e8d98e7bbab0613c7b7c3dd6f51fcf33ed3910a2e65e62fba7049337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc7bcc78dd550ace4def82e3db227e618d77e136274749f3bf55869e64be264`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:3a951d885f7bcec693f6fbf26a9ffd82b0c6218b6834fc6053e5812f7451b63e in /nats-server 
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:50:07 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:50:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:50:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6de87b4530f922b11edc08be8edeebc6ce0cb666907013348d4e1b9f5d51809`  
		Last Modified: Fri, 25 Feb 2022 02:52:29 GMT  
		Size: 4.2 MB (4165468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fa68b52226484e5870677184cdc47c93a7d453f334c144b5cb631346bc8111`  
		Last Modified: Fri, 25 Feb 2022 02:52:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:87cf3f8e33ebf28f35575ea083f8feb460d19fa9380d2622c82567ff3fa9d840
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eef99b95e572b23f90d60e6e157be90b05ab2f35dbcb10f83f96ece551945a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:3ee879939ad264e803dd4d6072181d968c4dd0fe076115159f70479c6309ef45 in /nats-server 
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:58:35 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:58:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67a3d8907097b9caffd9d1720b4fb2b1d2ac9dfda60a1d169abbf5494323d50a`  
		Last Modified: Fri, 25 Feb 2022 03:00:58 GMT  
		Size: 4.2 MB (4157409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5577f4846f032b281220b897161962481198ead0a1b9ad1d7c76cdd989747`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e970861a260709ae1e8c892eb36758c14323e81959ff4aaa1e9b7327b91d3e70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4414e48026697a15338f28dcb8e46ace9627ea7332559e1708f36ce62a5e327`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 03:01:42 GMT
COPY file:acd11e9a3a86f6f3da079c5155851337e747c3b31481ec05e2dd1e48e23becb2 in /nats-server 
# Fri, 25 Feb 2022 03:01:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 03:01:43 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 03:01:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6ad9fd47af885b43442590ad2c8171e4b4899caef84921ec73ba0540b9c03284`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 4.1 MB (4143299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7667f81936503f26a5ed657cfffdc9add626da8ae5bb78d691054cd3af7c3`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:17a7ba92d7d9e30b2ade1940d64a5f64ea45274342f23bce8aec50f7c7c0079a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:90209bda1cad3ec772bc2677672f501958ee7d62c33edfa857dc1716bda9220b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107602854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07847f304e7f8ec4f2b589a503ef48b8ec40f915777bb525440734cb80354bfe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:d5609a37f534b519fa4326428362ea5398f7165ee90493fb7bdc8b810da33b0e in C:\nats-server.exe 
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:40:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:40:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:40:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faa5157704c1d4e58658a58ee4a6c9c9311a1d1fad5bed72177cbe21cf41dcb`  
		Last Modified: Wed, 09 Mar 2022 16:41:04 GMT  
		Size: 4.5 MB (4541860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa65daf1bc9817f903056d7a32becb96a3c4ae626707c391c115f9672dd19f9`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ca210f6c322c3169919cabf4b4814ab663aa766949d78aa18e5e52bbc9c7b7`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa906eba8a8100c8da6161e182387637cb7d3e7272ba27fb859f8c511abc7ba4`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a943f384f132c325e714fb870d67abbfbde1e4ffb1379784d990e39e0e3913`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:17a7ba92d7d9e30b2ade1940d64a5f64ea45274342f23bce8aec50f7c7c0079a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:90209bda1cad3ec772bc2677672f501958ee7d62c33edfa857dc1716bda9220b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107602854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07847f304e7f8ec4f2b589a503ef48b8ec40f915777bb525440734cb80354bfe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Wed, 09 Mar 2022 16:40:09 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:d5609a37f534b519fa4326428362ea5398f7165ee90493fb7bdc8b810da33b0e in C:\nats-server.exe 
# Wed, 09 Mar 2022 16:40:10 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:40:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:40:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:40:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6bc8e7abd2b889d7f3d81ab72c0dc6f44c22859ff125c228ec1147cd803c7e6c`  
		Last Modified: Wed, 09 Mar 2022 16:41:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faa5157704c1d4e58658a58ee4a6c9c9311a1d1fad5bed72177cbe21cf41dcb`  
		Last Modified: Wed, 09 Mar 2022 16:41:04 GMT  
		Size: 4.5 MB (4541860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa65daf1bc9817f903056d7a32becb96a3c4ae626707c391c115f9672dd19f9`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ca210f6c322c3169919cabf4b4814ab663aa766949d78aa18e5e52bbc9c7b7`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa906eba8a8100c8da6161e182387637cb7d3e7272ba27fb859f8c511abc7ba4`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a943f384f132c325e714fb870d67abbfbde1e4ffb1379784d990e39e0e3913`  
		Last Modified: Wed, 09 Mar 2022 16:40:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:4fe2c16e211795858e7e7538197ec57f67ed6e9ca5d91d06d925e09ec6724d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:5fd249efa75cf3eb595342175207fdbb390eee3034f7fe49355d7a479fa3ffe2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4499407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84de17b17b3458d2b6e6d4264ea6186c82bab718ca058f5d7738e53ca2759ac`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:8a814b0c66a47e63e5a7f4287478948812fe6e03c224d539f37ce3f950d2b6c6 in /nats-server 
# Fri, 25 Feb 2022 02:21:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:21:14 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:21:14 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:21:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:277fae1baf41821774f7a2e1c3f465b28aa8693ee0cd77e0ad0bace55d9c616e`  
		Last Modified: Fri, 25 Feb 2022 02:22:04 GMT  
		Size: 4.5 MB (4498900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb932b4b3fbc873b56e996c6357055bb7700c701d17d7d87cdec31211142b49a`  
		Last Modified: Fri, 25 Feb 2022 02:22:03 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:2e3339e7e8d98e7bbab0613c7b7c3dd6f51fcf33ed3910a2e65e62fba7049337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc7bcc78dd550ace4def82e3db227e618d77e136274749f3bf55869e64be264`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:3a951d885f7bcec693f6fbf26a9ffd82b0c6218b6834fc6053e5812f7451b63e in /nats-server 
# Fri, 25 Feb 2022 02:50:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:50:07 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:50:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:50:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6de87b4530f922b11edc08be8edeebc6ce0cb666907013348d4e1b9f5d51809`  
		Last Modified: Fri, 25 Feb 2022 02:52:29 GMT  
		Size: 4.2 MB (4165468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fa68b52226484e5870677184cdc47c93a7d453f334c144b5cb631346bc8111`  
		Last Modified: Fri, 25 Feb 2022 02:52:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:87cf3f8e33ebf28f35575ea083f8feb460d19fa9380d2622c82567ff3fa9d840
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eef99b95e572b23f90d60e6e157be90b05ab2f35dbcb10f83f96ece551945a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:3ee879939ad264e803dd4d6072181d968c4dd0fe076115159f70479c6309ef45 in /nats-server 
# Fri, 25 Feb 2022 02:58:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 02:58:35 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 02:58:35 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 02:58:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67a3d8907097b9caffd9d1720b4fb2b1d2ac9dfda60a1d169abbf5494323d50a`  
		Last Modified: Fri, 25 Feb 2022 03:00:58 GMT  
		Size: 4.2 MB (4157409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f5577f4846f032b281220b897161962481198ead0a1b9ad1d7c76cdd989747`  
		Last Modified: Fri, 25 Feb 2022 03:00:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e970861a260709ae1e8c892eb36758c14323e81959ff4aaa1e9b7327b91d3e70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4414e48026697a15338f28dcb8e46ace9627ea7332559e1708f36ce62a5e327`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Feb 2022 03:01:42 GMT
COPY file:acd11e9a3a86f6f3da079c5155851337e747c3b31481ec05e2dd1e48e23becb2 in /nats-server 
# Fri, 25 Feb 2022 03:01:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 25 Feb 2022 03:01:43 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Feb 2022 03:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Feb 2022 03:01:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6ad9fd47af885b43442590ad2c8171e4b4899caef84921ec73ba0540b9c03284`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 4.1 MB (4143299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7667f81936503f26a5ed657cfffdc9add626da8ae5bb78d691054cd3af7c3`  
		Last Modified: Fri, 25 Feb 2022 03:02:59 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:73e27c192194143e9b62c4f2ded2984b5675129b8657d9736845bcce6621cfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:e1ff01e9229d5c7bec881c29fbeb094ef95b03e54a80f66f0e65fbe41a33bb4f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720683253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd5fd97f45903baa3340c5695af50b2d1ed687b8a10e52d1f64d26c98161a5f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:36:40 GMT
ENV NATS_SERVER=2.7.3
# Wed, 09 Mar 2022 16:36:41 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.3/nats-server-v2.7.3-windows-amd64.zip
# Wed, 09 Mar 2022 16:36:42 GMT
ENV NATS_SERVER_SHASUM=ddb372da68741d897006c8d4b160c7f4788603cbaacb3fa105ddf7baada04428
# Wed, 09 Mar 2022 16:38:04 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 16:39:51 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 16:39:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:39:53 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:39:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:39:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e42c5b8ce3d2860dee66c1b5a94f8984a7164e8821a7730b2a2f3ae2ab3574`  
		Last Modified: Wed, 09 Mar 2022 16:40:42 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf812b1cfcec29602d107bef7e05f2c42661e6de68d06f42a6a50444bdfe0cb`  
		Last Modified: Wed, 09 Mar 2022 16:40:42 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4408e08c023d4b1c45f075bfdf96f67d7f0e09376be774314dd45c56ab1bd01d`  
		Last Modified: Wed, 09 Mar 2022 16:40:43 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d548cdcfc93bc734d4de576e696a2cdd3088415d58fedc3b9888e2a8a8c9e4b`  
		Last Modified: Wed, 09 Mar 2022 16:40:43 GMT  
		Size: 349.8 KB (349760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd44951b18faf73d172b09675cbb05b8f9da0d304fa69141e9c317015e2126a6`  
		Last Modified: Wed, 09 Mar 2022 16:40:41 GMT  
		Size: 4.9 MB (4867494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc91fe37c5dfe9f191cd5f4612758e1dd9320b570ab236f45b76afa49a16b7b`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c93c11781e7cd21ad6b3b0eec7bc6a86e0c9076512fe83fb39f3c9eab62a05`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b639b85df7a056548a52711dfe322991b5fe92f311037f385e9788ffe8ae1aa4`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8667684816445549d2ee046f4686fd6e753de7ecebcedb42f8e517fff3989fbd`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:73e27c192194143e9b62c4f2ded2984b5675129b8657d9736845bcce6621cfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull nats@sha256:e1ff01e9229d5c7bec881c29fbeb094ef95b03e54a80f66f0e65fbe41a33bb4f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720683253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd5fd97f45903baa3340c5695af50b2d1ed687b8a10e52d1f64d26c98161a5f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 20:10:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Mar 2022 16:36:38 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Mar 2022 16:36:40 GMT
ENV NATS_SERVER=2.7.3
# Wed, 09 Mar 2022 16:36:41 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.3/nats-server-v2.7.3-windows-amd64.zip
# Wed, 09 Mar 2022 16:36:42 GMT
ENV NATS_SERVER_SHASUM=ddb372da68741d897006c8d4b160c7f4788603cbaacb3fa105ddf7baada04428
# Wed, 09 Mar 2022 16:38:04 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Mar 2022 16:39:51 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Mar 2022 16:39:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Mar 2022 16:39:53 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Mar 2022 16:39:54 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Mar 2022 16:39:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4688be73f177648e78a5e4d7da9b850d16dafa3dbf1700a2ed3e35e1ffff22ed`  
		Last Modified: Tue, 08 Mar 2022 20:38:24 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431f904a213b56f70ee2943fb5c2ed2f4bcc65a509c6d79fce7ff98cfdfb4956`  
		Last Modified: Wed, 09 Mar 2022 16:40:44 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e42c5b8ce3d2860dee66c1b5a94f8984a7164e8821a7730b2a2f3ae2ab3574`  
		Last Modified: Wed, 09 Mar 2022 16:40:42 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf812b1cfcec29602d107bef7e05f2c42661e6de68d06f42a6a50444bdfe0cb`  
		Last Modified: Wed, 09 Mar 2022 16:40:42 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4408e08c023d4b1c45f075bfdf96f67d7f0e09376be774314dd45c56ab1bd01d`  
		Last Modified: Wed, 09 Mar 2022 16:40:43 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d548cdcfc93bc734d4de576e696a2cdd3088415d58fedc3b9888e2a8a8c9e4b`  
		Last Modified: Wed, 09 Mar 2022 16:40:43 GMT  
		Size: 349.8 KB (349760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd44951b18faf73d172b09675cbb05b8f9da0d304fa69141e9c317015e2126a6`  
		Last Modified: Wed, 09 Mar 2022 16:40:41 GMT  
		Size: 4.9 MB (4867494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc91fe37c5dfe9f191cd5f4612758e1dd9320b570ab236f45b76afa49a16b7b`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c93c11781e7cd21ad6b3b0eec7bc6a86e0c9076512fe83fb39f3c9eab62a05`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b639b85df7a056548a52711dfe322991b5fe92f311037f385e9788ffe8ae1aa4`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8667684816445549d2ee046f4686fd6e753de7ecebcedb42f8e517fff3989fbd`  
		Last Modified: Wed, 09 Mar 2022 16:40:40 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
