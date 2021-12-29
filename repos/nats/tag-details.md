<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.14`](#nats2-alpine314)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2-windowsservercore-ltsc2016`](#nats2-windowsservercore-ltsc2016)
-	[`nats:2.6`](#nats26)
-	[`nats:2.6-alpine`](#nats26-alpine)
-	[`nats:2.6-alpine3.14`](#nats26-alpine314)
-	[`nats:2.6-linux`](#nats26-linux)
-	[`nats:2.6-nanoserver`](#nats26-nanoserver)
-	[`nats:2.6-nanoserver-1809`](#nats26-nanoserver-1809)
-	[`nats:2.6-scratch`](#nats26-scratch)
-	[`nats:2.6-windowsservercore`](#nats26-windowsservercore)
-	[`nats:2.6-windowsservercore-1809`](#nats26-windowsservercore-1809)
-	[`nats:2.6-windowsservercore-ltsc2016`](#nats26-windowsservercore-ltsc2016)
-	[`nats:2.6.6`](#nats266)
-	[`nats:2.6.6-alpine`](#nats266-alpine)
-	[`nats:2.6.6-alpine3.14`](#nats266-alpine314)
-	[`nats:2.6.6-linux`](#nats266-linux)
-	[`nats:2.6.6-nanoserver`](#nats266-nanoserver)
-	[`nats:2.6.6-nanoserver-1809`](#nats266-nanoserver-1809)
-	[`nats:2.6.6-scratch`](#nats266-scratch)
-	[`nats:2.6.6-windowsservercore`](#nats266-windowsservercore)
-	[`nats:2.6.6-windowsservercore-1809`](#nats266-windowsservercore-1809)
-	[`nats:2.6.6-windowsservercore-ltsc2016`](#nats266-windowsservercore-ltsc2016)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.14`](#natsalpine314)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)
-	[`nats:windowsservercore-ltsc2016`](#natswindowsservercore-ltsc2016)

## `nats:2`

```console
$ docker pull nats@sha256:4d4b166c324b4e9f0853e36d62cf831c5e4bd089fc6c5932ad9a98a8f73a143e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2366; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:dad4f69520337c2a80d2a9123963c971836f07f530cf4b7c56dde98a622e0a6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba73da93bdda8525a9f473851ee3de9a2d23c21e1d0a51d7da118bc122df420`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 21:23:03 GMT
COPY file:4070919cac43aa01e3ef5dd95589f24a9d649dcc7b4d6364927c764b1f90392e in /nats-server 
# Fri, 03 Dec 2021 21:23:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 21:23:04 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:23:04 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 21:23:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:730cae3de796bb1fbb06f0f847317c2b738bf9af9d1233daafcf2f708eade5ec`  
		Last Modified: Fri, 03 Dec 2021 21:24:01 GMT  
		Size: 4.6 MB (4577696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39027e71725d02ee81938943fd0f3e980f01abbe21c5e8f8ea8219687aaae862`  
		Last Modified: Fri, 03 Dec 2021 21:24:00 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:78ee1d57413d89c46e808dbb121ad895537b74af783c6e6189366afa07638b66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3276dd6f6de73a2af8ca0c6bd2dc88c7f7ae0a0ce334bcae39c14047aab540`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:025e99b21a301a69c768cc2c72e67c371165b6314d59d0a5a95958216fd24eac in /nats-server 
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 04 Dec 2021 07:52:29 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:52:29 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 04 Dec 2021 07:52:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:75a8e365d6e58c8d8f7fe944a206f76f3e800542aca1b53e849c4bffc78fd22d`  
		Last Modified: Sat, 04 Dec 2021 07:55:01 GMT  
		Size: 4.2 MB (4237211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2920e0912e6a42ee2fd0b7b8b31c6cca01c6c99f16c760f904492422ff7cae`  
		Last Modified: Sat, 04 Dec 2021 07:54:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8ecffb2097f683980b94450d536a99c79b3fe7654f8bc91fd1c45ad0825e6aae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb404fba49386fc48ceb05ee04604d317ff225da69f159d0bd4cc63a930c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 16:57:31 GMT
COPY file:b5f62686ba6debf89a42d2be7c4442db5f8735dba6b8932e6f01f315a2e63e27 in /nats-server 
# Fri, 03 Dec 2021 16:57:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 16:57:32 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 16:57:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44ff62bde832e2b2bca85708fd2fc86d7d6d1f4ca7c58b5d0e18e3d07c9c5bac`  
		Last Modified: Fri, 03 Dec 2021 16:58:50 GMT  
		Size: 4.2 MB (4189288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcbc70566b6f8312605c0214812444ccad7a55594fa2e7f0792c21af818ef0`  
		Last Modified: Fri, 03 Dec 2021 16:58:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d5b187939141b66d0480e6dd5e3b878abd5372efc6f4f26a92b7c0029ea48056
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107547635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96befd294a3f45573c0d15724d0700dbff10edac97ede11a013bffad728168e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 04:34:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4f56553f84cd7b4574c0b4d1ee6585d70eda0c9f3a5f1b276ec5e7cdc713bd74`  
		Last Modified: Sat, 18 Dec 2021 08:06:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc8a1565220717c5c64229e0ba21ccd6622cde8482e3c124233dfa9003b60cd`  
		Last Modified: Wed, 29 Dec 2021 13:24:21 GMT  
		Size: 4.6 MB (4637251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883fbea1eb1283a4bbf26392acf172e4ef79b4ab0b4778d46f4b1a84493b1dca`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939ae0d8b1fb893c6f64343b668aa03be89852764eb042ee8803cda7f6a8cd78`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca947ae0ca6d9fe8fb291c8d5bd0fb944a8eb0d77d86744b85f13d91431ac9b3`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0aaab409f72994f4e3999f144ef170ad74faff15cb7507c2acab06bf80cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:8e2e34eb798631cd76f341277f529f78618a2366d81b59586d3b81f6cb839b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:687f39ecdab1eeda8a4eaa7b7210586d96698faa5e5e7e47aaf5ef8084d504e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7689543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5dc2cfb512e016e62911eca35c050a2eb5ca4b783d5f2d413ba64c68c420bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 03 Dec 2021 21:22:18 GMT
ENV NATS_SERVER=2.6.6
# Fri, 03 Dec 2021 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 03 Dec 2021 21:22:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 03 Dec 2021 21:22:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 03 Dec 2021 21:22:22 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:22:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 21:22:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeb19d8d614f4a1df58ed04d3c72469fa9f7286c9d5482ee274405723b5e645`  
		Last Modified: Fri, 03 Dec 2021 21:23:37 GMT  
		Size: 4.9 MB (4865593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51c3679390c1ab0c5f5e6786505ad9278d45683059fc7fac0298dcbb6dede86`  
		Last Modified: Fri, 03 Dec 2021 21:23:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14f15cf01b25470e7340acc8ca0860eb4a00a7e1b5d5180bd7c23db1dd273af`  
		Last Modified: Fri, 03 Dec 2021 21:23:36 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d42d25248435c99492dd0fbcd97688486c692c680069bc9a1eb8a7b1c85eebff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7161537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae84a8c7e689bc4d7fd2915ef9aaf1fb624c094cb183af5863d4b20984f29cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Thu, 02 Dec 2021 22:49:35 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 22:49:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Dec 2021 22:49:41 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 22:49:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c7b89c441a056fc0e4d867cd4fd28308f188bd0f6b306e5feee96fee47cbdf`  
		Last Modified: Thu, 02 Dec 2021 22:51:52 GMT  
		Size: 4.5 MB (4525169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67a5f3b97f233f2d6d30a90acd85b9e856cb9b98c298b71e2b5cbae3e0268cf`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706486ffe19b237b40203ebf10cb1110d7566cba5a3c10bf738be70173a1aa69`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:dbc345345cfc225bd88b35e80f85f412483db712134bde3a0e4d959cb543350f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6958146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaa47180fd5390c3f39b81e39db30c26897fc1b070c064d4677ebdd14c1f801`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 04 Dec 2021 07:51:50 GMT
ENV NATS_SERVER=2.6.6
# Sat, 04 Dec 2021 07:51:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 04 Dec 2021 07:51:55 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 04 Dec 2021 07:51:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 04 Dec 2021 07:51:56 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:51:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Dec 2021 07:51:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157eac698795baeacb3153cf2bbbc17f348e477e8062fa45b6728e97dd02e157`  
		Last Modified: Sat, 04 Dec 2021 07:54:19 GMT  
		Size: 4.5 MB (4518555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5241fcba964a14f9c4681ebcc94815a476df86f68c628494f5759a3bee8514`  
		Last Modified: Sat, 04 Dec 2021 07:54:16 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d02df08ee2f75a857120c105153a83b2b951337a87e902260e70e1de20dfd0`  
		Last Modified: Sat, 04 Dec 2021 07:54:16 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f1e7262504ed73a185ee16f6a6da14c19c3a76120f2b22c51a051a0988ac3bdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e483df89c189235b79aa4a9d2417378172236dba6fa85f6d5a0bb35756835f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 03 Dec 2021 16:57:10 GMT
ENV NATS_SERVER=2.6.6
# Fri, 03 Dec 2021 16:57:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 03 Dec 2021 16:57:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 03 Dec 2021 16:57:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 03 Dec 2021 16:57:16 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 16:57:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdee3b2a5421d3ceb50b8101857ce4c0815c4532476e1f292867c63034c08f61`  
		Last Modified: Fri, 03 Dec 2021 16:58:22 GMT  
		Size: 4.5 MB (4474835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a771880289bb86cd368ca8b39620b0cfe69694646e061ff6975f959ccfcd29`  
		Last Modified: Fri, 03 Dec 2021 16:58:21 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438c5abdffd6599ac83fe661d26a9491552d63f48aeb9147609299ee11b78c78`  
		Last Modified: Fri, 03 Dec 2021 16:58:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.14`

```console
$ docker pull nats@sha256:8e2e34eb798631cd76f341277f529f78618a2366d81b59586d3b81f6cb839b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:687f39ecdab1eeda8a4eaa7b7210586d96698faa5e5e7e47aaf5ef8084d504e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7689543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5dc2cfb512e016e62911eca35c050a2eb5ca4b783d5f2d413ba64c68c420bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 03 Dec 2021 21:22:18 GMT
ENV NATS_SERVER=2.6.6
# Fri, 03 Dec 2021 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 03 Dec 2021 21:22:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 03 Dec 2021 21:22:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 03 Dec 2021 21:22:22 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:22:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 21:22:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeb19d8d614f4a1df58ed04d3c72469fa9f7286c9d5482ee274405723b5e645`  
		Last Modified: Fri, 03 Dec 2021 21:23:37 GMT  
		Size: 4.9 MB (4865593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51c3679390c1ab0c5f5e6786505ad9278d45683059fc7fac0298dcbb6dede86`  
		Last Modified: Fri, 03 Dec 2021 21:23:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14f15cf01b25470e7340acc8ca0860eb4a00a7e1b5d5180bd7c23db1dd273af`  
		Last Modified: Fri, 03 Dec 2021 21:23:36 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:d42d25248435c99492dd0fbcd97688486c692c680069bc9a1eb8a7b1c85eebff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7161537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae84a8c7e689bc4d7fd2915ef9aaf1fb624c094cb183af5863d4b20984f29cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Thu, 02 Dec 2021 22:49:35 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 22:49:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Dec 2021 22:49:41 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 22:49:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c7b89c441a056fc0e4d867cd4fd28308f188bd0f6b306e5feee96fee47cbdf`  
		Last Modified: Thu, 02 Dec 2021 22:51:52 GMT  
		Size: 4.5 MB (4525169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67a5f3b97f233f2d6d30a90acd85b9e856cb9b98c298b71e2b5cbae3e0268cf`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706486ffe19b237b40203ebf10cb1110d7566cba5a3c10bf738be70173a1aa69`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:dbc345345cfc225bd88b35e80f85f412483db712134bde3a0e4d959cb543350f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6958146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaa47180fd5390c3f39b81e39db30c26897fc1b070c064d4677ebdd14c1f801`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 04 Dec 2021 07:51:50 GMT
ENV NATS_SERVER=2.6.6
# Sat, 04 Dec 2021 07:51:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 04 Dec 2021 07:51:55 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 04 Dec 2021 07:51:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 04 Dec 2021 07:51:56 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:51:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Dec 2021 07:51:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157eac698795baeacb3153cf2bbbc17f348e477e8062fa45b6728e97dd02e157`  
		Last Modified: Sat, 04 Dec 2021 07:54:19 GMT  
		Size: 4.5 MB (4518555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5241fcba964a14f9c4681ebcc94815a476df86f68c628494f5759a3bee8514`  
		Last Modified: Sat, 04 Dec 2021 07:54:16 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d02df08ee2f75a857120c105153a83b2b951337a87e902260e70e1de20dfd0`  
		Last Modified: Sat, 04 Dec 2021 07:54:16 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f1e7262504ed73a185ee16f6a6da14c19c3a76120f2b22c51a051a0988ac3bdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e483df89c189235b79aa4a9d2417378172236dba6fa85f6d5a0bb35756835f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 03 Dec 2021 16:57:10 GMT
ENV NATS_SERVER=2.6.6
# Fri, 03 Dec 2021 16:57:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 03 Dec 2021 16:57:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 03 Dec 2021 16:57:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 03 Dec 2021 16:57:16 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 16:57:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdee3b2a5421d3ceb50b8101857ce4c0815c4532476e1f292867c63034c08f61`  
		Last Modified: Fri, 03 Dec 2021 16:58:22 GMT  
		Size: 4.5 MB (4474835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a771880289bb86cd368ca8b39620b0cfe69694646e061ff6975f959ccfcd29`  
		Last Modified: Fri, 03 Dec 2021 16:58:21 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438c5abdffd6599ac83fe661d26a9491552d63f48aeb9147609299ee11b78c78`  
		Last Modified: Fri, 03 Dec 2021 16:58:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:5d130fed2ad109f922a3a52e45c0b87c0d5a674ad432024cb3d45f898cf425b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:dad4f69520337c2a80d2a9123963c971836f07f530cf4b7c56dde98a622e0a6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba73da93bdda8525a9f473851ee3de9a2d23c21e1d0a51d7da118bc122df420`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 21:23:03 GMT
COPY file:4070919cac43aa01e3ef5dd95589f24a9d649dcc7b4d6364927c764b1f90392e in /nats-server 
# Fri, 03 Dec 2021 21:23:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 21:23:04 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:23:04 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 21:23:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:730cae3de796bb1fbb06f0f847317c2b738bf9af9d1233daafcf2f708eade5ec`  
		Last Modified: Fri, 03 Dec 2021 21:24:01 GMT  
		Size: 4.6 MB (4577696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39027e71725d02ee81938943fd0f3e980f01abbe21c5e8f8ea8219687aaae862`  
		Last Modified: Fri, 03 Dec 2021 21:24:00 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:78ee1d57413d89c46e808dbb121ad895537b74af783c6e6189366afa07638b66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3276dd6f6de73a2af8ca0c6bd2dc88c7f7ae0a0ce334bcae39c14047aab540`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:025e99b21a301a69c768cc2c72e67c371165b6314d59d0a5a95958216fd24eac in /nats-server 
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 04 Dec 2021 07:52:29 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:52:29 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 04 Dec 2021 07:52:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:75a8e365d6e58c8d8f7fe944a206f76f3e800542aca1b53e849c4bffc78fd22d`  
		Last Modified: Sat, 04 Dec 2021 07:55:01 GMT  
		Size: 4.2 MB (4237211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2920e0912e6a42ee2fd0b7b8b31c6cca01c6c99f16c760f904492422ff7cae`  
		Last Modified: Sat, 04 Dec 2021 07:54:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8ecffb2097f683980b94450d536a99c79b3fe7654f8bc91fd1c45ad0825e6aae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb404fba49386fc48ceb05ee04604d317ff225da69f159d0bd4cc63a930c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 16:57:31 GMT
COPY file:b5f62686ba6debf89a42d2be7c4442db5f8735dba6b8932e6f01f315a2e63e27 in /nats-server 
# Fri, 03 Dec 2021 16:57:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 16:57:32 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 16:57:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44ff62bde832e2b2bca85708fd2fc86d7d6d1f4ca7c58b5d0e18e3d07c9c5bac`  
		Last Modified: Fri, 03 Dec 2021 16:58:50 GMT  
		Size: 4.2 MB (4189288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcbc70566b6f8312605c0214812444ccad7a55594fa2e7f0792c21af818ef0`  
		Last Modified: Fri, 03 Dec 2021 16:58:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:b35a028eb89d68dd32700c5ea035a6ab326a311d002970977341a82f6a785c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d5b187939141b66d0480e6dd5e3b878abd5372efc6f4f26a92b7c0029ea48056
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107547635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96befd294a3f45573c0d15724d0700dbff10edac97ede11a013bffad728168e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 04:34:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4f56553f84cd7b4574c0b4d1ee6585d70eda0c9f3a5f1b276ec5e7cdc713bd74`  
		Last Modified: Sat, 18 Dec 2021 08:06:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc8a1565220717c5c64229e0ba21ccd6622cde8482e3c124233dfa9003b60cd`  
		Last Modified: Wed, 29 Dec 2021 13:24:21 GMT  
		Size: 4.6 MB (4637251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883fbea1eb1283a4bbf26392acf172e4ef79b4ab0b4778d46f4b1a84493b1dca`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939ae0d8b1fb893c6f64343b668aa03be89852764eb042ee8803cda7f6a8cd78`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca947ae0ca6d9fe8fb291c8d5bd0fb944a8eb0d77d86744b85f13d91431ac9b3`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0aaab409f72994f4e3999f144ef170ad74faff15cb7507c2acab06bf80cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:b35a028eb89d68dd32700c5ea035a6ab326a311d002970977341a82f6a785c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d5b187939141b66d0480e6dd5e3b878abd5372efc6f4f26a92b7c0029ea48056
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107547635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96befd294a3f45573c0d15724d0700dbff10edac97ede11a013bffad728168e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 04:34:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4f56553f84cd7b4574c0b4d1ee6585d70eda0c9f3a5f1b276ec5e7cdc713bd74`  
		Last Modified: Sat, 18 Dec 2021 08:06:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc8a1565220717c5c64229e0ba21ccd6622cde8482e3c124233dfa9003b60cd`  
		Last Modified: Wed, 29 Dec 2021 13:24:21 GMT  
		Size: 4.6 MB (4637251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883fbea1eb1283a4bbf26392acf172e4ef79b4ab0b4778d46f4b1a84493b1dca`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939ae0d8b1fb893c6f64343b668aa03be89852764eb042ee8803cda7f6a8cd78`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca947ae0ca6d9fe8fb291c8d5bd0fb944a8eb0d77d86744b85f13d91431ac9b3`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0aaab409f72994f4e3999f144ef170ad74faff15cb7507c2acab06bf80cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:5d130fed2ad109f922a3a52e45c0b87c0d5a674ad432024cb3d45f898cf425b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:dad4f69520337c2a80d2a9123963c971836f07f530cf4b7c56dde98a622e0a6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba73da93bdda8525a9f473851ee3de9a2d23c21e1d0a51d7da118bc122df420`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 21:23:03 GMT
COPY file:4070919cac43aa01e3ef5dd95589f24a9d649dcc7b4d6364927c764b1f90392e in /nats-server 
# Fri, 03 Dec 2021 21:23:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 21:23:04 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:23:04 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 21:23:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:730cae3de796bb1fbb06f0f847317c2b738bf9af9d1233daafcf2f708eade5ec`  
		Last Modified: Fri, 03 Dec 2021 21:24:01 GMT  
		Size: 4.6 MB (4577696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39027e71725d02ee81938943fd0f3e980f01abbe21c5e8f8ea8219687aaae862`  
		Last Modified: Fri, 03 Dec 2021 21:24:00 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:78ee1d57413d89c46e808dbb121ad895537b74af783c6e6189366afa07638b66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3276dd6f6de73a2af8ca0c6bd2dc88c7f7ae0a0ce334bcae39c14047aab540`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:025e99b21a301a69c768cc2c72e67c371165b6314d59d0a5a95958216fd24eac in /nats-server 
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 04 Dec 2021 07:52:29 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:52:29 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 04 Dec 2021 07:52:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:75a8e365d6e58c8d8f7fe944a206f76f3e800542aca1b53e849c4bffc78fd22d`  
		Last Modified: Sat, 04 Dec 2021 07:55:01 GMT  
		Size: 4.2 MB (4237211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2920e0912e6a42ee2fd0b7b8b31c6cca01c6c99f16c760f904492422ff7cae`  
		Last Modified: Sat, 04 Dec 2021 07:54:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8ecffb2097f683980b94450d536a99c79b3fe7654f8bc91fd1c45ad0825e6aae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb404fba49386fc48ceb05ee04604d317ff225da69f159d0bd4cc63a930c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 16:57:31 GMT
COPY file:b5f62686ba6debf89a42d2be7c4442db5f8735dba6b8932e6f01f315a2e63e27 in /nats-server 
# Fri, 03 Dec 2021 16:57:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 16:57:32 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 16:57:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44ff62bde832e2b2bca85708fd2fc86d7d6d1f4ca7c58b5d0e18e3d07c9c5bac`  
		Last Modified: Fri, 03 Dec 2021 16:58:50 GMT  
		Size: 4.2 MB (4189288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcbc70566b6f8312605c0214812444ccad7a55594fa2e7f0792c21af818ef0`  
		Last Modified: Fri, 03 Dec 2021 16:58:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:13bb711f4847d1af1afafb5c962f574ecfeb01b1ab37fb2f3f328d2da02f40df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2366; amd64
	-	windows version 10.0.14393.4825; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d232cd8a1f4e7e8e07cab41c7df5e76a7621d4dab30d1d3010ce1a80d71d0031
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2713981684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72d62160474997048b207a63be5355a15b11e62f414d223416d6920c00e08d2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Sat, 18 Dec 2021 01:40:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 18 Dec 2021 04:32:10 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:32:10 GMT
ENV NATS_SERVER=2.6.6
# Sat, 18 Dec 2021 04:32:11 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Sat, 18 Dec 2021 04:32:12 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Sat, 18 Dec 2021 04:33:08 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Dec 2021 04:34:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Sat, 18 Dec 2021 04:34:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:27 GMT
EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d22d2238b031d3f13bcd6c144e80f8f8402332b8ee8e53cc54b7912c3ac808cb`  
		Last Modified: Sat, 18 Dec 2021 03:59:34 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c5f7f5394b88876960b5ac27980fb2e22584cf50ecde4d9537e88ddbf849c3`  
		Last Modified: Sat, 18 Dec 2021 08:06:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db095798002004c7354bde24c88ee14ba02e430ccfe960c761470e023d0549e`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0362f786811b6ac9b6dbbc36403b1ea4e26ffe73ca7a49ccbb06f1fb9403f315`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ef6c82efd2b3c96cdce7abcace76e1231881bfe847245fbae17e80674ed7bb`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5680cfa178ed5d45ba63a530d80c2b6e96002029544bfa9b2923e63a16f729cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 365.8 KB (365820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9fa2a9d1117be676892e9ced2a72a88583d6b54d4c61de0eb6f92b937b2d9d`  
		Last Modified: Wed, 29 Dec 2021 13:24:05 GMT  
		Size: 5.0 MB (4998116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c2686658f0d823b26ef428ef67cf347e470511ca1675365bbb286131925754`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eb06c9a0a37ab81dde05f4196f65ba87c5cab394a6333a3258f8d737d87571`  
		Last Modified: Wed, 29 Dec 2021 13:23:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db8a42caf1046ab762e7e442960441653dbf5854db77c937eb332552d8fc2ac`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b0fad0cdb1e2a3ebb2f7f59a2d5fc2f11486fe57937c012b4e76f26ac7524d`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.4825; amd64

```console
$ docker pull nats@sha256:70298f4fa8023d6a4d2a21c616ac79a3cb9cc8fff4e00f83ce618b7d237fb30e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6280045896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed150f48d56334a037ca5957d0291e7226e8088f5051e674f85f38bdf616f32`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 08 Dec 2021 08:38:00 GMT
RUN Install update ltsc2016-amd64
# Sat, 18 Dec 2021 01:55:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 18 Dec 2021 04:34:51 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:52 GMT
ENV NATS_SERVER=2.6.6
# Sat, 18 Dec 2021 04:34:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Sat, 18 Dec 2021 04:34:53 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Sat, 18 Dec 2021 04:35:50 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Dec 2021 04:37:24 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Sat, 18 Dec 2021 04:37:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:37:26 GMT
EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:37:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:37:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d026d646213ccf73d9f0584941d108253d62e73df2a74e070776884b7b0242b`  
		Size: 2.2 GB (2204728802 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6bffd19db3f71ba2031bea25a529c67034869e7e1bbf9e2431d5ee747bd6d6d`  
		Last Modified: Sat, 18 Dec 2021 04:00:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05006360e7d5d5f0fc5160410fd98cfab768e620dca3f3fbc5b44e611e3039b4`  
		Last Modified: Sat, 18 Dec 2021 08:06:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3409aa65b2e0951ea84912add432d4791b9410b3e7a3d6d5df8244185c447e97`  
		Last Modified: Wed, 29 Dec 2021 13:24:39 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b9931dce79731d8fc8f9aae5bb18374967450b16fbcdfd0a2da48dd3efe853`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a5ed1a9ed62c133c6a9b7716fba9971e3f97b64477de601e28cc3ca5b05c8b`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c69ccdace4415c2bdec7795fab2a239ce07eb9906db4b613e2f024a20433a5`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 331.3 KB (331314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b3ee24e2d2850f329b382be9ade011322d08041d68c519d1a03fe3673639af`  
		Last Modified: Wed, 29 Dec 2021 13:24:41 GMT  
		Size: 5.0 MB (4986765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a195460559eca4221d68693a9db0cff883762ae3c2db047097b924a1b368b2`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed2147e829d4d68e6c2022d8fcdaf109525ad0e2b99f88eb2fccf2a746d507c`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfe2741387f6d51946ffb233018a1523759ecf1633a6c8a647410ec3095b16c`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508de22e92ac689a8f2b98d8314afdae274bf00f2d37ab78fbd17452c67a2e26`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:1ba92dc8d94836ff1669b1c5a13754529e799eb1f4455e8598f74e2a5a0758df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d232cd8a1f4e7e8e07cab41c7df5e76a7621d4dab30d1d3010ce1a80d71d0031
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2713981684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72d62160474997048b207a63be5355a15b11e62f414d223416d6920c00e08d2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Sat, 18 Dec 2021 01:40:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 18 Dec 2021 04:32:10 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:32:10 GMT
ENV NATS_SERVER=2.6.6
# Sat, 18 Dec 2021 04:32:11 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Sat, 18 Dec 2021 04:32:12 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Sat, 18 Dec 2021 04:33:08 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Dec 2021 04:34:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Sat, 18 Dec 2021 04:34:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:27 GMT
EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d22d2238b031d3f13bcd6c144e80f8f8402332b8ee8e53cc54b7912c3ac808cb`  
		Last Modified: Sat, 18 Dec 2021 03:59:34 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c5f7f5394b88876960b5ac27980fb2e22584cf50ecde4d9537e88ddbf849c3`  
		Last Modified: Sat, 18 Dec 2021 08:06:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db095798002004c7354bde24c88ee14ba02e430ccfe960c761470e023d0549e`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0362f786811b6ac9b6dbbc36403b1ea4e26ffe73ca7a49ccbb06f1fb9403f315`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ef6c82efd2b3c96cdce7abcace76e1231881bfe847245fbae17e80674ed7bb`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5680cfa178ed5d45ba63a530d80c2b6e96002029544bfa9b2923e63a16f729cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 365.8 KB (365820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9fa2a9d1117be676892e9ced2a72a88583d6b54d4c61de0eb6f92b937b2d9d`  
		Last Modified: Wed, 29 Dec 2021 13:24:05 GMT  
		Size: 5.0 MB (4998116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c2686658f0d823b26ef428ef67cf347e470511ca1675365bbb286131925754`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eb06c9a0a37ab81dde05f4196f65ba87c5cab394a6333a3258f8d737d87571`  
		Last Modified: Wed, 29 Dec 2021 13:23:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db8a42caf1046ab762e7e442960441653dbf5854db77c937eb332552d8fc2ac`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b0fad0cdb1e2a3ebb2f7f59a2d5fc2f11486fe57937c012b4e76f26ac7524d`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:f684eb2487b5e3aa125e4d0bff1a7b94bde1929252423f1b70fe773365dc1704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4825; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4825; amd64

```console
$ docker pull nats@sha256:70298f4fa8023d6a4d2a21c616ac79a3cb9cc8fff4e00f83ce618b7d237fb30e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6280045896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed150f48d56334a037ca5957d0291e7226e8088f5051e674f85f38bdf616f32`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 08 Dec 2021 08:38:00 GMT
RUN Install update ltsc2016-amd64
# Sat, 18 Dec 2021 01:55:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 18 Dec 2021 04:34:51 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:52 GMT
ENV NATS_SERVER=2.6.6
# Sat, 18 Dec 2021 04:34:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Sat, 18 Dec 2021 04:34:53 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Sat, 18 Dec 2021 04:35:50 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Dec 2021 04:37:24 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Sat, 18 Dec 2021 04:37:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:37:26 GMT
EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:37:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:37:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d026d646213ccf73d9f0584941d108253d62e73df2a74e070776884b7b0242b`  
		Size: 2.2 GB (2204728802 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6bffd19db3f71ba2031bea25a529c67034869e7e1bbf9e2431d5ee747bd6d6d`  
		Last Modified: Sat, 18 Dec 2021 04:00:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05006360e7d5d5f0fc5160410fd98cfab768e620dca3f3fbc5b44e611e3039b4`  
		Last Modified: Sat, 18 Dec 2021 08:06:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3409aa65b2e0951ea84912add432d4791b9410b3e7a3d6d5df8244185c447e97`  
		Last Modified: Wed, 29 Dec 2021 13:24:39 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b9931dce79731d8fc8f9aae5bb18374967450b16fbcdfd0a2da48dd3efe853`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a5ed1a9ed62c133c6a9b7716fba9971e3f97b64477de601e28cc3ca5b05c8b`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c69ccdace4415c2bdec7795fab2a239ce07eb9906db4b613e2f024a20433a5`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 331.3 KB (331314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b3ee24e2d2850f329b382be9ade011322d08041d68c519d1a03fe3673639af`  
		Last Modified: Wed, 29 Dec 2021 13:24:41 GMT  
		Size: 5.0 MB (4986765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a195460559eca4221d68693a9db0cff883762ae3c2db047097b924a1b368b2`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed2147e829d4d68e6c2022d8fcdaf109525ad0e2b99f88eb2fccf2a746d507c`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfe2741387f6d51946ffb233018a1523759ecf1633a6c8a647410ec3095b16c`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508de22e92ac689a8f2b98d8314afdae274bf00f2d37ab78fbd17452c67a2e26`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6`

```console
$ docker pull nats@sha256:4d4b166c324b4e9f0853e36d62cf831c5e4bd089fc6c5932ad9a98a8f73a143e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2366; amd64

### `nats:2.6` - linux; amd64

```console
$ docker pull nats@sha256:dad4f69520337c2a80d2a9123963c971836f07f530cf4b7c56dde98a622e0a6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba73da93bdda8525a9f473851ee3de9a2d23c21e1d0a51d7da118bc122df420`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 21:23:03 GMT
COPY file:4070919cac43aa01e3ef5dd95589f24a9d649dcc7b4d6364927c764b1f90392e in /nats-server 
# Fri, 03 Dec 2021 21:23:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 21:23:04 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:23:04 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 21:23:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:730cae3de796bb1fbb06f0f847317c2b738bf9af9d1233daafcf2f708eade5ec`  
		Last Modified: Fri, 03 Dec 2021 21:24:01 GMT  
		Size: 4.6 MB (4577696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39027e71725d02ee81938943fd0f3e980f01abbe21c5e8f8ea8219687aaae862`  
		Last Modified: Fri, 03 Dec 2021 21:24:00 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6` - linux; arm variant v7

```console
$ docker pull nats@sha256:78ee1d57413d89c46e808dbb121ad895537b74af783c6e6189366afa07638b66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3276dd6f6de73a2af8ca0c6bd2dc88c7f7ae0a0ce334bcae39c14047aab540`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:025e99b21a301a69c768cc2c72e67c371165b6314d59d0a5a95958216fd24eac in /nats-server 
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 04 Dec 2021 07:52:29 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:52:29 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 04 Dec 2021 07:52:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:75a8e365d6e58c8d8f7fe944a206f76f3e800542aca1b53e849c4bffc78fd22d`  
		Last Modified: Sat, 04 Dec 2021 07:55:01 GMT  
		Size: 4.2 MB (4237211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2920e0912e6a42ee2fd0b7b8b31c6cca01c6c99f16c760f904492422ff7cae`  
		Last Modified: Sat, 04 Dec 2021 07:54:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8ecffb2097f683980b94450d536a99c79b3fe7654f8bc91fd1c45ad0825e6aae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb404fba49386fc48ceb05ee04604d317ff225da69f159d0bd4cc63a930c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 16:57:31 GMT
COPY file:b5f62686ba6debf89a42d2be7c4442db5f8735dba6b8932e6f01f315a2e63e27 in /nats-server 
# Fri, 03 Dec 2021 16:57:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 16:57:32 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 16:57:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44ff62bde832e2b2bca85708fd2fc86d7d6d1f4ca7c58b5d0e18e3d07c9c5bac`  
		Last Modified: Fri, 03 Dec 2021 16:58:50 GMT  
		Size: 4.2 MB (4189288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcbc70566b6f8312605c0214812444ccad7a55594fa2e7f0792c21af818ef0`  
		Last Modified: Fri, 03 Dec 2021 16:58:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d5b187939141b66d0480e6dd5e3b878abd5372efc6f4f26a92b7c0029ea48056
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107547635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96befd294a3f45573c0d15724d0700dbff10edac97ede11a013bffad728168e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 04:34:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4f56553f84cd7b4574c0b4d1ee6585d70eda0c9f3a5f1b276ec5e7cdc713bd74`  
		Last Modified: Sat, 18 Dec 2021 08:06:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc8a1565220717c5c64229e0ba21ccd6622cde8482e3c124233dfa9003b60cd`  
		Last Modified: Wed, 29 Dec 2021 13:24:21 GMT  
		Size: 4.6 MB (4637251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883fbea1eb1283a4bbf26392acf172e4ef79b4ab0b4778d46f4b1a84493b1dca`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939ae0d8b1fb893c6f64343b668aa03be89852764eb042ee8803cda7f6a8cd78`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca947ae0ca6d9fe8fb291c8d5bd0fb944a8eb0d77d86744b85f13d91431ac9b3`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0aaab409f72994f4e3999f144ef170ad74faff15cb7507c2acab06bf80cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-alpine`

```console
$ docker pull nats@sha256:8e2e34eb798631cd76f341277f529f78618a2366d81b59586d3b81f6cb839b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6-alpine` - linux; amd64

```console
$ docker pull nats@sha256:687f39ecdab1eeda8a4eaa7b7210586d96698faa5e5e7e47aaf5ef8084d504e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7689543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5dc2cfb512e016e62911eca35c050a2eb5ca4b783d5f2d413ba64c68c420bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 03 Dec 2021 21:22:18 GMT
ENV NATS_SERVER=2.6.6
# Fri, 03 Dec 2021 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 03 Dec 2021 21:22:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 03 Dec 2021 21:22:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 03 Dec 2021 21:22:22 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:22:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 21:22:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeb19d8d614f4a1df58ed04d3c72469fa9f7286c9d5482ee274405723b5e645`  
		Last Modified: Fri, 03 Dec 2021 21:23:37 GMT  
		Size: 4.9 MB (4865593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51c3679390c1ab0c5f5e6786505ad9278d45683059fc7fac0298dcbb6dede86`  
		Last Modified: Fri, 03 Dec 2021 21:23:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14f15cf01b25470e7340acc8ca0860eb4a00a7e1b5d5180bd7c23db1dd273af`  
		Last Modified: Fri, 03 Dec 2021 21:23:36 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d42d25248435c99492dd0fbcd97688486c692c680069bc9a1eb8a7b1c85eebff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7161537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae84a8c7e689bc4d7fd2915ef9aaf1fb624c094cb183af5863d4b20984f29cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Thu, 02 Dec 2021 22:49:35 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 22:49:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Dec 2021 22:49:41 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 22:49:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c7b89c441a056fc0e4d867cd4fd28308f188bd0f6b306e5feee96fee47cbdf`  
		Last Modified: Thu, 02 Dec 2021 22:51:52 GMT  
		Size: 4.5 MB (4525169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67a5f3b97f233f2d6d30a90acd85b9e856cb9b98c298b71e2b5cbae3e0268cf`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706486ffe19b237b40203ebf10cb1110d7566cba5a3c10bf738be70173a1aa69`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:dbc345345cfc225bd88b35e80f85f412483db712134bde3a0e4d959cb543350f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6958146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaa47180fd5390c3f39b81e39db30c26897fc1b070c064d4677ebdd14c1f801`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 04 Dec 2021 07:51:50 GMT
ENV NATS_SERVER=2.6.6
# Sat, 04 Dec 2021 07:51:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 04 Dec 2021 07:51:55 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 04 Dec 2021 07:51:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 04 Dec 2021 07:51:56 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:51:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Dec 2021 07:51:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157eac698795baeacb3153cf2bbbc17f348e477e8062fa45b6728e97dd02e157`  
		Last Modified: Sat, 04 Dec 2021 07:54:19 GMT  
		Size: 4.5 MB (4518555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5241fcba964a14f9c4681ebcc94815a476df86f68c628494f5759a3bee8514`  
		Last Modified: Sat, 04 Dec 2021 07:54:16 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d02df08ee2f75a857120c105153a83b2b951337a87e902260e70e1de20dfd0`  
		Last Modified: Sat, 04 Dec 2021 07:54:16 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f1e7262504ed73a185ee16f6a6da14c19c3a76120f2b22c51a051a0988ac3bdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e483df89c189235b79aa4a9d2417378172236dba6fa85f6d5a0bb35756835f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 03 Dec 2021 16:57:10 GMT
ENV NATS_SERVER=2.6.6
# Fri, 03 Dec 2021 16:57:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 03 Dec 2021 16:57:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 03 Dec 2021 16:57:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 03 Dec 2021 16:57:16 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 16:57:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdee3b2a5421d3ceb50b8101857ce4c0815c4532476e1f292867c63034c08f61`  
		Last Modified: Fri, 03 Dec 2021 16:58:22 GMT  
		Size: 4.5 MB (4474835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a771880289bb86cd368ca8b39620b0cfe69694646e061ff6975f959ccfcd29`  
		Last Modified: Fri, 03 Dec 2021 16:58:21 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438c5abdffd6599ac83fe661d26a9491552d63f48aeb9147609299ee11b78c78`  
		Last Modified: Fri, 03 Dec 2021 16:58:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-alpine3.14`

```console
$ docker pull nats@sha256:8e2e34eb798631cd76f341277f529f78618a2366d81b59586d3b81f6cb839b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6-alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:687f39ecdab1eeda8a4eaa7b7210586d96698faa5e5e7e47aaf5ef8084d504e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7689543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5dc2cfb512e016e62911eca35c050a2eb5ca4b783d5f2d413ba64c68c420bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 03 Dec 2021 21:22:18 GMT
ENV NATS_SERVER=2.6.6
# Fri, 03 Dec 2021 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 03 Dec 2021 21:22:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 03 Dec 2021 21:22:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 03 Dec 2021 21:22:22 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:22:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 21:22:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeb19d8d614f4a1df58ed04d3c72469fa9f7286c9d5482ee274405723b5e645`  
		Last Modified: Fri, 03 Dec 2021 21:23:37 GMT  
		Size: 4.9 MB (4865593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51c3679390c1ab0c5f5e6786505ad9278d45683059fc7fac0298dcbb6dede86`  
		Last Modified: Fri, 03 Dec 2021 21:23:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14f15cf01b25470e7340acc8ca0860eb4a00a7e1b5d5180bd7c23db1dd273af`  
		Last Modified: Fri, 03 Dec 2021 21:23:36 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine3.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:d42d25248435c99492dd0fbcd97688486c692c680069bc9a1eb8a7b1c85eebff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7161537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae84a8c7e689bc4d7fd2915ef9aaf1fb624c094cb183af5863d4b20984f29cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Thu, 02 Dec 2021 22:49:35 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 22:49:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Dec 2021 22:49:41 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 22:49:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c7b89c441a056fc0e4d867cd4fd28308f188bd0f6b306e5feee96fee47cbdf`  
		Last Modified: Thu, 02 Dec 2021 22:51:52 GMT  
		Size: 4.5 MB (4525169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67a5f3b97f233f2d6d30a90acd85b9e856cb9b98c298b71e2b5cbae3e0268cf`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706486ffe19b237b40203ebf10cb1110d7566cba5a3c10bf738be70173a1aa69`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine3.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:dbc345345cfc225bd88b35e80f85f412483db712134bde3a0e4d959cb543350f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6958146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaa47180fd5390c3f39b81e39db30c26897fc1b070c064d4677ebdd14c1f801`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 04 Dec 2021 07:51:50 GMT
ENV NATS_SERVER=2.6.6
# Sat, 04 Dec 2021 07:51:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 04 Dec 2021 07:51:55 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 04 Dec 2021 07:51:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 04 Dec 2021 07:51:56 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:51:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Dec 2021 07:51:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157eac698795baeacb3153cf2bbbc17f348e477e8062fa45b6728e97dd02e157`  
		Last Modified: Sat, 04 Dec 2021 07:54:19 GMT  
		Size: 4.5 MB (4518555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5241fcba964a14f9c4681ebcc94815a476df86f68c628494f5759a3bee8514`  
		Last Modified: Sat, 04 Dec 2021 07:54:16 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d02df08ee2f75a857120c105153a83b2b951337a87e902260e70e1de20dfd0`  
		Last Modified: Sat, 04 Dec 2021 07:54:16 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f1e7262504ed73a185ee16f6a6da14c19c3a76120f2b22c51a051a0988ac3bdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e483df89c189235b79aa4a9d2417378172236dba6fa85f6d5a0bb35756835f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 03 Dec 2021 16:57:10 GMT
ENV NATS_SERVER=2.6.6
# Fri, 03 Dec 2021 16:57:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 03 Dec 2021 16:57:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 03 Dec 2021 16:57:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 03 Dec 2021 16:57:16 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 16:57:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdee3b2a5421d3ceb50b8101857ce4c0815c4532476e1f292867c63034c08f61`  
		Last Modified: Fri, 03 Dec 2021 16:58:22 GMT  
		Size: 4.5 MB (4474835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a771880289bb86cd368ca8b39620b0cfe69694646e061ff6975f959ccfcd29`  
		Last Modified: Fri, 03 Dec 2021 16:58:21 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438c5abdffd6599ac83fe661d26a9491552d63f48aeb9147609299ee11b78c78`  
		Last Modified: Fri, 03 Dec 2021 16:58:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-linux`

```console
$ docker pull nats@sha256:5d130fed2ad109f922a3a52e45c0b87c0d5a674ad432024cb3d45f898cf425b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6-linux` - linux; amd64

```console
$ docker pull nats@sha256:dad4f69520337c2a80d2a9123963c971836f07f530cf4b7c56dde98a622e0a6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba73da93bdda8525a9f473851ee3de9a2d23c21e1d0a51d7da118bc122df420`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 21:23:03 GMT
COPY file:4070919cac43aa01e3ef5dd95589f24a9d649dcc7b4d6364927c764b1f90392e in /nats-server 
# Fri, 03 Dec 2021 21:23:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 21:23:04 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:23:04 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 21:23:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:730cae3de796bb1fbb06f0f847317c2b738bf9af9d1233daafcf2f708eade5ec`  
		Last Modified: Fri, 03 Dec 2021 21:24:01 GMT  
		Size: 4.6 MB (4577696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39027e71725d02ee81938943fd0f3e980f01abbe21c5e8f8ea8219687aaae862`  
		Last Modified: Fri, 03 Dec 2021 21:24:00 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:78ee1d57413d89c46e808dbb121ad895537b74af783c6e6189366afa07638b66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3276dd6f6de73a2af8ca0c6bd2dc88c7f7ae0a0ce334bcae39c14047aab540`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:025e99b21a301a69c768cc2c72e67c371165b6314d59d0a5a95958216fd24eac in /nats-server 
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 04 Dec 2021 07:52:29 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:52:29 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 04 Dec 2021 07:52:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:75a8e365d6e58c8d8f7fe944a206f76f3e800542aca1b53e849c4bffc78fd22d`  
		Last Modified: Sat, 04 Dec 2021 07:55:01 GMT  
		Size: 4.2 MB (4237211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2920e0912e6a42ee2fd0b7b8b31c6cca01c6c99f16c760f904492422ff7cae`  
		Last Modified: Sat, 04 Dec 2021 07:54:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8ecffb2097f683980b94450d536a99c79b3fe7654f8bc91fd1c45ad0825e6aae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb404fba49386fc48ceb05ee04604d317ff225da69f159d0bd4cc63a930c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 16:57:31 GMT
COPY file:b5f62686ba6debf89a42d2be7c4442db5f8735dba6b8932e6f01f315a2e63e27 in /nats-server 
# Fri, 03 Dec 2021 16:57:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 16:57:32 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 16:57:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44ff62bde832e2b2bca85708fd2fc86d7d6d1f4ca7c58b5d0e18e3d07c9c5bac`  
		Last Modified: Fri, 03 Dec 2021 16:58:50 GMT  
		Size: 4.2 MB (4189288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcbc70566b6f8312605c0214812444ccad7a55594fa2e7f0792c21af818ef0`  
		Last Modified: Fri, 03 Dec 2021 16:58:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-nanoserver`

```console
$ docker pull nats@sha256:b35a028eb89d68dd32700c5ea035a6ab326a311d002970977341a82f6a785c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `nats:2.6-nanoserver` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d5b187939141b66d0480e6dd5e3b878abd5372efc6f4f26a92b7c0029ea48056
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107547635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96befd294a3f45573c0d15724d0700dbff10edac97ede11a013bffad728168e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 04:34:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4f56553f84cd7b4574c0b4d1ee6585d70eda0c9f3a5f1b276ec5e7cdc713bd74`  
		Last Modified: Sat, 18 Dec 2021 08:06:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc8a1565220717c5c64229e0ba21ccd6622cde8482e3c124233dfa9003b60cd`  
		Last Modified: Wed, 29 Dec 2021 13:24:21 GMT  
		Size: 4.6 MB (4637251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883fbea1eb1283a4bbf26392acf172e4ef79b4ab0b4778d46f4b1a84493b1dca`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939ae0d8b1fb893c6f64343b668aa03be89852764eb042ee8803cda7f6a8cd78`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca947ae0ca6d9fe8fb291c8d5bd0fb944a8eb0d77d86744b85f13d91431ac9b3`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0aaab409f72994f4e3999f144ef170ad74faff15cb7507c2acab06bf80cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-nanoserver-1809`

```console
$ docker pull nats@sha256:b35a028eb89d68dd32700c5ea035a6ab326a311d002970977341a82f6a785c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `nats:2.6-nanoserver-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d5b187939141b66d0480e6dd5e3b878abd5372efc6f4f26a92b7c0029ea48056
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107547635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96befd294a3f45573c0d15724d0700dbff10edac97ede11a013bffad728168e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 04:34:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4f56553f84cd7b4574c0b4d1ee6585d70eda0c9f3a5f1b276ec5e7cdc713bd74`  
		Last Modified: Sat, 18 Dec 2021 08:06:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc8a1565220717c5c64229e0ba21ccd6622cde8482e3c124233dfa9003b60cd`  
		Last Modified: Wed, 29 Dec 2021 13:24:21 GMT  
		Size: 4.6 MB (4637251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883fbea1eb1283a4bbf26392acf172e4ef79b4ab0b4778d46f4b1a84493b1dca`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939ae0d8b1fb893c6f64343b668aa03be89852764eb042ee8803cda7f6a8cd78`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca947ae0ca6d9fe8fb291c8d5bd0fb944a8eb0d77d86744b85f13d91431ac9b3`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0aaab409f72994f4e3999f144ef170ad74faff15cb7507c2acab06bf80cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-scratch`

```console
$ docker pull nats@sha256:5d130fed2ad109f922a3a52e45c0b87c0d5a674ad432024cb3d45f898cf425b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6-scratch` - linux; amd64

```console
$ docker pull nats@sha256:dad4f69520337c2a80d2a9123963c971836f07f530cf4b7c56dde98a622e0a6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba73da93bdda8525a9f473851ee3de9a2d23c21e1d0a51d7da118bc122df420`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 21:23:03 GMT
COPY file:4070919cac43aa01e3ef5dd95589f24a9d649dcc7b4d6364927c764b1f90392e in /nats-server 
# Fri, 03 Dec 2021 21:23:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 21:23:04 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:23:04 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 21:23:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:730cae3de796bb1fbb06f0f847317c2b738bf9af9d1233daafcf2f708eade5ec`  
		Last Modified: Fri, 03 Dec 2021 21:24:01 GMT  
		Size: 4.6 MB (4577696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39027e71725d02ee81938943fd0f3e980f01abbe21c5e8f8ea8219687aaae862`  
		Last Modified: Fri, 03 Dec 2021 21:24:00 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:78ee1d57413d89c46e808dbb121ad895537b74af783c6e6189366afa07638b66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3276dd6f6de73a2af8ca0c6bd2dc88c7f7ae0a0ce334bcae39c14047aab540`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:025e99b21a301a69c768cc2c72e67c371165b6314d59d0a5a95958216fd24eac in /nats-server 
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 04 Dec 2021 07:52:29 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:52:29 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 04 Dec 2021 07:52:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:75a8e365d6e58c8d8f7fe944a206f76f3e800542aca1b53e849c4bffc78fd22d`  
		Last Modified: Sat, 04 Dec 2021 07:55:01 GMT  
		Size: 4.2 MB (4237211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2920e0912e6a42ee2fd0b7b8b31c6cca01c6c99f16c760f904492422ff7cae`  
		Last Modified: Sat, 04 Dec 2021 07:54:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8ecffb2097f683980b94450d536a99c79b3fe7654f8bc91fd1c45ad0825e6aae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb404fba49386fc48ceb05ee04604d317ff225da69f159d0bd4cc63a930c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 16:57:31 GMT
COPY file:b5f62686ba6debf89a42d2be7c4442db5f8735dba6b8932e6f01f315a2e63e27 in /nats-server 
# Fri, 03 Dec 2021 16:57:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 16:57:32 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 16:57:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44ff62bde832e2b2bca85708fd2fc86d7d6d1f4ca7c58b5d0e18e3d07c9c5bac`  
		Last Modified: Fri, 03 Dec 2021 16:58:50 GMT  
		Size: 4.2 MB (4189288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcbc70566b6f8312605c0214812444ccad7a55594fa2e7f0792c21af818ef0`  
		Last Modified: Fri, 03 Dec 2021 16:58:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-windowsservercore`

```console
$ docker pull nats@sha256:13bb711f4847d1af1afafb5c962f574ecfeb01b1ab37fb2f3f328d2da02f40df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2366; amd64
	-	windows version 10.0.14393.4825; amd64

### `nats:2.6-windowsservercore` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d232cd8a1f4e7e8e07cab41c7df5e76a7621d4dab30d1d3010ce1a80d71d0031
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2713981684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72d62160474997048b207a63be5355a15b11e62f414d223416d6920c00e08d2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Sat, 18 Dec 2021 01:40:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 18 Dec 2021 04:32:10 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:32:10 GMT
ENV NATS_SERVER=2.6.6
# Sat, 18 Dec 2021 04:32:11 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Sat, 18 Dec 2021 04:32:12 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Sat, 18 Dec 2021 04:33:08 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Dec 2021 04:34:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Sat, 18 Dec 2021 04:34:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:27 GMT
EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d22d2238b031d3f13bcd6c144e80f8f8402332b8ee8e53cc54b7912c3ac808cb`  
		Last Modified: Sat, 18 Dec 2021 03:59:34 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c5f7f5394b88876960b5ac27980fb2e22584cf50ecde4d9537e88ddbf849c3`  
		Last Modified: Sat, 18 Dec 2021 08:06:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db095798002004c7354bde24c88ee14ba02e430ccfe960c761470e023d0549e`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0362f786811b6ac9b6dbbc36403b1ea4e26ffe73ca7a49ccbb06f1fb9403f315`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ef6c82efd2b3c96cdce7abcace76e1231881bfe847245fbae17e80674ed7bb`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5680cfa178ed5d45ba63a530d80c2b6e96002029544bfa9b2923e63a16f729cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 365.8 KB (365820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9fa2a9d1117be676892e9ced2a72a88583d6b54d4c61de0eb6f92b937b2d9d`  
		Last Modified: Wed, 29 Dec 2021 13:24:05 GMT  
		Size: 5.0 MB (4998116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c2686658f0d823b26ef428ef67cf347e470511ca1675365bbb286131925754`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eb06c9a0a37ab81dde05f4196f65ba87c5cab394a6333a3258f8d737d87571`  
		Last Modified: Wed, 29 Dec 2021 13:23:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db8a42caf1046ab762e7e442960441653dbf5854db77c937eb332552d8fc2ac`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b0fad0cdb1e2a3ebb2f7f59a2d5fc2f11486fe57937c012b4e76f26ac7524d`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-windowsservercore` - windows version 10.0.14393.4825; amd64

```console
$ docker pull nats@sha256:70298f4fa8023d6a4d2a21c616ac79a3cb9cc8fff4e00f83ce618b7d237fb30e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6280045896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed150f48d56334a037ca5957d0291e7226e8088f5051e674f85f38bdf616f32`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 08 Dec 2021 08:38:00 GMT
RUN Install update ltsc2016-amd64
# Sat, 18 Dec 2021 01:55:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 18 Dec 2021 04:34:51 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:52 GMT
ENV NATS_SERVER=2.6.6
# Sat, 18 Dec 2021 04:34:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Sat, 18 Dec 2021 04:34:53 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Sat, 18 Dec 2021 04:35:50 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Dec 2021 04:37:24 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Sat, 18 Dec 2021 04:37:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:37:26 GMT
EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:37:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:37:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d026d646213ccf73d9f0584941d108253d62e73df2a74e070776884b7b0242b`  
		Size: 2.2 GB (2204728802 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6bffd19db3f71ba2031bea25a529c67034869e7e1bbf9e2431d5ee747bd6d6d`  
		Last Modified: Sat, 18 Dec 2021 04:00:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05006360e7d5d5f0fc5160410fd98cfab768e620dca3f3fbc5b44e611e3039b4`  
		Last Modified: Sat, 18 Dec 2021 08:06:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3409aa65b2e0951ea84912add432d4791b9410b3e7a3d6d5df8244185c447e97`  
		Last Modified: Wed, 29 Dec 2021 13:24:39 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b9931dce79731d8fc8f9aae5bb18374967450b16fbcdfd0a2da48dd3efe853`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a5ed1a9ed62c133c6a9b7716fba9971e3f97b64477de601e28cc3ca5b05c8b`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c69ccdace4415c2bdec7795fab2a239ce07eb9906db4b613e2f024a20433a5`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 331.3 KB (331314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b3ee24e2d2850f329b382be9ade011322d08041d68c519d1a03fe3673639af`  
		Last Modified: Wed, 29 Dec 2021 13:24:41 GMT  
		Size: 5.0 MB (4986765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a195460559eca4221d68693a9db0cff883762ae3c2db047097b924a1b368b2`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed2147e829d4d68e6c2022d8fcdaf109525ad0e2b99f88eb2fccf2a746d507c`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfe2741387f6d51946ffb233018a1523759ecf1633a6c8a647410ec3095b16c`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508de22e92ac689a8f2b98d8314afdae274bf00f2d37ab78fbd17452c67a2e26`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-windowsservercore-1809`

```console
$ docker pull nats@sha256:1ba92dc8d94836ff1669b1c5a13754529e799eb1f4455e8598f74e2a5a0758df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `nats:2.6-windowsservercore-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d232cd8a1f4e7e8e07cab41c7df5e76a7621d4dab30d1d3010ce1a80d71d0031
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2713981684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72d62160474997048b207a63be5355a15b11e62f414d223416d6920c00e08d2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Sat, 18 Dec 2021 01:40:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 18 Dec 2021 04:32:10 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:32:10 GMT
ENV NATS_SERVER=2.6.6
# Sat, 18 Dec 2021 04:32:11 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Sat, 18 Dec 2021 04:32:12 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Sat, 18 Dec 2021 04:33:08 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Dec 2021 04:34:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Sat, 18 Dec 2021 04:34:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:27 GMT
EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d22d2238b031d3f13bcd6c144e80f8f8402332b8ee8e53cc54b7912c3ac808cb`  
		Last Modified: Sat, 18 Dec 2021 03:59:34 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c5f7f5394b88876960b5ac27980fb2e22584cf50ecde4d9537e88ddbf849c3`  
		Last Modified: Sat, 18 Dec 2021 08:06:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db095798002004c7354bde24c88ee14ba02e430ccfe960c761470e023d0549e`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0362f786811b6ac9b6dbbc36403b1ea4e26ffe73ca7a49ccbb06f1fb9403f315`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ef6c82efd2b3c96cdce7abcace76e1231881bfe847245fbae17e80674ed7bb`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5680cfa178ed5d45ba63a530d80c2b6e96002029544bfa9b2923e63a16f729cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 365.8 KB (365820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9fa2a9d1117be676892e9ced2a72a88583d6b54d4c61de0eb6f92b937b2d9d`  
		Last Modified: Wed, 29 Dec 2021 13:24:05 GMT  
		Size: 5.0 MB (4998116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c2686658f0d823b26ef428ef67cf347e470511ca1675365bbb286131925754`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eb06c9a0a37ab81dde05f4196f65ba87c5cab394a6333a3258f8d737d87571`  
		Last Modified: Wed, 29 Dec 2021 13:23:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db8a42caf1046ab762e7e442960441653dbf5854db77c937eb332552d8fc2ac`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b0fad0cdb1e2a3ebb2f7f59a2d5fc2f11486fe57937c012b4e76f26ac7524d`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:f684eb2487b5e3aa125e4d0bff1a7b94bde1929252423f1b70fe773365dc1704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4825; amd64

### `nats:2.6-windowsservercore-ltsc2016` - windows version 10.0.14393.4825; amd64

```console
$ docker pull nats@sha256:70298f4fa8023d6a4d2a21c616ac79a3cb9cc8fff4e00f83ce618b7d237fb30e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6280045896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed150f48d56334a037ca5957d0291e7226e8088f5051e674f85f38bdf616f32`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 08 Dec 2021 08:38:00 GMT
RUN Install update ltsc2016-amd64
# Sat, 18 Dec 2021 01:55:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 18 Dec 2021 04:34:51 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:52 GMT
ENV NATS_SERVER=2.6.6
# Sat, 18 Dec 2021 04:34:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Sat, 18 Dec 2021 04:34:53 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Sat, 18 Dec 2021 04:35:50 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Dec 2021 04:37:24 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Sat, 18 Dec 2021 04:37:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:37:26 GMT
EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:37:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:37:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d026d646213ccf73d9f0584941d108253d62e73df2a74e070776884b7b0242b`  
		Size: 2.2 GB (2204728802 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6bffd19db3f71ba2031bea25a529c67034869e7e1bbf9e2431d5ee747bd6d6d`  
		Last Modified: Sat, 18 Dec 2021 04:00:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05006360e7d5d5f0fc5160410fd98cfab768e620dca3f3fbc5b44e611e3039b4`  
		Last Modified: Sat, 18 Dec 2021 08:06:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3409aa65b2e0951ea84912add432d4791b9410b3e7a3d6d5df8244185c447e97`  
		Last Modified: Wed, 29 Dec 2021 13:24:39 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b9931dce79731d8fc8f9aae5bb18374967450b16fbcdfd0a2da48dd3efe853`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a5ed1a9ed62c133c6a9b7716fba9971e3f97b64477de601e28cc3ca5b05c8b`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c69ccdace4415c2bdec7795fab2a239ce07eb9906db4b613e2f024a20433a5`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 331.3 KB (331314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b3ee24e2d2850f329b382be9ade011322d08041d68c519d1a03fe3673639af`  
		Last Modified: Wed, 29 Dec 2021 13:24:41 GMT  
		Size: 5.0 MB (4986765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a195460559eca4221d68693a9db0cff883762ae3c2db047097b924a1b368b2`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed2147e829d4d68e6c2022d8fcdaf109525ad0e2b99f88eb2fccf2a746d507c`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfe2741387f6d51946ffb233018a1523759ecf1633a6c8a647410ec3095b16c`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508de22e92ac689a8f2b98d8314afdae274bf00f2d37ab78fbd17452c67a2e26`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6`

```console
$ docker pull nats@sha256:4d4b166c324b4e9f0853e36d62cf831c5e4bd089fc6c5932ad9a98a8f73a143e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2366; amd64

### `nats:2.6.6` - linux; amd64

```console
$ docker pull nats@sha256:dad4f69520337c2a80d2a9123963c971836f07f530cf4b7c56dde98a622e0a6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba73da93bdda8525a9f473851ee3de9a2d23c21e1d0a51d7da118bc122df420`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 21:23:03 GMT
COPY file:4070919cac43aa01e3ef5dd95589f24a9d649dcc7b4d6364927c764b1f90392e in /nats-server 
# Fri, 03 Dec 2021 21:23:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 21:23:04 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:23:04 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 21:23:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:730cae3de796bb1fbb06f0f847317c2b738bf9af9d1233daafcf2f708eade5ec`  
		Last Modified: Fri, 03 Dec 2021 21:24:01 GMT  
		Size: 4.6 MB (4577696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39027e71725d02ee81938943fd0f3e980f01abbe21c5e8f8ea8219687aaae862`  
		Last Modified: Fri, 03 Dec 2021 21:24:00 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6` - linux; arm variant v7

```console
$ docker pull nats@sha256:78ee1d57413d89c46e808dbb121ad895537b74af783c6e6189366afa07638b66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3276dd6f6de73a2af8ca0c6bd2dc88c7f7ae0a0ce334bcae39c14047aab540`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:025e99b21a301a69c768cc2c72e67c371165b6314d59d0a5a95958216fd24eac in /nats-server 
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 04 Dec 2021 07:52:29 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:52:29 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 04 Dec 2021 07:52:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:75a8e365d6e58c8d8f7fe944a206f76f3e800542aca1b53e849c4bffc78fd22d`  
		Last Modified: Sat, 04 Dec 2021 07:55:01 GMT  
		Size: 4.2 MB (4237211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2920e0912e6a42ee2fd0b7b8b31c6cca01c6c99f16c760f904492422ff7cae`  
		Last Modified: Sat, 04 Dec 2021 07:54:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8ecffb2097f683980b94450d536a99c79b3fe7654f8bc91fd1c45ad0825e6aae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb404fba49386fc48ceb05ee04604d317ff225da69f159d0bd4cc63a930c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 16:57:31 GMT
COPY file:b5f62686ba6debf89a42d2be7c4442db5f8735dba6b8932e6f01f315a2e63e27 in /nats-server 
# Fri, 03 Dec 2021 16:57:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 16:57:32 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 16:57:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44ff62bde832e2b2bca85708fd2fc86d7d6d1f4ca7c58b5d0e18e3d07c9c5bac`  
		Last Modified: Fri, 03 Dec 2021 16:58:50 GMT  
		Size: 4.2 MB (4189288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcbc70566b6f8312605c0214812444ccad7a55594fa2e7f0792c21af818ef0`  
		Last Modified: Fri, 03 Dec 2021 16:58:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d5b187939141b66d0480e6dd5e3b878abd5372efc6f4f26a92b7c0029ea48056
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107547635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96befd294a3f45573c0d15724d0700dbff10edac97ede11a013bffad728168e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 04:34:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4f56553f84cd7b4574c0b4d1ee6585d70eda0c9f3a5f1b276ec5e7cdc713bd74`  
		Last Modified: Sat, 18 Dec 2021 08:06:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc8a1565220717c5c64229e0ba21ccd6622cde8482e3c124233dfa9003b60cd`  
		Last Modified: Wed, 29 Dec 2021 13:24:21 GMT  
		Size: 4.6 MB (4637251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883fbea1eb1283a4bbf26392acf172e4ef79b4ab0b4778d46f4b1a84493b1dca`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939ae0d8b1fb893c6f64343b668aa03be89852764eb042ee8803cda7f6a8cd78`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca947ae0ca6d9fe8fb291c8d5bd0fb944a8eb0d77d86744b85f13d91431ac9b3`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0aaab409f72994f4e3999f144ef170ad74faff15cb7507c2acab06bf80cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-alpine`

```console
$ docker pull nats@sha256:8e2e34eb798631cd76f341277f529f78618a2366d81b59586d3b81f6cb839b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6.6-alpine` - linux; amd64

```console
$ docker pull nats@sha256:687f39ecdab1eeda8a4eaa7b7210586d96698faa5e5e7e47aaf5ef8084d504e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7689543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5dc2cfb512e016e62911eca35c050a2eb5ca4b783d5f2d413ba64c68c420bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 03 Dec 2021 21:22:18 GMT
ENV NATS_SERVER=2.6.6
# Fri, 03 Dec 2021 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 03 Dec 2021 21:22:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 03 Dec 2021 21:22:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 03 Dec 2021 21:22:22 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:22:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 21:22:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeb19d8d614f4a1df58ed04d3c72469fa9f7286c9d5482ee274405723b5e645`  
		Last Modified: Fri, 03 Dec 2021 21:23:37 GMT  
		Size: 4.9 MB (4865593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51c3679390c1ab0c5f5e6786505ad9278d45683059fc7fac0298dcbb6dede86`  
		Last Modified: Fri, 03 Dec 2021 21:23:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14f15cf01b25470e7340acc8ca0860eb4a00a7e1b5d5180bd7c23db1dd273af`  
		Last Modified: Fri, 03 Dec 2021 21:23:36 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d42d25248435c99492dd0fbcd97688486c692c680069bc9a1eb8a7b1c85eebff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7161537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae84a8c7e689bc4d7fd2915ef9aaf1fb624c094cb183af5863d4b20984f29cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Thu, 02 Dec 2021 22:49:35 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 22:49:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Dec 2021 22:49:41 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 22:49:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c7b89c441a056fc0e4d867cd4fd28308f188bd0f6b306e5feee96fee47cbdf`  
		Last Modified: Thu, 02 Dec 2021 22:51:52 GMT  
		Size: 4.5 MB (4525169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67a5f3b97f233f2d6d30a90acd85b9e856cb9b98c298b71e2b5cbae3e0268cf`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706486ffe19b237b40203ebf10cb1110d7566cba5a3c10bf738be70173a1aa69`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:dbc345345cfc225bd88b35e80f85f412483db712134bde3a0e4d959cb543350f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6958146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaa47180fd5390c3f39b81e39db30c26897fc1b070c064d4677ebdd14c1f801`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 04 Dec 2021 07:51:50 GMT
ENV NATS_SERVER=2.6.6
# Sat, 04 Dec 2021 07:51:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 04 Dec 2021 07:51:55 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 04 Dec 2021 07:51:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 04 Dec 2021 07:51:56 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:51:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Dec 2021 07:51:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157eac698795baeacb3153cf2bbbc17f348e477e8062fa45b6728e97dd02e157`  
		Last Modified: Sat, 04 Dec 2021 07:54:19 GMT  
		Size: 4.5 MB (4518555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5241fcba964a14f9c4681ebcc94815a476df86f68c628494f5759a3bee8514`  
		Last Modified: Sat, 04 Dec 2021 07:54:16 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d02df08ee2f75a857120c105153a83b2b951337a87e902260e70e1de20dfd0`  
		Last Modified: Sat, 04 Dec 2021 07:54:16 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f1e7262504ed73a185ee16f6a6da14c19c3a76120f2b22c51a051a0988ac3bdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e483df89c189235b79aa4a9d2417378172236dba6fa85f6d5a0bb35756835f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 03 Dec 2021 16:57:10 GMT
ENV NATS_SERVER=2.6.6
# Fri, 03 Dec 2021 16:57:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 03 Dec 2021 16:57:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 03 Dec 2021 16:57:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 03 Dec 2021 16:57:16 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 16:57:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdee3b2a5421d3ceb50b8101857ce4c0815c4532476e1f292867c63034c08f61`  
		Last Modified: Fri, 03 Dec 2021 16:58:22 GMT  
		Size: 4.5 MB (4474835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a771880289bb86cd368ca8b39620b0cfe69694646e061ff6975f959ccfcd29`  
		Last Modified: Fri, 03 Dec 2021 16:58:21 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438c5abdffd6599ac83fe661d26a9491552d63f48aeb9147609299ee11b78c78`  
		Last Modified: Fri, 03 Dec 2021 16:58:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-alpine3.14`

```console
$ docker pull nats@sha256:8e2e34eb798631cd76f341277f529f78618a2366d81b59586d3b81f6cb839b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6.6-alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:687f39ecdab1eeda8a4eaa7b7210586d96698faa5e5e7e47aaf5ef8084d504e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7689543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5dc2cfb512e016e62911eca35c050a2eb5ca4b783d5f2d413ba64c68c420bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 03 Dec 2021 21:22:18 GMT
ENV NATS_SERVER=2.6.6
# Fri, 03 Dec 2021 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 03 Dec 2021 21:22:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 03 Dec 2021 21:22:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 03 Dec 2021 21:22:22 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:22:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 21:22:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeb19d8d614f4a1df58ed04d3c72469fa9f7286c9d5482ee274405723b5e645`  
		Last Modified: Fri, 03 Dec 2021 21:23:37 GMT  
		Size: 4.9 MB (4865593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51c3679390c1ab0c5f5e6786505ad9278d45683059fc7fac0298dcbb6dede86`  
		Last Modified: Fri, 03 Dec 2021 21:23:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14f15cf01b25470e7340acc8ca0860eb4a00a7e1b5d5180bd7c23db1dd273af`  
		Last Modified: Fri, 03 Dec 2021 21:23:36 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6-alpine3.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:d42d25248435c99492dd0fbcd97688486c692c680069bc9a1eb8a7b1c85eebff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7161537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae84a8c7e689bc4d7fd2915ef9aaf1fb624c094cb183af5863d4b20984f29cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Thu, 02 Dec 2021 22:49:35 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 22:49:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Dec 2021 22:49:41 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 22:49:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c7b89c441a056fc0e4d867cd4fd28308f188bd0f6b306e5feee96fee47cbdf`  
		Last Modified: Thu, 02 Dec 2021 22:51:52 GMT  
		Size: 4.5 MB (4525169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67a5f3b97f233f2d6d30a90acd85b9e856cb9b98c298b71e2b5cbae3e0268cf`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706486ffe19b237b40203ebf10cb1110d7566cba5a3c10bf738be70173a1aa69`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6-alpine3.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:dbc345345cfc225bd88b35e80f85f412483db712134bde3a0e4d959cb543350f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6958146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaa47180fd5390c3f39b81e39db30c26897fc1b070c064d4677ebdd14c1f801`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 04 Dec 2021 07:51:50 GMT
ENV NATS_SERVER=2.6.6
# Sat, 04 Dec 2021 07:51:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 04 Dec 2021 07:51:55 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 04 Dec 2021 07:51:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 04 Dec 2021 07:51:56 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:51:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Dec 2021 07:51:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157eac698795baeacb3153cf2bbbc17f348e477e8062fa45b6728e97dd02e157`  
		Last Modified: Sat, 04 Dec 2021 07:54:19 GMT  
		Size: 4.5 MB (4518555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5241fcba964a14f9c4681ebcc94815a476df86f68c628494f5759a3bee8514`  
		Last Modified: Sat, 04 Dec 2021 07:54:16 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d02df08ee2f75a857120c105153a83b2b951337a87e902260e70e1de20dfd0`  
		Last Modified: Sat, 04 Dec 2021 07:54:16 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f1e7262504ed73a185ee16f6a6da14c19c3a76120f2b22c51a051a0988ac3bdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e483df89c189235b79aa4a9d2417378172236dba6fa85f6d5a0bb35756835f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 03 Dec 2021 16:57:10 GMT
ENV NATS_SERVER=2.6.6
# Fri, 03 Dec 2021 16:57:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 03 Dec 2021 16:57:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 03 Dec 2021 16:57:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 03 Dec 2021 16:57:16 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 16:57:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdee3b2a5421d3ceb50b8101857ce4c0815c4532476e1f292867c63034c08f61`  
		Last Modified: Fri, 03 Dec 2021 16:58:22 GMT  
		Size: 4.5 MB (4474835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a771880289bb86cd368ca8b39620b0cfe69694646e061ff6975f959ccfcd29`  
		Last Modified: Fri, 03 Dec 2021 16:58:21 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438c5abdffd6599ac83fe661d26a9491552d63f48aeb9147609299ee11b78c78`  
		Last Modified: Fri, 03 Dec 2021 16:58:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-linux`

```console
$ docker pull nats@sha256:5d130fed2ad109f922a3a52e45c0b87c0d5a674ad432024cb3d45f898cf425b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6.6-linux` - linux; amd64

```console
$ docker pull nats@sha256:dad4f69520337c2a80d2a9123963c971836f07f530cf4b7c56dde98a622e0a6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba73da93bdda8525a9f473851ee3de9a2d23c21e1d0a51d7da118bc122df420`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 21:23:03 GMT
COPY file:4070919cac43aa01e3ef5dd95589f24a9d649dcc7b4d6364927c764b1f90392e in /nats-server 
# Fri, 03 Dec 2021 21:23:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 21:23:04 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:23:04 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 21:23:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:730cae3de796bb1fbb06f0f847317c2b738bf9af9d1233daafcf2f708eade5ec`  
		Last Modified: Fri, 03 Dec 2021 21:24:01 GMT  
		Size: 4.6 MB (4577696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39027e71725d02ee81938943fd0f3e980f01abbe21c5e8f8ea8219687aaae862`  
		Last Modified: Fri, 03 Dec 2021 21:24:00 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:78ee1d57413d89c46e808dbb121ad895537b74af783c6e6189366afa07638b66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3276dd6f6de73a2af8ca0c6bd2dc88c7f7ae0a0ce334bcae39c14047aab540`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:025e99b21a301a69c768cc2c72e67c371165b6314d59d0a5a95958216fd24eac in /nats-server 
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 04 Dec 2021 07:52:29 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:52:29 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 04 Dec 2021 07:52:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:75a8e365d6e58c8d8f7fe944a206f76f3e800542aca1b53e849c4bffc78fd22d`  
		Last Modified: Sat, 04 Dec 2021 07:55:01 GMT  
		Size: 4.2 MB (4237211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2920e0912e6a42ee2fd0b7b8b31c6cca01c6c99f16c760f904492422ff7cae`  
		Last Modified: Sat, 04 Dec 2021 07:54:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8ecffb2097f683980b94450d536a99c79b3fe7654f8bc91fd1c45ad0825e6aae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb404fba49386fc48ceb05ee04604d317ff225da69f159d0bd4cc63a930c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 16:57:31 GMT
COPY file:b5f62686ba6debf89a42d2be7c4442db5f8735dba6b8932e6f01f315a2e63e27 in /nats-server 
# Fri, 03 Dec 2021 16:57:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 16:57:32 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 16:57:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44ff62bde832e2b2bca85708fd2fc86d7d6d1f4ca7c58b5d0e18e3d07c9c5bac`  
		Last Modified: Fri, 03 Dec 2021 16:58:50 GMT  
		Size: 4.2 MB (4189288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcbc70566b6f8312605c0214812444ccad7a55594fa2e7f0792c21af818ef0`  
		Last Modified: Fri, 03 Dec 2021 16:58:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-nanoserver`

```console
$ docker pull nats@sha256:b35a028eb89d68dd32700c5ea035a6ab326a311d002970977341a82f6a785c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `nats:2.6.6-nanoserver` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d5b187939141b66d0480e6dd5e3b878abd5372efc6f4f26a92b7c0029ea48056
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107547635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96befd294a3f45573c0d15724d0700dbff10edac97ede11a013bffad728168e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 04:34:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4f56553f84cd7b4574c0b4d1ee6585d70eda0c9f3a5f1b276ec5e7cdc713bd74`  
		Last Modified: Sat, 18 Dec 2021 08:06:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc8a1565220717c5c64229e0ba21ccd6622cde8482e3c124233dfa9003b60cd`  
		Last Modified: Wed, 29 Dec 2021 13:24:21 GMT  
		Size: 4.6 MB (4637251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883fbea1eb1283a4bbf26392acf172e4ef79b4ab0b4778d46f4b1a84493b1dca`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939ae0d8b1fb893c6f64343b668aa03be89852764eb042ee8803cda7f6a8cd78`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca947ae0ca6d9fe8fb291c8d5bd0fb944a8eb0d77d86744b85f13d91431ac9b3`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0aaab409f72994f4e3999f144ef170ad74faff15cb7507c2acab06bf80cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-nanoserver-1809`

```console
$ docker pull nats@sha256:b35a028eb89d68dd32700c5ea035a6ab326a311d002970977341a82f6a785c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `nats:2.6.6-nanoserver-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d5b187939141b66d0480e6dd5e3b878abd5372efc6f4f26a92b7c0029ea48056
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107547635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96befd294a3f45573c0d15724d0700dbff10edac97ede11a013bffad728168e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 04:34:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4f56553f84cd7b4574c0b4d1ee6585d70eda0c9f3a5f1b276ec5e7cdc713bd74`  
		Last Modified: Sat, 18 Dec 2021 08:06:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc8a1565220717c5c64229e0ba21ccd6622cde8482e3c124233dfa9003b60cd`  
		Last Modified: Wed, 29 Dec 2021 13:24:21 GMT  
		Size: 4.6 MB (4637251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883fbea1eb1283a4bbf26392acf172e4ef79b4ab0b4778d46f4b1a84493b1dca`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939ae0d8b1fb893c6f64343b668aa03be89852764eb042ee8803cda7f6a8cd78`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca947ae0ca6d9fe8fb291c8d5bd0fb944a8eb0d77d86744b85f13d91431ac9b3`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0aaab409f72994f4e3999f144ef170ad74faff15cb7507c2acab06bf80cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-scratch`

```console
$ docker pull nats@sha256:5d130fed2ad109f922a3a52e45c0b87c0d5a674ad432024cb3d45f898cf425b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6.6-scratch` - linux; amd64

```console
$ docker pull nats@sha256:dad4f69520337c2a80d2a9123963c971836f07f530cf4b7c56dde98a622e0a6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba73da93bdda8525a9f473851ee3de9a2d23c21e1d0a51d7da118bc122df420`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 21:23:03 GMT
COPY file:4070919cac43aa01e3ef5dd95589f24a9d649dcc7b4d6364927c764b1f90392e in /nats-server 
# Fri, 03 Dec 2021 21:23:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 21:23:04 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:23:04 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 21:23:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:730cae3de796bb1fbb06f0f847317c2b738bf9af9d1233daafcf2f708eade5ec`  
		Last Modified: Fri, 03 Dec 2021 21:24:01 GMT  
		Size: 4.6 MB (4577696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39027e71725d02ee81938943fd0f3e980f01abbe21c5e8f8ea8219687aaae862`  
		Last Modified: Fri, 03 Dec 2021 21:24:00 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:78ee1d57413d89c46e808dbb121ad895537b74af783c6e6189366afa07638b66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3276dd6f6de73a2af8ca0c6bd2dc88c7f7ae0a0ce334bcae39c14047aab540`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:025e99b21a301a69c768cc2c72e67c371165b6314d59d0a5a95958216fd24eac in /nats-server 
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 04 Dec 2021 07:52:29 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:52:29 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 04 Dec 2021 07:52:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:75a8e365d6e58c8d8f7fe944a206f76f3e800542aca1b53e849c4bffc78fd22d`  
		Last Modified: Sat, 04 Dec 2021 07:55:01 GMT  
		Size: 4.2 MB (4237211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2920e0912e6a42ee2fd0b7b8b31c6cca01c6c99f16c760f904492422ff7cae`  
		Last Modified: Sat, 04 Dec 2021 07:54:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8ecffb2097f683980b94450d536a99c79b3fe7654f8bc91fd1c45ad0825e6aae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb404fba49386fc48ceb05ee04604d317ff225da69f159d0bd4cc63a930c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 16:57:31 GMT
COPY file:b5f62686ba6debf89a42d2be7c4442db5f8735dba6b8932e6f01f315a2e63e27 in /nats-server 
# Fri, 03 Dec 2021 16:57:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 16:57:32 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 16:57:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44ff62bde832e2b2bca85708fd2fc86d7d6d1f4ca7c58b5d0e18e3d07c9c5bac`  
		Last Modified: Fri, 03 Dec 2021 16:58:50 GMT  
		Size: 4.2 MB (4189288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcbc70566b6f8312605c0214812444ccad7a55594fa2e7f0792c21af818ef0`  
		Last Modified: Fri, 03 Dec 2021 16:58:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-windowsservercore`

```console
$ docker pull nats@sha256:13bb711f4847d1af1afafb5c962f574ecfeb01b1ab37fb2f3f328d2da02f40df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2366; amd64
	-	windows version 10.0.14393.4825; amd64

### `nats:2.6.6-windowsservercore` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d232cd8a1f4e7e8e07cab41c7df5e76a7621d4dab30d1d3010ce1a80d71d0031
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2713981684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72d62160474997048b207a63be5355a15b11e62f414d223416d6920c00e08d2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Sat, 18 Dec 2021 01:40:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 18 Dec 2021 04:32:10 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:32:10 GMT
ENV NATS_SERVER=2.6.6
# Sat, 18 Dec 2021 04:32:11 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Sat, 18 Dec 2021 04:32:12 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Sat, 18 Dec 2021 04:33:08 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Dec 2021 04:34:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Sat, 18 Dec 2021 04:34:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:27 GMT
EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d22d2238b031d3f13bcd6c144e80f8f8402332b8ee8e53cc54b7912c3ac808cb`  
		Last Modified: Sat, 18 Dec 2021 03:59:34 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c5f7f5394b88876960b5ac27980fb2e22584cf50ecde4d9537e88ddbf849c3`  
		Last Modified: Sat, 18 Dec 2021 08:06:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db095798002004c7354bde24c88ee14ba02e430ccfe960c761470e023d0549e`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0362f786811b6ac9b6dbbc36403b1ea4e26ffe73ca7a49ccbb06f1fb9403f315`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ef6c82efd2b3c96cdce7abcace76e1231881bfe847245fbae17e80674ed7bb`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5680cfa178ed5d45ba63a530d80c2b6e96002029544bfa9b2923e63a16f729cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 365.8 KB (365820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9fa2a9d1117be676892e9ced2a72a88583d6b54d4c61de0eb6f92b937b2d9d`  
		Last Modified: Wed, 29 Dec 2021 13:24:05 GMT  
		Size: 5.0 MB (4998116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c2686658f0d823b26ef428ef67cf347e470511ca1675365bbb286131925754`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eb06c9a0a37ab81dde05f4196f65ba87c5cab394a6333a3258f8d737d87571`  
		Last Modified: Wed, 29 Dec 2021 13:23:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db8a42caf1046ab762e7e442960441653dbf5854db77c937eb332552d8fc2ac`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b0fad0cdb1e2a3ebb2f7f59a2d5fc2f11486fe57937c012b4e76f26ac7524d`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6.6-windowsservercore` - windows version 10.0.14393.4825; amd64

```console
$ docker pull nats@sha256:70298f4fa8023d6a4d2a21c616ac79a3cb9cc8fff4e00f83ce618b7d237fb30e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6280045896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed150f48d56334a037ca5957d0291e7226e8088f5051e674f85f38bdf616f32`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 08 Dec 2021 08:38:00 GMT
RUN Install update ltsc2016-amd64
# Sat, 18 Dec 2021 01:55:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 18 Dec 2021 04:34:51 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:52 GMT
ENV NATS_SERVER=2.6.6
# Sat, 18 Dec 2021 04:34:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Sat, 18 Dec 2021 04:34:53 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Sat, 18 Dec 2021 04:35:50 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Dec 2021 04:37:24 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Sat, 18 Dec 2021 04:37:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:37:26 GMT
EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:37:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:37:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d026d646213ccf73d9f0584941d108253d62e73df2a74e070776884b7b0242b`  
		Size: 2.2 GB (2204728802 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6bffd19db3f71ba2031bea25a529c67034869e7e1bbf9e2431d5ee747bd6d6d`  
		Last Modified: Sat, 18 Dec 2021 04:00:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05006360e7d5d5f0fc5160410fd98cfab768e620dca3f3fbc5b44e611e3039b4`  
		Last Modified: Sat, 18 Dec 2021 08:06:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3409aa65b2e0951ea84912add432d4791b9410b3e7a3d6d5df8244185c447e97`  
		Last Modified: Wed, 29 Dec 2021 13:24:39 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b9931dce79731d8fc8f9aae5bb18374967450b16fbcdfd0a2da48dd3efe853`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a5ed1a9ed62c133c6a9b7716fba9971e3f97b64477de601e28cc3ca5b05c8b`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c69ccdace4415c2bdec7795fab2a239ce07eb9906db4b613e2f024a20433a5`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 331.3 KB (331314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b3ee24e2d2850f329b382be9ade011322d08041d68c519d1a03fe3673639af`  
		Last Modified: Wed, 29 Dec 2021 13:24:41 GMT  
		Size: 5.0 MB (4986765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a195460559eca4221d68693a9db0cff883762ae3c2db047097b924a1b368b2`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed2147e829d4d68e6c2022d8fcdaf109525ad0e2b99f88eb2fccf2a746d507c`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfe2741387f6d51946ffb233018a1523759ecf1633a6c8a647410ec3095b16c`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508de22e92ac689a8f2b98d8314afdae274bf00f2d37ab78fbd17452c67a2e26`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-windowsservercore-1809`

```console
$ docker pull nats@sha256:1ba92dc8d94836ff1669b1c5a13754529e799eb1f4455e8598f74e2a5a0758df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `nats:2.6.6-windowsservercore-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d232cd8a1f4e7e8e07cab41c7df5e76a7621d4dab30d1d3010ce1a80d71d0031
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2713981684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72d62160474997048b207a63be5355a15b11e62f414d223416d6920c00e08d2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Sat, 18 Dec 2021 01:40:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 18 Dec 2021 04:32:10 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:32:10 GMT
ENV NATS_SERVER=2.6.6
# Sat, 18 Dec 2021 04:32:11 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Sat, 18 Dec 2021 04:32:12 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Sat, 18 Dec 2021 04:33:08 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Dec 2021 04:34:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Sat, 18 Dec 2021 04:34:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:27 GMT
EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d22d2238b031d3f13bcd6c144e80f8f8402332b8ee8e53cc54b7912c3ac808cb`  
		Last Modified: Sat, 18 Dec 2021 03:59:34 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c5f7f5394b88876960b5ac27980fb2e22584cf50ecde4d9537e88ddbf849c3`  
		Last Modified: Sat, 18 Dec 2021 08:06:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db095798002004c7354bde24c88ee14ba02e430ccfe960c761470e023d0549e`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0362f786811b6ac9b6dbbc36403b1ea4e26ffe73ca7a49ccbb06f1fb9403f315`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ef6c82efd2b3c96cdce7abcace76e1231881bfe847245fbae17e80674ed7bb`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5680cfa178ed5d45ba63a530d80c2b6e96002029544bfa9b2923e63a16f729cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 365.8 KB (365820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9fa2a9d1117be676892e9ced2a72a88583d6b54d4c61de0eb6f92b937b2d9d`  
		Last Modified: Wed, 29 Dec 2021 13:24:05 GMT  
		Size: 5.0 MB (4998116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c2686658f0d823b26ef428ef67cf347e470511ca1675365bbb286131925754`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eb06c9a0a37ab81dde05f4196f65ba87c5cab394a6333a3258f8d737d87571`  
		Last Modified: Wed, 29 Dec 2021 13:23:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db8a42caf1046ab762e7e442960441653dbf5854db77c937eb332552d8fc2ac`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b0fad0cdb1e2a3ebb2f7f59a2d5fc2f11486fe57937c012b4e76f26ac7524d`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.6-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:f684eb2487b5e3aa125e4d0bff1a7b94bde1929252423f1b70fe773365dc1704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4825; amd64

### `nats:2.6.6-windowsservercore-ltsc2016` - windows version 10.0.14393.4825; amd64

```console
$ docker pull nats@sha256:70298f4fa8023d6a4d2a21c616ac79a3cb9cc8fff4e00f83ce618b7d237fb30e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6280045896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed150f48d56334a037ca5957d0291e7226e8088f5051e674f85f38bdf616f32`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 08 Dec 2021 08:38:00 GMT
RUN Install update ltsc2016-amd64
# Sat, 18 Dec 2021 01:55:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 18 Dec 2021 04:34:51 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:52 GMT
ENV NATS_SERVER=2.6.6
# Sat, 18 Dec 2021 04:34:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Sat, 18 Dec 2021 04:34:53 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Sat, 18 Dec 2021 04:35:50 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Dec 2021 04:37:24 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Sat, 18 Dec 2021 04:37:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:37:26 GMT
EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:37:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:37:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d026d646213ccf73d9f0584941d108253d62e73df2a74e070776884b7b0242b`  
		Size: 2.2 GB (2204728802 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6bffd19db3f71ba2031bea25a529c67034869e7e1bbf9e2431d5ee747bd6d6d`  
		Last Modified: Sat, 18 Dec 2021 04:00:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05006360e7d5d5f0fc5160410fd98cfab768e620dca3f3fbc5b44e611e3039b4`  
		Last Modified: Sat, 18 Dec 2021 08:06:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3409aa65b2e0951ea84912add432d4791b9410b3e7a3d6d5df8244185c447e97`  
		Last Modified: Wed, 29 Dec 2021 13:24:39 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b9931dce79731d8fc8f9aae5bb18374967450b16fbcdfd0a2da48dd3efe853`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a5ed1a9ed62c133c6a9b7716fba9971e3f97b64477de601e28cc3ca5b05c8b`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c69ccdace4415c2bdec7795fab2a239ce07eb9906db4b613e2f024a20433a5`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 331.3 KB (331314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b3ee24e2d2850f329b382be9ade011322d08041d68c519d1a03fe3673639af`  
		Last Modified: Wed, 29 Dec 2021 13:24:41 GMT  
		Size: 5.0 MB (4986765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a195460559eca4221d68693a9db0cff883762ae3c2db047097b924a1b368b2`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed2147e829d4d68e6c2022d8fcdaf109525ad0e2b99f88eb2fccf2a746d507c`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfe2741387f6d51946ffb233018a1523759ecf1633a6c8a647410ec3095b16c`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508de22e92ac689a8f2b98d8314afdae274bf00f2d37ab78fbd17452c67a2e26`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:8e2e34eb798631cd76f341277f529f78618a2366d81b59586d3b81f6cb839b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:687f39ecdab1eeda8a4eaa7b7210586d96698faa5e5e7e47aaf5ef8084d504e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7689543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5dc2cfb512e016e62911eca35c050a2eb5ca4b783d5f2d413ba64c68c420bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 03 Dec 2021 21:22:18 GMT
ENV NATS_SERVER=2.6.6
# Fri, 03 Dec 2021 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 03 Dec 2021 21:22:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 03 Dec 2021 21:22:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 03 Dec 2021 21:22:22 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:22:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 21:22:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeb19d8d614f4a1df58ed04d3c72469fa9f7286c9d5482ee274405723b5e645`  
		Last Modified: Fri, 03 Dec 2021 21:23:37 GMT  
		Size: 4.9 MB (4865593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51c3679390c1ab0c5f5e6786505ad9278d45683059fc7fac0298dcbb6dede86`  
		Last Modified: Fri, 03 Dec 2021 21:23:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14f15cf01b25470e7340acc8ca0860eb4a00a7e1b5d5180bd7c23db1dd273af`  
		Last Modified: Fri, 03 Dec 2021 21:23:36 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d42d25248435c99492dd0fbcd97688486c692c680069bc9a1eb8a7b1c85eebff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7161537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae84a8c7e689bc4d7fd2915ef9aaf1fb624c094cb183af5863d4b20984f29cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Thu, 02 Dec 2021 22:49:35 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 22:49:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Dec 2021 22:49:41 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 22:49:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c7b89c441a056fc0e4d867cd4fd28308f188bd0f6b306e5feee96fee47cbdf`  
		Last Modified: Thu, 02 Dec 2021 22:51:52 GMT  
		Size: 4.5 MB (4525169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67a5f3b97f233f2d6d30a90acd85b9e856cb9b98c298b71e2b5cbae3e0268cf`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706486ffe19b237b40203ebf10cb1110d7566cba5a3c10bf738be70173a1aa69`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:dbc345345cfc225bd88b35e80f85f412483db712134bde3a0e4d959cb543350f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6958146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaa47180fd5390c3f39b81e39db30c26897fc1b070c064d4677ebdd14c1f801`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 04 Dec 2021 07:51:50 GMT
ENV NATS_SERVER=2.6.6
# Sat, 04 Dec 2021 07:51:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 04 Dec 2021 07:51:55 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 04 Dec 2021 07:51:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 04 Dec 2021 07:51:56 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:51:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Dec 2021 07:51:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157eac698795baeacb3153cf2bbbc17f348e477e8062fa45b6728e97dd02e157`  
		Last Modified: Sat, 04 Dec 2021 07:54:19 GMT  
		Size: 4.5 MB (4518555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5241fcba964a14f9c4681ebcc94815a476df86f68c628494f5759a3bee8514`  
		Last Modified: Sat, 04 Dec 2021 07:54:16 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d02df08ee2f75a857120c105153a83b2b951337a87e902260e70e1de20dfd0`  
		Last Modified: Sat, 04 Dec 2021 07:54:16 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f1e7262504ed73a185ee16f6a6da14c19c3a76120f2b22c51a051a0988ac3bdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e483df89c189235b79aa4a9d2417378172236dba6fa85f6d5a0bb35756835f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 03 Dec 2021 16:57:10 GMT
ENV NATS_SERVER=2.6.6
# Fri, 03 Dec 2021 16:57:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 03 Dec 2021 16:57:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 03 Dec 2021 16:57:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 03 Dec 2021 16:57:16 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 16:57:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdee3b2a5421d3ceb50b8101857ce4c0815c4532476e1f292867c63034c08f61`  
		Last Modified: Fri, 03 Dec 2021 16:58:22 GMT  
		Size: 4.5 MB (4474835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a771880289bb86cd368ca8b39620b0cfe69694646e061ff6975f959ccfcd29`  
		Last Modified: Fri, 03 Dec 2021 16:58:21 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438c5abdffd6599ac83fe661d26a9491552d63f48aeb9147609299ee11b78c78`  
		Last Modified: Fri, 03 Dec 2021 16:58:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.14`

```console
$ docker pull nats@sha256:8e2e34eb798631cd76f341277f529f78618a2366d81b59586d3b81f6cb839b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:687f39ecdab1eeda8a4eaa7b7210586d96698faa5e5e7e47aaf5ef8084d504e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7689543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5dc2cfb512e016e62911eca35c050a2eb5ca4b783d5f2d413ba64c68c420bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 03 Dec 2021 21:22:18 GMT
ENV NATS_SERVER=2.6.6
# Fri, 03 Dec 2021 21:22:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 03 Dec 2021 21:22:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 03 Dec 2021 21:22:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 03 Dec 2021 21:22:22 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:22:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 21:22:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeb19d8d614f4a1df58ed04d3c72469fa9f7286c9d5482ee274405723b5e645`  
		Last Modified: Fri, 03 Dec 2021 21:23:37 GMT  
		Size: 4.9 MB (4865593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51c3679390c1ab0c5f5e6786505ad9278d45683059fc7fac0298dcbb6dede86`  
		Last Modified: Fri, 03 Dec 2021 21:23:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14f15cf01b25470e7340acc8ca0860eb4a00a7e1b5d5180bd7c23db1dd273af`  
		Last Modified: Fri, 03 Dec 2021 21:23:36 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:d42d25248435c99492dd0fbcd97688486c692c680069bc9a1eb8a7b1c85eebff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7161537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae84a8c7e689bc4d7fd2915ef9aaf1fb624c094cb183af5863d4b20984f29cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Thu, 02 Dec 2021 22:49:35 GMT
ENV NATS_SERVER=2.6.6
# Thu, 02 Dec 2021 22:49:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 02 Dec 2021 22:49:40 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 02 Dec 2021 22:49:41 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:49:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Dec 2021 22:49:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c7b89c441a056fc0e4d867cd4fd28308f188bd0f6b306e5feee96fee47cbdf`  
		Last Modified: Thu, 02 Dec 2021 22:51:52 GMT  
		Size: 4.5 MB (4525169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67a5f3b97f233f2d6d30a90acd85b9e856cb9b98c298b71e2b5cbae3e0268cf`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706486ffe19b237b40203ebf10cb1110d7566cba5a3c10bf738be70173a1aa69`  
		Last Modified: Thu, 02 Dec 2021 22:51:50 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:dbc345345cfc225bd88b35e80f85f412483db712134bde3a0e4d959cb543350f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6958146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaa47180fd5390c3f39b81e39db30c26897fc1b070c064d4677ebdd14c1f801`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 04 Dec 2021 07:51:50 GMT
ENV NATS_SERVER=2.6.6
# Sat, 04 Dec 2021 07:51:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 04 Dec 2021 07:51:55 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Sat, 04 Dec 2021 07:51:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 04 Dec 2021 07:51:56 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:51:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Dec 2021 07:51:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157eac698795baeacb3153cf2bbbc17f348e477e8062fa45b6728e97dd02e157`  
		Last Modified: Sat, 04 Dec 2021 07:54:19 GMT  
		Size: 4.5 MB (4518555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5241fcba964a14f9c4681ebcc94815a476df86f68c628494f5759a3bee8514`  
		Last Modified: Sat, 04 Dec 2021 07:54:16 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d02df08ee2f75a857120c105153a83b2b951337a87e902260e70e1de20dfd0`  
		Last Modified: Sat, 04 Dec 2021 07:54:16 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f1e7262504ed73a185ee16f6a6da14c19c3a76120f2b22c51a051a0988ac3bdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e483df89c189235b79aa4a9d2417378172236dba6fa85f6d5a0bb35756835f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 03 Dec 2021 16:57:10 GMT
ENV NATS_SERVER=2.6.6
# Fri, 03 Dec 2021 16:57:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='70da0ad3694aebfc742f9aae919d3a4aa5b8c863946e99c5d332195fbbdad49c' ;; 		armhf) natsArch='arm6'; sha256='e2cc1e198d5d5c83e2f2c2dcb15fafb71601603e3740065682812afaa7dd443a' ;; 		armv7) natsArch='arm7'; sha256='f3698a4fb18c6664d477b920d5f07637141a6623cf2fa998900155fea0d97e61' ;; 		x86_64) natsArch='amd64'; sha256='2c2fc16322fb2bc0b166ee2a01e163d4beb2cf7b49d083cebcd36695dc05a381' ;; 		x86) natsArch='386'; sha256='1da03b0d163dc98209f010bf6efa5fc6c81a23b4bab7a98bebe142e19fc26bdc' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 03 Dec 2021 16:57:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 03 Dec 2021 16:57:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 03 Dec 2021 16:57:16 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Dec 2021 16:57:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdee3b2a5421d3ceb50b8101857ce4c0815c4532476e1f292867c63034c08f61`  
		Last Modified: Fri, 03 Dec 2021 16:58:22 GMT  
		Size: 4.5 MB (4474835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a771880289bb86cd368ca8b39620b0cfe69694646e061ff6975f959ccfcd29`  
		Last Modified: Fri, 03 Dec 2021 16:58:21 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438c5abdffd6599ac83fe661d26a9491552d63f48aeb9147609299ee11b78c78`  
		Last Modified: Fri, 03 Dec 2021 16:58:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:4d4b166c324b4e9f0853e36d62cf831c5e4bd089fc6c5932ad9a98a8f73a143e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2366; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:dad4f69520337c2a80d2a9123963c971836f07f530cf4b7c56dde98a622e0a6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba73da93bdda8525a9f473851ee3de9a2d23c21e1d0a51d7da118bc122df420`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 21:23:03 GMT
COPY file:4070919cac43aa01e3ef5dd95589f24a9d649dcc7b4d6364927c764b1f90392e in /nats-server 
# Fri, 03 Dec 2021 21:23:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 21:23:04 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:23:04 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 21:23:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:730cae3de796bb1fbb06f0f847317c2b738bf9af9d1233daafcf2f708eade5ec`  
		Last Modified: Fri, 03 Dec 2021 21:24:01 GMT  
		Size: 4.6 MB (4577696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39027e71725d02ee81938943fd0f3e980f01abbe21c5e8f8ea8219687aaae862`  
		Last Modified: Fri, 03 Dec 2021 21:24:00 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:78ee1d57413d89c46e808dbb121ad895537b74af783c6e6189366afa07638b66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3276dd6f6de73a2af8ca0c6bd2dc88c7f7ae0a0ce334bcae39c14047aab540`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:025e99b21a301a69c768cc2c72e67c371165b6314d59d0a5a95958216fd24eac in /nats-server 
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 04 Dec 2021 07:52:29 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:52:29 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 04 Dec 2021 07:52:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:75a8e365d6e58c8d8f7fe944a206f76f3e800542aca1b53e849c4bffc78fd22d`  
		Last Modified: Sat, 04 Dec 2021 07:55:01 GMT  
		Size: 4.2 MB (4237211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2920e0912e6a42ee2fd0b7b8b31c6cca01c6c99f16c760f904492422ff7cae`  
		Last Modified: Sat, 04 Dec 2021 07:54:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8ecffb2097f683980b94450d536a99c79b3fe7654f8bc91fd1c45ad0825e6aae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb404fba49386fc48ceb05ee04604d317ff225da69f159d0bd4cc63a930c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 16:57:31 GMT
COPY file:b5f62686ba6debf89a42d2be7c4442db5f8735dba6b8932e6f01f315a2e63e27 in /nats-server 
# Fri, 03 Dec 2021 16:57:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 16:57:32 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 16:57:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44ff62bde832e2b2bca85708fd2fc86d7d6d1f4ca7c58b5d0e18e3d07c9c5bac`  
		Last Modified: Fri, 03 Dec 2021 16:58:50 GMT  
		Size: 4.2 MB (4189288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcbc70566b6f8312605c0214812444ccad7a55594fa2e7f0792c21af818ef0`  
		Last Modified: Fri, 03 Dec 2021 16:58:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d5b187939141b66d0480e6dd5e3b878abd5372efc6f4f26a92b7c0029ea48056
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107547635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96befd294a3f45573c0d15724d0700dbff10edac97ede11a013bffad728168e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 04:34:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4f56553f84cd7b4574c0b4d1ee6585d70eda0c9f3a5f1b276ec5e7cdc713bd74`  
		Last Modified: Sat, 18 Dec 2021 08:06:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc8a1565220717c5c64229e0ba21ccd6622cde8482e3c124233dfa9003b60cd`  
		Last Modified: Wed, 29 Dec 2021 13:24:21 GMT  
		Size: 4.6 MB (4637251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883fbea1eb1283a4bbf26392acf172e4ef79b4ab0b4778d46f4b1a84493b1dca`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939ae0d8b1fb893c6f64343b668aa03be89852764eb042ee8803cda7f6a8cd78`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca947ae0ca6d9fe8fb291c8d5bd0fb944a8eb0d77d86744b85f13d91431ac9b3`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0aaab409f72994f4e3999f144ef170ad74faff15cb7507c2acab06bf80cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:5d130fed2ad109f922a3a52e45c0b87c0d5a674ad432024cb3d45f898cf425b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:dad4f69520337c2a80d2a9123963c971836f07f530cf4b7c56dde98a622e0a6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba73da93bdda8525a9f473851ee3de9a2d23c21e1d0a51d7da118bc122df420`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 21:23:03 GMT
COPY file:4070919cac43aa01e3ef5dd95589f24a9d649dcc7b4d6364927c764b1f90392e in /nats-server 
# Fri, 03 Dec 2021 21:23:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 21:23:04 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:23:04 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 21:23:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:730cae3de796bb1fbb06f0f847317c2b738bf9af9d1233daafcf2f708eade5ec`  
		Last Modified: Fri, 03 Dec 2021 21:24:01 GMT  
		Size: 4.6 MB (4577696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39027e71725d02ee81938943fd0f3e980f01abbe21c5e8f8ea8219687aaae862`  
		Last Modified: Fri, 03 Dec 2021 21:24:00 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:78ee1d57413d89c46e808dbb121ad895537b74af783c6e6189366afa07638b66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3276dd6f6de73a2af8ca0c6bd2dc88c7f7ae0a0ce334bcae39c14047aab540`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:025e99b21a301a69c768cc2c72e67c371165b6314d59d0a5a95958216fd24eac in /nats-server 
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 04 Dec 2021 07:52:29 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:52:29 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 04 Dec 2021 07:52:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:75a8e365d6e58c8d8f7fe944a206f76f3e800542aca1b53e849c4bffc78fd22d`  
		Last Modified: Sat, 04 Dec 2021 07:55:01 GMT  
		Size: 4.2 MB (4237211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2920e0912e6a42ee2fd0b7b8b31c6cca01c6c99f16c760f904492422ff7cae`  
		Last Modified: Sat, 04 Dec 2021 07:54:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8ecffb2097f683980b94450d536a99c79b3fe7654f8bc91fd1c45ad0825e6aae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb404fba49386fc48ceb05ee04604d317ff225da69f159d0bd4cc63a930c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 16:57:31 GMT
COPY file:b5f62686ba6debf89a42d2be7c4442db5f8735dba6b8932e6f01f315a2e63e27 in /nats-server 
# Fri, 03 Dec 2021 16:57:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 16:57:32 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 16:57:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44ff62bde832e2b2bca85708fd2fc86d7d6d1f4ca7c58b5d0e18e3d07c9c5bac`  
		Last Modified: Fri, 03 Dec 2021 16:58:50 GMT  
		Size: 4.2 MB (4189288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcbc70566b6f8312605c0214812444ccad7a55594fa2e7f0792c21af818ef0`  
		Last Modified: Fri, 03 Dec 2021 16:58:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:b35a028eb89d68dd32700c5ea035a6ab326a311d002970977341a82f6a785c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `nats:nanoserver` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d5b187939141b66d0480e6dd5e3b878abd5372efc6f4f26a92b7c0029ea48056
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107547635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96befd294a3f45573c0d15724d0700dbff10edac97ede11a013bffad728168e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 04:34:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4f56553f84cd7b4574c0b4d1ee6585d70eda0c9f3a5f1b276ec5e7cdc713bd74`  
		Last Modified: Sat, 18 Dec 2021 08:06:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc8a1565220717c5c64229e0ba21ccd6622cde8482e3c124233dfa9003b60cd`  
		Last Modified: Wed, 29 Dec 2021 13:24:21 GMT  
		Size: 4.6 MB (4637251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883fbea1eb1283a4bbf26392acf172e4ef79b4ab0b4778d46f4b1a84493b1dca`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939ae0d8b1fb893c6f64343b668aa03be89852764eb042ee8803cda7f6a8cd78`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca947ae0ca6d9fe8fb291c8d5bd0fb944a8eb0d77d86744b85f13d91431ac9b3`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0aaab409f72994f4e3999f144ef170ad74faff15cb7507c2acab06bf80cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:b35a028eb89d68dd32700c5ea035a6ab326a311d002970977341a82f6a785c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d5b187939141b66d0480e6dd5e3b878abd5372efc6f4f26a92b7c0029ea48056
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107547635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96befd294a3f45573c0d15724d0700dbff10edac97ede11a013bffad728168e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 04:34:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4f56553f84cd7b4574c0b4d1ee6585d70eda0c9f3a5f1b276ec5e7cdc713bd74`  
		Last Modified: Sat, 18 Dec 2021 08:06:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc8a1565220717c5c64229e0ba21ccd6622cde8482e3c124233dfa9003b60cd`  
		Last Modified: Wed, 29 Dec 2021 13:24:21 GMT  
		Size: 4.6 MB (4637251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883fbea1eb1283a4bbf26392acf172e4ef79b4ab0b4778d46f4b1a84493b1dca`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939ae0d8b1fb893c6f64343b668aa03be89852764eb042ee8803cda7f6a8cd78`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca947ae0ca6d9fe8fb291c8d5bd0fb944a8eb0d77d86744b85f13d91431ac9b3`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0aaab409f72994f4e3999f144ef170ad74faff15cb7507c2acab06bf80cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:5d130fed2ad109f922a3a52e45c0b87c0d5a674ad432024cb3d45f898cf425b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:dad4f69520337c2a80d2a9123963c971836f07f530cf4b7c56dde98a622e0a6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba73da93bdda8525a9f473851ee3de9a2d23c21e1d0a51d7da118bc122df420`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 21:23:03 GMT
COPY file:4070919cac43aa01e3ef5dd95589f24a9d649dcc7b4d6364927c764b1f90392e in /nats-server 
# Fri, 03 Dec 2021 21:23:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 21:23:04 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:23:04 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 21:23:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:730cae3de796bb1fbb06f0f847317c2b738bf9af9d1233daafcf2f708eade5ec`  
		Last Modified: Fri, 03 Dec 2021 21:24:01 GMT  
		Size: 4.6 MB (4577696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39027e71725d02ee81938943fd0f3e980f01abbe21c5e8f8ea8219687aaae862`  
		Last Modified: Fri, 03 Dec 2021 21:24:00 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:78ee1d57413d89c46e808dbb121ad895537b74af783c6e6189366afa07638b66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3276dd6f6de73a2af8ca0c6bd2dc88c7f7ae0a0ce334bcae39c14047aab540`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:025e99b21a301a69c768cc2c72e67c371165b6314d59d0a5a95958216fd24eac in /nats-server 
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 04 Dec 2021 07:52:29 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:52:29 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 04 Dec 2021 07:52:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:75a8e365d6e58c8d8f7fe944a206f76f3e800542aca1b53e849c4bffc78fd22d`  
		Last Modified: Sat, 04 Dec 2021 07:55:01 GMT  
		Size: 4.2 MB (4237211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2920e0912e6a42ee2fd0b7b8b31c6cca01c6c99f16c760f904492422ff7cae`  
		Last Modified: Sat, 04 Dec 2021 07:54:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8ecffb2097f683980b94450d536a99c79b3fe7654f8bc91fd1c45ad0825e6aae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb404fba49386fc48ceb05ee04604d317ff225da69f159d0bd4cc63a930c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 16:57:31 GMT
COPY file:b5f62686ba6debf89a42d2be7c4442db5f8735dba6b8932e6f01f315a2e63e27 in /nats-server 
# Fri, 03 Dec 2021 16:57:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 16:57:32 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 16:57:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44ff62bde832e2b2bca85708fd2fc86d7d6d1f4ca7c58b5d0e18e3d07c9c5bac`  
		Last Modified: Fri, 03 Dec 2021 16:58:50 GMT  
		Size: 4.2 MB (4189288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcbc70566b6f8312605c0214812444ccad7a55594fa2e7f0792c21af818ef0`  
		Last Modified: Fri, 03 Dec 2021 16:58:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:13bb711f4847d1af1afafb5c962f574ecfeb01b1ab37fb2f3f328d2da02f40df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2366; amd64
	-	windows version 10.0.14393.4825; amd64

### `nats:windowsservercore` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d232cd8a1f4e7e8e07cab41c7df5e76a7621d4dab30d1d3010ce1a80d71d0031
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2713981684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72d62160474997048b207a63be5355a15b11e62f414d223416d6920c00e08d2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Sat, 18 Dec 2021 01:40:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 18 Dec 2021 04:32:10 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:32:10 GMT
ENV NATS_SERVER=2.6.6
# Sat, 18 Dec 2021 04:32:11 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Sat, 18 Dec 2021 04:32:12 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Sat, 18 Dec 2021 04:33:08 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Dec 2021 04:34:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Sat, 18 Dec 2021 04:34:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:27 GMT
EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d22d2238b031d3f13bcd6c144e80f8f8402332b8ee8e53cc54b7912c3ac808cb`  
		Last Modified: Sat, 18 Dec 2021 03:59:34 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c5f7f5394b88876960b5ac27980fb2e22584cf50ecde4d9537e88ddbf849c3`  
		Last Modified: Sat, 18 Dec 2021 08:06:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db095798002004c7354bde24c88ee14ba02e430ccfe960c761470e023d0549e`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0362f786811b6ac9b6dbbc36403b1ea4e26ffe73ca7a49ccbb06f1fb9403f315`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ef6c82efd2b3c96cdce7abcace76e1231881bfe847245fbae17e80674ed7bb`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5680cfa178ed5d45ba63a530d80c2b6e96002029544bfa9b2923e63a16f729cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 365.8 KB (365820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9fa2a9d1117be676892e9ced2a72a88583d6b54d4c61de0eb6f92b937b2d9d`  
		Last Modified: Wed, 29 Dec 2021 13:24:05 GMT  
		Size: 5.0 MB (4998116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c2686658f0d823b26ef428ef67cf347e470511ca1675365bbb286131925754`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eb06c9a0a37ab81dde05f4196f65ba87c5cab394a6333a3258f8d737d87571`  
		Last Modified: Wed, 29 Dec 2021 13:23:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db8a42caf1046ab762e7e442960441653dbf5854db77c937eb332552d8fc2ac`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b0fad0cdb1e2a3ebb2f7f59a2d5fc2f11486fe57937c012b4e76f26ac7524d`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.4825; amd64

```console
$ docker pull nats@sha256:70298f4fa8023d6a4d2a21c616ac79a3cb9cc8fff4e00f83ce618b7d237fb30e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6280045896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed150f48d56334a037ca5957d0291e7226e8088f5051e674f85f38bdf616f32`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 08 Dec 2021 08:38:00 GMT
RUN Install update ltsc2016-amd64
# Sat, 18 Dec 2021 01:55:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 18 Dec 2021 04:34:51 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:52 GMT
ENV NATS_SERVER=2.6.6
# Sat, 18 Dec 2021 04:34:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Sat, 18 Dec 2021 04:34:53 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Sat, 18 Dec 2021 04:35:50 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Dec 2021 04:37:24 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Sat, 18 Dec 2021 04:37:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:37:26 GMT
EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:37:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:37:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d026d646213ccf73d9f0584941d108253d62e73df2a74e070776884b7b0242b`  
		Size: 2.2 GB (2204728802 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6bffd19db3f71ba2031bea25a529c67034869e7e1bbf9e2431d5ee747bd6d6d`  
		Last Modified: Sat, 18 Dec 2021 04:00:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05006360e7d5d5f0fc5160410fd98cfab768e620dca3f3fbc5b44e611e3039b4`  
		Last Modified: Sat, 18 Dec 2021 08:06:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3409aa65b2e0951ea84912add432d4791b9410b3e7a3d6d5df8244185c447e97`  
		Last Modified: Wed, 29 Dec 2021 13:24:39 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b9931dce79731d8fc8f9aae5bb18374967450b16fbcdfd0a2da48dd3efe853`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a5ed1a9ed62c133c6a9b7716fba9971e3f97b64477de601e28cc3ca5b05c8b`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c69ccdace4415c2bdec7795fab2a239ce07eb9906db4b613e2f024a20433a5`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 331.3 KB (331314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b3ee24e2d2850f329b382be9ade011322d08041d68c519d1a03fe3673639af`  
		Last Modified: Wed, 29 Dec 2021 13:24:41 GMT  
		Size: 5.0 MB (4986765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a195460559eca4221d68693a9db0cff883762ae3c2db047097b924a1b368b2`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed2147e829d4d68e6c2022d8fcdaf109525ad0e2b99f88eb2fccf2a746d507c`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfe2741387f6d51946ffb233018a1523759ecf1633a6c8a647410ec3095b16c`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508de22e92ac689a8f2b98d8314afdae274bf00f2d37ab78fbd17452c67a2e26`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:1ba92dc8d94836ff1669b1c5a13754529e799eb1f4455e8598f74e2a5a0758df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d232cd8a1f4e7e8e07cab41c7df5e76a7621d4dab30d1d3010ce1a80d71d0031
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2713981684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72d62160474997048b207a63be5355a15b11e62f414d223416d6920c00e08d2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Sat, 18 Dec 2021 01:40:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 18 Dec 2021 04:32:10 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:32:10 GMT
ENV NATS_SERVER=2.6.6
# Sat, 18 Dec 2021 04:32:11 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Sat, 18 Dec 2021 04:32:12 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Sat, 18 Dec 2021 04:33:08 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Dec 2021 04:34:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Sat, 18 Dec 2021 04:34:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:27 GMT
EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d22d2238b031d3f13bcd6c144e80f8f8402332b8ee8e53cc54b7912c3ac808cb`  
		Last Modified: Sat, 18 Dec 2021 03:59:34 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c5f7f5394b88876960b5ac27980fb2e22584cf50ecde4d9537e88ddbf849c3`  
		Last Modified: Sat, 18 Dec 2021 08:06:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db095798002004c7354bde24c88ee14ba02e430ccfe960c761470e023d0549e`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0362f786811b6ac9b6dbbc36403b1ea4e26ffe73ca7a49ccbb06f1fb9403f315`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ef6c82efd2b3c96cdce7abcace76e1231881bfe847245fbae17e80674ed7bb`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5680cfa178ed5d45ba63a530d80c2b6e96002029544bfa9b2923e63a16f729cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:02 GMT  
		Size: 365.8 KB (365820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9fa2a9d1117be676892e9ced2a72a88583d6b54d4c61de0eb6f92b937b2d9d`  
		Last Modified: Wed, 29 Dec 2021 13:24:05 GMT  
		Size: 5.0 MB (4998116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c2686658f0d823b26ef428ef67cf347e470511ca1675365bbb286131925754`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eb06c9a0a37ab81dde05f4196f65ba87c5cab394a6333a3258f8d737d87571`  
		Last Modified: Wed, 29 Dec 2021 13:23:59 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db8a42caf1046ab762e7e442960441653dbf5854db77c937eb332552d8fc2ac`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b0fad0cdb1e2a3ebb2f7f59a2d5fc2f11486fe57937c012b4e76f26ac7524d`  
		Last Modified: Wed, 29 Dec 2021 13:24:00 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:f684eb2487b5e3aa125e4d0bff1a7b94bde1929252423f1b70fe773365dc1704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4825; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.4825; amd64

```console
$ docker pull nats@sha256:70298f4fa8023d6a4d2a21c616ac79a3cb9cc8fff4e00f83ce618b7d237fb30e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6280045896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed150f48d56334a037ca5957d0291e7226e8088f5051e674f85f38bdf616f32`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 08 Dec 2021 08:38:00 GMT
RUN Install update ltsc2016-amd64
# Sat, 18 Dec 2021 01:55:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 18 Dec 2021 04:34:51 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:52 GMT
ENV NATS_SERVER=2.6.6
# Sat, 18 Dec 2021 04:34:53 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.6/nats-server-v2.6.6-windows-amd64.zip
# Sat, 18 Dec 2021 04:34:53 GMT
ENV NATS_SERVER_SHASUM=9730ea401beed7ac40aeada0a8dccfb70207bb234202035aad5644e93ec657da
# Sat, 18 Dec 2021 04:35:50 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Dec 2021 04:37:24 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Sat, 18 Dec 2021 04:37:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:37:26 GMT
EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:37:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:37:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d026d646213ccf73d9f0584941d108253d62e73df2a74e070776884b7b0242b`  
		Size: 2.2 GB (2204728802 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f6bffd19db3f71ba2031bea25a529c67034869e7e1bbf9e2431d5ee747bd6d6d`  
		Last Modified: Sat, 18 Dec 2021 04:00:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05006360e7d5d5f0fc5160410fd98cfab768e620dca3f3fbc5b44e611e3039b4`  
		Last Modified: Sat, 18 Dec 2021 08:06:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3409aa65b2e0951ea84912add432d4791b9410b3e7a3d6d5df8244185c447e97`  
		Last Modified: Wed, 29 Dec 2021 13:24:39 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b9931dce79731d8fc8f9aae5bb18374967450b16fbcdfd0a2da48dd3efe853`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a5ed1a9ed62c133c6a9b7716fba9971e3f97b64477de601e28cc3ca5b05c8b`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c69ccdace4415c2bdec7795fab2a239ce07eb9906db4b613e2f024a20433a5`  
		Last Modified: Wed, 29 Dec 2021 13:24:38 GMT  
		Size: 331.3 KB (331314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b3ee24e2d2850f329b382be9ade011322d08041d68c519d1a03fe3673639af`  
		Last Modified: Wed, 29 Dec 2021 13:24:41 GMT  
		Size: 5.0 MB (4986765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a195460559eca4221d68693a9db0cff883762ae3c2db047097b924a1b368b2`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed2147e829d4d68e6c2022d8fcdaf109525ad0e2b99f88eb2fccf2a746d507c`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfe2741387f6d51946ffb233018a1523759ecf1633a6c8a647410ec3095b16c`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508de22e92ac689a8f2b98d8314afdae274bf00f2d37ab78fbd17452c67a2e26`  
		Last Modified: Wed, 29 Dec 2021 13:24:36 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
