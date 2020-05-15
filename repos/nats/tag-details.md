<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2.1`](#nats21)
-	[`nats:2.1.7`](#nats217)
-	[`nats:2.1.7-alpine`](#nats217-alpine)
-	[`nats:2.1.7-alpine3.11`](#nats217-alpine311)
-	[`nats:2.1.7-linux`](#nats217-linux)
-	[`nats:2.1.7-nanoserver`](#nats217-nanoserver)
-	[`nats:2.1.7-nanoserver-1809`](#nats217-nanoserver-1809)
-	[`nats:2.1.7-scratch`](#nats217-scratch)
-	[`nats:2.1.7-windowsservercore`](#nats217-windowsservercore)
-	[`nats:2.1.7-windowsservercore-1809`](#nats217-windowsservercore-1809)
-	[`nats:2.1.7-windowsservercore-ltsc2016`](#nats217-windowsservercore-ltsc2016)
-	[`nats:2.1-alpine`](#nats21-alpine)
-	[`nats:2.1-alpine3.11`](#nats21-alpine311)
-	[`nats:2.1-linux`](#nats21-linux)
-	[`nats:2.1-nanoserver`](#nats21-nanoserver)
-	[`nats:2.1-nanoserver-1809`](#nats21-nanoserver-1809)
-	[`nats:2.1-scratch`](#nats21-scratch)
-	[`nats:2.1-windowsservercore`](#nats21-windowsservercore)
-	[`nats:2.1-windowsservercore-1809`](#nats21-windowsservercore-1809)
-	[`nats:2.1-windowsservercore-ltsc2016`](#nats21-windowsservercore-ltsc2016)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.11`](#nats2-alpine311)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2-windowsservercore-ltsc2016`](#nats2-windowsservercore-ltsc2016)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.11`](#natsalpine311)
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
$ docker pull nats@sha256:ea10ff7cb0c8a0289cb21f856ca42ac0c4e7441ce40fb9d79e25504b0f89a72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1217; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:03f7a9538ca823f3e342254f0e0bd62fce56410fd037d70f11e208a64b9be51b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4068777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d7629fb1351a52582452f08d569ef8aa395377751df3706474cb5769e8400d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:b5fc4f9d62c474e25c56f62242c0cbb4f21e732408978c639846820bd9b440a3 in /nats-server 
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9bafc186f2720cd817d9a0dca0d2d85b62db3667b346e18ad3cedee711853463`  
		Last Modified: Wed, 01 Apr 2020 06:49:48 GMT  
		Size: 4.1 MB (4068300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99d87cfb673f46f50d4862e4486d00a26509752daa87beb60702054d53a2f8`  
		Last Modified: Wed, 01 Apr 2020 06:49:47 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:bdda6b6ae6c62c1e78f902992214eca27cf00de2fc7d8d47235a663b3b35940a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7120ba5b06cdd64603f112b86a27c044b9e157fbfc6bdfad548f92351f75bbfe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:07:20 GMT
COPY file:846a74a5cdf1833ec24475ab97e1c375ea237825039dd6ad1d133be2c007faaf in /nats-server 
# Wed, 01 Apr 2020 06:07:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:07:23 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:07:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3779a152c2262214f75fbef66a9ffa608a8a92efab5ce35515692282ae11c664`  
		Last Modified: Wed, 01 Apr 2020 06:08:10 GMT  
		Size: 3.8 MB (3774441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54270160df8d1b1d48a5e855464e3400a606022608035ba66e6914d03dd235f1`  
		Last Modified: Wed, 01 Apr 2020 06:08:08 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:983d25974e771f9316c9e4a5bb71b449518805ddb52e6c7878e171bcccecc945
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105081331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dac43460097cf1c43ccb252c52bbba61b8d41b4a7e413763329d909f5d4f89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 14:50:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:41 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Fri, 15 May 2020 20:15:43 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eafb3f3d63d93b402dfcc428e091787a4242326bc71283a6e3ad40046a60cba0`  
		Last Modified: Wed, 13 May 2020 14:55:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516b6f4ab70976d0f6eefe7345d23e3384290ec3d07e5fd84e86a38a9355f2af`  
		Last Modified: Fri, 15 May 2020 20:20:01 GMT  
		Size: 4.1 MB (4056463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63162a0c7c0aaa22ee2b6ad6d892c8fc4e3d3a0b8ddbf7bd7f2b43b97178540b`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84857e1674bb786ff63ae8a8ddc3a7af87297c5623e8649378c6cd00f404f023`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd47e8ce84e533b8e666ae64628d761d36656664b77077b25b1c1b629f37af6`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ec79ba35428ffa62bae3a80bfa890befff422d5089eed1ec724da29df0ab2`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1`

```console
$ docker pull nats@sha256:ea10ff7cb0c8a0289cb21f856ca42ac0c4e7441ce40fb9d79e25504b0f89a72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1217; amd64

### `nats:2.1` - linux; amd64

```console
$ docker pull nats@sha256:03f7a9538ca823f3e342254f0e0bd62fce56410fd037d70f11e208a64b9be51b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4068777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d7629fb1351a52582452f08d569ef8aa395377751df3706474cb5769e8400d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:b5fc4f9d62c474e25c56f62242c0cbb4f21e732408978c639846820bd9b440a3 in /nats-server 
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9bafc186f2720cd817d9a0dca0d2d85b62db3667b346e18ad3cedee711853463`  
		Last Modified: Wed, 01 Apr 2020 06:49:48 GMT  
		Size: 4.1 MB (4068300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99d87cfb673f46f50d4862e4486d00a26509752daa87beb60702054d53a2f8`  
		Last Modified: Wed, 01 Apr 2020 06:49:47 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm variant v7

```console
$ docker pull nats@sha256:bdda6b6ae6c62c1e78f902992214eca27cf00de2fc7d8d47235a663b3b35940a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7120ba5b06cdd64603f112b86a27c044b9e157fbfc6bdfad548f92351f75bbfe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:07:20 GMT
COPY file:846a74a5cdf1833ec24475ab97e1c375ea237825039dd6ad1d133be2c007faaf in /nats-server 
# Wed, 01 Apr 2020 06:07:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:07:23 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:07:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3779a152c2262214f75fbef66a9ffa608a8a92efab5ce35515692282ae11c664`  
		Last Modified: Wed, 01 Apr 2020 06:08:10 GMT  
		Size: 3.8 MB (3774441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54270160df8d1b1d48a5e855464e3400a606022608035ba66e6914d03dd235f1`  
		Last Modified: Wed, 01 Apr 2020 06:08:08 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:983d25974e771f9316c9e4a5bb71b449518805ddb52e6c7878e171bcccecc945
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105081331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dac43460097cf1c43ccb252c52bbba61b8d41b4a7e413763329d909f5d4f89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 14:50:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:41 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Fri, 15 May 2020 20:15:43 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eafb3f3d63d93b402dfcc428e091787a4242326bc71283a6e3ad40046a60cba0`  
		Last Modified: Wed, 13 May 2020 14:55:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516b6f4ab70976d0f6eefe7345d23e3384290ec3d07e5fd84e86a38a9355f2af`  
		Last Modified: Fri, 15 May 2020 20:20:01 GMT  
		Size: 4.1 MB (4056463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63162a0c7c0aaa22ee2b6ad6d892c8fc4e3d3a0b8ddbf7bd7f2b43b97178540b`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84857e1674bb786ff63ae8a8ddc3a7af87297c5623e8649378c6cd00f404f023`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd47e8ce84e533b8e666ae64628d761d36656664b77077b25b1c1b629f37af6`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ec79ba35428ffa62bae3a80bfa890befff422d5089eed1ec724da29df0ab2`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.7`

```console
$ docker pull nats@sha256:1993e643017b4e04571ec86eecd7e1a717d229d49ab34931642ab96122ec4f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6
	-	windows version 10.0.17763.1217; amd64

### `nats:2.1.7` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.7` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:983d25974e771f9316c9e4a5bb71b449518805ddb52e6c7878e171bcccecc945
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105081331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dac43460097cf1c43ccb252c52bbba61b8d41b4a7e413763329d909f5d4f89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 14:50:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:41 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Fri, 15 May 2020 20:15:43 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eafb3f3d63d93b402dfcc428e091787a4242326bc71283a6e3ad40046a60cba0`  
		Last Modified: Wed, 13 May 2020 14:55:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516b6f4ab70976d0f6eefe7345d23e3384290ec3d07e5fd84e86a38a9355f2af`  
		Last Modified: Fri, 15 May 2020 20:20:01 GMT  
		Size: 4.1 MB (4056463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63162a0c7c0aaa22ee2b6ad6d892c8fc4e3d3a0b8ddbf7bd7f2b43b97178540b`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84857e1674bb786ff63ae8a8ddc3a7af87297c5623e8649378c6cd00f404f023`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd47e8ce84e533b8e666ae64628d761d36656664b77077b25b1c1b629f37af6`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ec79ba35428ffa62bae3a80bfa890befff422d5089eed1ec724da29df0ab2`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.7-alpine`

```console
$ docker pull nats@sha256:abbd79ba7de38c16b28b795cb45d8e081f820deacba48ff3720c814ad53e3611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6

### `nats:2.1.7-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:137e44204c5f787b06b0902fa7370caaec2678981aa81600aed2393409a6de96
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6719649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563e60546d1dbf482ad7632b907a661f4d1b5b4a9dc0105adb89b0545452b743`
-	Default Command: `["nats-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2020 19:50:13 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 19:50:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 15 May 2020 19:50:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 15 May 2020 19:50:27 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:50:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2da3e9f49b6c3ee3b36761ca52b69d8d5eef0937cb74cd8fddbb46850e21eea`  
		Last Modified: Fri, 15 May 2020 19:54:08 GMT  
		Size: 4.1 MB (4099154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf99cc6797b449693d5c09898c063ff989f060f8aec84ee465a356d2a45323c`  
		Last Modified: Fri, 15 May 2020 19:54:06 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.7-alpine3.11`

```console
$ docker pull nats@sha256:abbd79ba7de38c16b28b795cb45d8e081f820deacba48ff3720c814ad53e3611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6

### `nats:2.1.7-alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:137e44204c5f787b06b0902fa7370caaec2678981aa81600aed2393409a6de96
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6719649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563e60546d1dbf482ad7632b907a661f4d1b5b4a9dc0105adb89b0545452b743`
-	Default Command: `["nats-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2020 19:50:13 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 19:50:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 15 May 2020 19:50:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 15 May 2020 19:50:27 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:50:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2da3e9f49b6c3ee3b36761ca52b69d8d5eef0937cb74cd8fddbb46850e21eea`  
		Last Modified: Fri, 15 May 2020 19:54:08 GMT  
		Size: 4.1 MB (4099154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf99cc6797b449693d5c09898c063ff989f060f8aec84ee465a356d2a45323c`  
		Last Modified: Fri, 15 May 2020 19:54:06 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.7-linux`

```console
$ docker pull nats@sha256:0c17ccfb7a4e3db29e21fa25870332520d48481b15f630662e4197e04b681a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6

### `nats:2.1.7-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.7-nanoserver`

```console
$ docker pull nats@sha256:e93c53dfa92b3aa8a99b0b82e1e065c6180489121d90d447fbbe352bb04d4334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `nats:2.1.7-nanoserver` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:983d25974e771f9316c9e4a5bb71b449518805ddb52e6c7878e171bcccecc945
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105081331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dac43460097cf1c43ccb252c52bbba61b8d41b4a7e413763329d909f5d4f89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 14:50:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:41 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Fri, 15 May 2020 20:15:43 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eafb3f3d63d93b402dfcc428e091787a4242326bc71283a6e3ad40046a60cba0`  
		Last Modified: Wed, 13 May 2020 14:55:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516b6f4ab70976d0f6eefe7345d23e3384290ec3d07e5fd84e86a38a9355f2af`  
		Last Modified: Fri, 15 May 2020 20:20:01 GMT  
		Size: 4.1 MB (4056463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63162a0c7c0aaa22ee2b6ad6d892c8fc4e3d3a0b8ddbf7bd7f2b43b97178540b`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84857e1674bb786ff63ae8a8ddc3a7af87297c5623e8649378c6cd00f404f023`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd47e8ce84e533b8e666ae64628d761d36656664b77077b25b1c1b629f37af6`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ec79ba35428ffa62bae3a80bfa890befff422d5089eed1ec724da29df0ab2`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.7-nanoserver-1809`

```console
$ docker pull nats@sha256:e93c53dfa92b3aa8a99b0b82e1e065c6180489121d90d447fbbe352bb04d4334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `nats:2.1.7-nanoserver-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:983d25974e771f9316c9e4a5bb71b449518805ddb52e6c7878e171bcccecc945
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105081331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dac43460097cf1c43ccb252c52bbba61b8d41b4a7e413763329d909f5d4f89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 14:50:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:41 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Fri, 15 May 2020 20:15:43 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eafb3f3d63d93b402dfcc428e091787a4242326bc71283a6e3ad40046a60cba0`  
		Last Modified: Wed, 13 May 2020 14:55:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516b6f4ab70976d0f6eefe7345d23e3384290ec3d07e5fd84e86a38a9355f2af`  
		Last Modified: Fri, 15 May 2020 20:20:01 GMT  
		Size: 4.1 MB (4056463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63162a0c7c0aaa22ee2b6ad6d892c8fc4e3d3a0b8ddbf7bd7f2b43b97178540b`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84857e1674bb786ff63ae8a8ddc3a7af87297c5623e8649378c6cd00f404f023`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd47e8ce84e533b8e666ae64628d761d36656664b77077b25b1c1b629f37af6`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ec79ba35428ffa62bae3a80bfa890befff422d5089eed1ec724da29df0ab2`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.7-scratch`

```console
$ docker pull nats@sha256:0c17ccfb7a4e3db29e21fa25870332520d48481b15f630662e4197e04b681a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v6

### `nats:2.1.7-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.7-windowsservercore`

```console
$ docker pull nats@sha256:79891322cb1d314fc48bc91e5fb81898349861c3689ba759a7ed8c9ffd0f72e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64
	-	windows version 10.0.14393.3686; amd64

### `nats:2.1.7-windowsservercore` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:2e808e4820850550bfe857b7882f9d2ec3770e0a77135137b715ee56f8865a3d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723094192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb5eb9524269197d09f9bfd26b36ba48e1c49a38ab8dd9c549052b31db4308d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 13:04:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:49:24 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:14:14 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:14:35 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:15:25 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:15:26 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:27 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6e220442d94ba050201e82fee90c58b5e714748e7906735032367404c473c91c`  
		Last Modified: Wed, 13 May 2020 14:27:38 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef78e6a0bb5c035fff387c2c5470bd8420babb53d74f1856b9e3ed900cd9af2`  
		Last Modified: Wed, 13 May 2020 14:54:40 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3733fe8392820a6176aabbce2fea6e7f5cef35d18d29c985b3d6d8ca530b040`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ec67b51ba3368bcc10659dea28daabcfc7f499ebfcfd842eb0225d3ef64bc3`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e950aa317a893230e32972c9029d3055b3c97b947e8edd05d14f8a8171bf4b`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 363.9 KB (363883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad60f095cd746e908ba4cbf28bf09d893d3bed31ab282e76a82fda02a2920c6a`  
		Last Modified: Fri, 15 May 2020 20:19:41 GMT  
		Size: 4.4 MB (4387713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213500fe8035d9fbefc9fc80861db0087b3faa36c0cec1fd54f1df89d563f0c5`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bad6f3a4966270bdc5ea21caec6010e5cc8fa9b5702d54af3f80bc4be10fec`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0be37cd8bdefc66402e2d1b8f176c815ab9387935ca74f36fa899efa9604b3`  
		Last Modified: Fri, 15 May 2020 20:19:35 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c352832c962e7536881277d349b432e55dda53ddb36f026e2af6ed3a2e02ed3d`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.7-windowsservercore` - windows version 10.0.14393.3686; amd64

```console
$ docker pull nats@sha256:7d6dc2fc9b5be7820c127bb780394be4df5edd15ead8fe4ee35111825b09fbf0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5751211970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ce5815af4bf55d474ff2df1c879f7f1c76df45820494ee959d5b15a8c06c8c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 13:13:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:51:03 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:53 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:15:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:16:54 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:18:43 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:18:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:18:47 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:18:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:18:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d9ecf24b3b7ef3e61c8b38d40e28e57a80552d6c97884f4cc142af2110ddff`  
		Last Modified: Wed, 13 May 2020 14:28:09 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356fa8d07c48624dd3553b12cafae53b1e6818e2e77c7b4ad7c5e37a6edf5f5`  
		Last Modified: Wed, 13 May 2020 14:55:20 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9053aba643e655abc4300887f89356fa95a058b168b8d3404b5627365ce052a`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39bb0a54403409eeecf7ca0af5b7256923560250ba96cf5c6559ba385ac63ff`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26a263f1c36137f9ae855980e5932549cd9ba1b2d46f835ec4436f85161680`  
		Last Modified: Fri, 15 May 2020 20:20:20 GMT  
		Size: 5.4 MB (5380243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c19479d4b0b4596257e15252e96bb469f2347136f7714e78a0392001039914a`  
		Last Modified: Fri, 15 May 2020 20:20:24 GMT  
		Size: 13.9 MB (13932166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5f6330c66b8c1505013ec5f840e8a1d49e0d2e486d31927832512fba92e373`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c740936073ba5f4006ea263354ff9fa5e0b59bc5b3945a6cbc4f7458531ad83`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f31836cddc824c6c9fbd8264bda5ec6369a6d10eb828e04528c6989a11c7a1`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4187a4d9e22eb583a18d4ff3c1c002ec90c4841754c44cf33db01ad1fe0ec26`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.7-windowsservercore-1809`

```console
$ docker pull nats@sha256:f29246f54ab87c353272363dc66d3c4c048e1509a00978c0948bf7444af6e691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `nats:2.1.7-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:2e808e4820850550bfe857b7882f9d2ec3770e0a77135137b715ee56f8865a3d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723094192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb5eb9524269197d09f9bfd26b36ba48e1c49a38ab8dd9c549052b31db4308d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 13:04:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:49:24 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:14:14 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:14:35 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:15:25 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:15:26 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:27 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6e220442d94ba050201e82fee90c58b5e714748e7906735032367404c473c91c`  
		Last Modified: Wed, 13 May 2020 14:27:38 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef78e6a0bb5c035fff387c2c5470bd8420babb53d74f1856b9e3ed900cd9af2`  
		Last Modified: Wed, 13 May 2020 14:54:40 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3733fe8392820a6176aabbce2fea6e7f5cef35d18d29c985b3d6d8ca530b040`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ec67b51ba3368bcc10659dea28daabcfc7f499ebfcfd842eb0225d3ef64bc3`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e950aa317a893230e32972c9029d3055b3c97b947e8edd05d14f8a8171bf4b`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 363.9 KB (363883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad60f095cd746e908ba4cbf28bf09d893d3bed31ab282e76a82fda02a2920c6a`  
		Last Modified: Fri, 15 May 2020 20:19:41 GMT  
		Size: 4.4 MB (4387713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213500fe8035d9fbefc9fc80861db0087b3faa36c0cec1fd54f1df89d563f0c5`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bad6f3a4966270bdc5ea21caec6010e5cc8fa9b5702d54af3f80bc4be10fec`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0be37cd8bdefc66402e2d1b8f176c815ab9387935ca74f36fa899efa9604b3`  
		Last Modified: Fri, 15 May 2020 20:19:35 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c352832c962e7536881277d349b432e55dda53ddb36f026e2af6ed3a2e02ed3d`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.7-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:2715bb95a8cc376301a71de3e59d4d2563b22a7e4b0b410d3eabc8b9f2d59e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `nats:2.1.7-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull nats@sha256:7d6dc2fc9b5be7820c127bb780394be4df5edd15ead8fe4ee35111825b09fbf0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5751211970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ce5815af4bf55d474ff2df1c879f7f1c76df45820494ee959d5b15a8c06c8c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 13:13:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:51:03 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:53 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:15:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:16:54 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:18:43 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:18:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:18:47 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:18:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:18:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d9ecf24b3b7ef3e61c8b38d40e28e57a80552d6c97884f4cc142af2110ddff`  
		Last Modified: Wed, 13 May 2020 14:28:09 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356fa8d07c48624dd3553b12cafae53b1e6818e2e77c7b4ad7c5e37a6edf5f5`  
		Last Modified: Wed, 13 May 2020 14:55:20 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9053aba643e655abc4300887f89356fa95a058b168b8d3404b5627365ce052a`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39bb0a54403409eeecf7ca0af5b7256923560250ba96cf5c6559ba385ac63ff`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26a263f1c36137f9ae855980e5932549cd9ba1b2d46f835ec4436f85161680`  
		Last Modified: Fri, 15 May 2020 20:20:20 GMT  
		Size: 5.4 MB (5380243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c19479d4b0b4596257e15252e96bb469f2347136f7714e78a0392001039914a`  
		Last Modified: Fri, 15 May 2020 20:20:24 GMT  
		Size: 13.9 MB (13932166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5f6330c66b8c1505013ec5f840e8a1d49e0d2e486d31927832512fba92e373`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c740936073ba5f4006ea263354ff9fa5e0b59bc5b3945a6cbc4f7458531ad83`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f31836cddc824c6c9fbd8264bda5ec6369a6d10eb828e04528c6989a11c7a1`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4187a4d9e22eb583a18d4ff3c1c002ec90c4841754c44cf33db01ad1fe0ec26`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-alpine`

```console
$ docker pull nats@sha256:e5d7a810606b2510df6dfb3c500853c9bbd32c41118b59bc6bd7e26043f42bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1-alpine` - linux; amd64

```console
$ docker pull nats@sha256:b970847a4d2c22f011fa8e238804d5ddca1e5fe149b1ce98b5b89264e94fa14a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5826bdbbffbca20fb421446c8380c24d0fe9eaa58c2d3926b5b69cdfe179afa0`
-	Default Command: `["nats-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:23:38 GMT
ENV NATS_SERVER=2.1.6
# Fri, 24 Apr 2020 19:23:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 24 Apr 2020 19:23:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 24 Apr 2020 19:23:41 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Apr 2020 19:23:41 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483d71d24eb24c812955e03b49a7aefe6addd1e9a27eed62d1063ccacb1daa35`  
		Last Modified: Fri, 24 Apr 2020 19:24:18 GMT  
		Size: 4.4 MB (4371577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28ddeb70b7c98a0c730372dfa9384e654535103ec63fd67de5c666ad1ed10b8`  
		Last Modified: Fri, 24 Apr 2020 19:24:18 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:137e44204c5f787b06b0902fa7370caaec2678981aa81600aed2393409a6de96
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6719649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563e60546d1dbf482ad7632b907a661f4d1b5b4a9dc0105adb89b0545452b743`
-	Default Command: `["nats-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2020 19:50:13 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 19:50:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 15 May 2020 19:50:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 15 May 2020 19:50:27 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:50:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2da3e9f49b6c3ee3b36761ca52b69d8d5eef0937cb74cd8fddbb46850e21eea`  
		Last Modified: Fri, 15 May 2020 19:54:08 GMT  
		Size: 4.1 MB (4099154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf99cc6797b449693d5c09898c063ff989f060f8aec84ee465a356d2a45323c`  
		Last Modified: Fri, 15 May 2020 19:54:06 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:deebc7d7dc1b0429405f75d02ea6b57083cdd895d86b614a651d7623ec14a01e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6499411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f80067dd868fea84d26f61d15ffaa2122d56c7788a50d5cc07243e534c1dff`
-	Default Command: `["nats-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:02:16 GMT
ENV NATS_SERVER=2.1.6
# Fri, 24 Apr 2020 02:02:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 24 Apr 2020 02:02:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 24 Apr 2020 02:02:25 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Apr 2020 02:02:27 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6fe91083b82217baefe1a9f0ed7d83e845198f22641b4d2b3f4b3c309cbac3`  
		Last Modified: Fri, 24 Apr 2020 02:03:03 GMT  
		Size: 4.1 MB (4076790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c4bd5409f67062e55b33a74e24037fc0aed5ad5d8e37095e02415d9ea93b84`  
		Last Modified: Fri, 24 Apr 2020 02:03:03 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-alpine3.11`

```console
$ docker pull nats@sha256:e5d7a810606b2510df6dfb3c500853c9bbd32c41118b59bc6bd7e26043f42bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2.1-alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:b970847a4d2c22f011fa8e238804d5ddca1e5fe149b1ce98b5b89264e94fa14a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5826bdbbffbca20fb421446c8380c24d0fe9eaa58c2d3926b5b69cdfe179afa0`
-	Default Command: `["nats-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:23:38 GMT
ENV NATS_SERVER=2.1.6
# Fri, 24 Apr 2020 19:23:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 24 Apr 2020 19:23:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 24 Apr 2020 19:23:41 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Apr 2020 19:23:41 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483d71d24eb24c812955e03b49a7aefe6addd1e9a27eed62d1063ccacb1daa35`  
		Last Modified: Fri, 24 Apr 2020 19:24:18 GMT  
		Size: 4.4 MB (4371577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28ddeb70b7c98a0c730372dfa9384e654535103ec63fd67de5c666ad1ed10b8`  
		Last Modified: Fri, 24 Apr 2020 19:24:18 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:137e44204c5f787b06b0902fa7370caaec2678981aa81600aed2393409a6de96
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6719649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563e60546d1dbf482ad7632b907a661f4d1b5b4a9dc0105adb89b0545452b743`
-	Default Command: `["nats-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2020 19:50:13 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 19:50:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 15 May 2020 19:50:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 15 May 2020 19:50:27 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:50:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2da3e9f49b6c3ee3b36761ca52b69d8d5eef0937cb74cd8fddbb46850e21eea`  
		Last Modified: Fri, 15 May 2020 19:54:08 GMT  
		Size: 4.1 MB (4099154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf99cc6797b449693d5c09898c063ff989f060f8aec84ee465a356d2a45323c`  
		Last Modified: Fri, 15 May 2020 19:54:06 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:deebc7d7dc1b0429405f75d02ea6b57083cdd895d86b614a651d7623ec14a01e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6499411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f80067dd868fea84d26f61d15ffaa2122d56c7788a50d5cc07243e534c1dff`
-	Default Command: `["nats-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:02:16 GMT
ENV NATS_SERVER=2.1.6
# Fri, 24 Apr 2020 02:02:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 24 Apr 2020 02:02:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 24 Apr 2020 02:02:25 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Apr 2020 02:02:27 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6fe91083b82217baefe1a9f0ed7d83e845198f22641b4d2b3f4b3c309cbac3`  
		Last Modified: Fri, 24 Apr 2020 02:03:03 GMT  
		Size: 4.1 MB (4076790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c4bd5409f67062e55b33a74e24037fc0aed5ad5d8e37095e02415d9ea93b84`  
		Last Modified: Fri, 24 Apr 2020 02:03:03 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-linux`

```console
$ docker pull nats@sha256:22e7a4786a4a893d407d2359fd93e1332d46d2bf051596fec67a8cb1469b10d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-linux` - linux; amd64

```console
$ docker pull nats@sha256:03f7a9538ca823f3e342254f0e0bd62fce56410fd037d70f11e208a64b9be51b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4068777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d7629fb1351a52582452f08d569ef8aa395377751df3706474cb5769e8400d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:b5fc4f9d62c474e25c56f62242c0cbb4f21e732408978c639846820bd9b440a3 in /nats-server 
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9bafc186f2720cd817d9a0dca0d2d85b62db3667b346e18ad3cedee711853463`  
		Last Modified: Wed, 01 Apr 2020 06:49:48 GMT  
		Size: 4.1 MB (4068300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99d87cfb673f46f50d4862e4486d00a26509752daa87beb60702054d53a2f8`  
		Last Modified: Wed, 01 Apr 2020 06:49:47 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bdda6b6ae6c62c1e78f902992214eca27cf00de2fc7d8d47235a663b3b35940a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7120ba5b06cdd64603f112b86a27c044b9e157fbfc6bdfad548f92351f75bbfe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:07:20 GMT
COPY file:846a74a5cdf1833ec24475ab97e1c375ea237825039dd6ad1d133be2c007faaf in /nats-server 
# Wed, 01 Apr 2020 06:07:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:07:23 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:07:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3779a152c2262214f75fbef66a9ffa608a8a92efab5ce35515692282ae11c664`  
		Last Modified: Wed, 01 Apr 2020 06:08:10 GMT  
		Size: 3.8 MB (3774441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54270160df8d1b1d48a5e855464e3400a606022608035ba66e6914d03dd235f1`  
		Last Modified: Wed, 01 Apr 2020 06:08:08 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-nanoserver`

```console
$ docker pull nats@sha256:e93c53dfa92b3aa8a99b0b82e1e065c6180489121d90d447fbbe352bb04d4334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `nats:2.1-nanoserver` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:983d25974e771f9316c9e4a5bb71b449518805ddb52e6c7878e171bcccecc945
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105081331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dac43460097cf1c43ccb252c52bbba61b8d41b4a7e413763329d909f5d4f89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 14:50:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:41 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Fri, 15 May 2020 20:15:43 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eafb3f3d63d93b402dfcc428e091787a4242326bc71283a6e3ad40046a60cba0`  
		Last Modified: Wed, 13 May 2020 14:55:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516b6f4ab70976d0f6eefe7345d23e3384290ec3d07e5fd84e86a38a9355f2af`  
		Last Modified: Fri, 15 May 2020 20:20:01 GMT  
		Size: 4.1 MB (4056463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63162a0c7c0aaa22ee2b6ad6d892c8fc4e3d3a0b8ddbf7bd7f2b43b97178540b`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84857e1674bb786ff63ae8a8ddc3a7af87297c5623e8649378c6cd00f404f023`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd47e8ce84e533b8e666ae64628d761d36656664b77077b25b1c1b629f37af6`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ec79ba35428ffa62bae3a80bfa890befff422d5089eed1ec724da29df0ab2`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-nanoserver-1809`

```console
$ docker pull nats@sha256:e93c53dfa92b3aa8a99b0b82e1e065c6180489121d90d447fbbe352bb04d4334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `nats:2.1-nanoserver-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:983d25974e771f9316c9e4a5bb71b449518805ddb52e6c7878e171bcccecc945
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105081331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dac43460097cf1c43ccb252c52bbba61b8d41b4a7e413763329d909f5d4f89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 14:50:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:41 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Fri, 15 May 2020 20:15:43 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eafb3f3d63d93b402dfcc428e091787a4242326bc71283a6e3ad40046a60cba0`  
		Last Modified: Wed, 13 May 2020 14:55:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516b6f4ab70976d0f6eefe7345d23e3384290ec3d07e5fd84e86a38a9355f2af`  
		Last Modified: Fri, 15 May 2020 20:20:01 GMT  
		Size: 4.1 MB (4056463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63162a0c7c0aaa22ee2b6ad6d892c8fc4e3d3a0b8ddbf7bd7f2b43b97178540b`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84857e1674bb786ff63ae8a8ddc3a7af87297c5623e8649378c6cd00f404f023`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd47e8ce84e533b8e666ae64628d761d36656664b77077b25b1c1b629f37af6`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ec79ba35428ffa62bae3a80bfa890befff422d5089eed1ec724da29df0ab2`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-scratch`

```console
$ docker pull nats@sha256:22e7a4786a4a893d407d2359fd93e1332d46d2bf051596fec67a8cb1469b10d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-scratch` - linux; amd64

```console
$ docker pull nats@sha256:03f7a9538ca823f3e342254f0e0bd62fce56410fd037d70f11e208a64b9be51b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4068777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d7629fb1351a52582452f08d569ef8aa395377751df3706474cb5769e8400d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:b5fc4f9d62c474e25c56f62242c0cbb4f21e732408978c639846820bd9b440a3 in /nats-server 
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9bafc186f2720cd817d9a0dca0d2d85b62db3667b346e18ad3cedee711853463`  
		Last Modified: Wed, 01 Apr 2020 06:49:48 GMT  
		Size: 4.1 MB (4068300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99d87cfb673f46f50d4862e4486d00a26509752daa87beb60702054d53a2f8`  
		Last Modified: Wed, 01 Apr 2020 06:49:47 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bdda6b6ae6c62c1e78f902992214eca27cf00de2fc7d8d47235a663b3b35940a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7120ba5b06cdd64603f112b86a27c044b9e157fbfc6bdfad548f92351f75bbfe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:07:20 GMT
COPY file:846a74a5cdf1833ec24475ab97e1c375ea237825039dd6ad1d133be2c007faaf in /nats-server 
# Wed, 01 Apr 2020 06:07:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:07:23 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:07:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3779a152c2262214f75fbef66a9ffa608a8a92efab5ce35515692282ae11c664`  
		Last Modified: Wed, 01 Apr 2020 06:08:10 GMT  
		Size: 3.8 MB (3774441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54270160df8d1b1d48a5e855464e3400a606022608035ba66e6914d03dd235f1`  
		Last Modified: Wed, 01 Apr 2020 06:08:08 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore`

```console
$ docker pull nats@sha256:79891322cb1d314fc48bc91e5fb81898349861c3689ba759a7ed8c9ffd0f72e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64
	-	windows version 10.0.14393.3686; amd64

### `nats:2.1-windowsservercore` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:2e808e4820850550bfe857b7882f9d2ec3770e0a77135137b715ee56f8865a3d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723094192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb5eb9524269197d09f9bfd26b36ba48e1c49a38ab8dd9c549052b31db4308d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 13:04:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:49:24 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:14:14 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:14:35 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:15:25 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:15:26 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:27 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6e220442d94ba050201e82fee90c58b5e714748e7906735032367404c473c91c`  
		Last Modified: Wed, 13 May 2020 14:27:38 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef78e6a0bb5c035fff387c2c5470bd8420babb53d74f1856b9e3ed900cd9af2`  
		Last Modified: Wed, 13 May 2020 14:54:40 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3733fe8392820a6176aabbce2fea6e7f5cef35d18d29c985b3d6d8ca530b040`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ec67b51ba3368bcc10659dea28daabcfc7f499ebfcfd842eb0225d3ef64bc3`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e950aa317a893230e32972c9029d3055b3c97b947e8edd05d14f8a8171bf4b`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 363.9 KB (363883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad60f095cd746e908ba4cbf28bf09d893d3bed31ab282e76a82fda02a2920c6a`  
		Last Modified: Fri, 15 May 2020 20:19:41 GMT  
		Size: 4.4 MB (4387713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213500fe8035d9fbefc9fc80861db0087b3faa36c0cec1fd54f1df89d563f0c5`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bad6f3a4966270bdc5ea21caec6010e5cc8fa9b5702d54af3f80bc4be10fec`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0be37cd8bdefc66402e2d1b8f176c815ab9387935ca74f36fa899efa9604b3`  
		Last Modified: Fri, 15 May 2020 20:19:35 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c352832c962e7536881277d349b432e55dda53ddb36f026e2af6ed3a2e02ed3d`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-windowsservercore` - windows version 10.0.14393.3686; amd64

```console
$ docker pull nats@sha256:7d6dc2fc9b5be7820c127bb780394be4df5edd15ead8fe4ee35111825b09fbf0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5751211970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ce5815af4bf55d474ff2df1c879f7f1c76df45820494ee959d5b15a8c06c8c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 13:13:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:51:03 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:53 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:15:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:16:54 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:18:43 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:18:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:18:47 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:18:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:18:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d9ecf24b3b7ef3e61c8b38d40e28e57a80552d6c97884f4cc142af2110ddff`  
		Last Modified: Wed, 13 May 2020 14:28:09 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356fa8d07c48624dd3553b12cafae53b1e6818e2e77c7b4ad7c5e37a6edf5f5`  
		Last Modified: Wed, 13 May 2020 14:55:20 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9053aba643e655abc4300887f89356fa95a058b168b8d3404b5627365ce052a`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39bb0a54403409eeecf7ca0af5b7256923560250ba96cf5c6559ba385ac63ff`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26a263f1c36137f9ae855980e5932549cd9ba1b2d46f835ec4436f85161680`  
		Last Modified: Fri, 15 May 2020 20:20:20 GMT  
		Size: 5.4 MB (5380243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c19479d4b0b4596257e15252e96bb469f2347136f7714e78a0392001039914a`  
		Last Modified: Fri, 15 May 2020 20:20:24 GMT  
		Size: 13.9 MB (13932166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5f6330c66b8c1505013ec5f840e8a1d49e0d2e486d31927832512fba92e373`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c740936073ba5f4006ea263354ff9fa5e0b59bc5b3945a6cbc4f7458531ad83`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f31836cddc824c6c9fbd8264bda5ec6369a6d10eb828e04528c6989a11c7a1`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4187a4d9e22eb583a18d4ff3c1c002ec90c4841754c44cf33db01ad1fe0ec26`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-1809`

```console
$ docker pull nats@sha256:f29246f54ab87c353272363dc66d3c4c048e1509a00978c0948bf7444af6e691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `nats:2.1-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:2e808e4820850550bfe857b7882f9d2ec3770e0a77135137b715ee56f8865a3d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723094192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb5eb9524269197d09f9bfd26b36ba48e1c49a38ab8dd9c549052b31db4308d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 13:04:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:49:24 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:14:14 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:14:35 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:15:25 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:15:26 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:27 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6e220442d94ba050201e82fee90c58b5e714748e7906735032367404c473c91c`  
		Last Modified: Wed, 13 May 2020 14:27:38 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef78e6a0bb5c035fff387c2c5470bd8420babb53d74f1856b9e3ed900cd9af2`  
		Last Modified: Wed, 13 May 2020 14:54:40 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3733fe8392820a6176aabbce2fea6e7f5cef35d18d29c985b3d6d8ca530b040`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ec67b51ba3368bcc10659dea28daabcfc7f499ebfcfd842eb0225d3ef64bc3`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e950aa317a893230e32972c9029d3055b3c97b947e8edd05d14f8a8171bf4b`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 363.9 KB (363883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad60f095cd746e908ba4cbf28bf09d893d3bed31ab282e76a82fda02a2920c6a`  
		Last Modified: Fri, 15 May 2020 20:19:41 GMT  
		Size: 4.4 MB (4387713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213500fe8035d9fbefc9fc80861db0087b3faa36c0cec1fd54f1df89d563f0c5`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bad6f3a4966270bdc5ea21caec6010e5cc8fa9b5702d54af3f80bc4be10fec`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0be37cd8bdefc66402e2d1b8f176c815ab9387935ca74f36fa899efa9604b3`  
		Last Modified: Fri, 15 May 2020 20:19:35 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c352832c962e7536881277d349b432e55dda53ddb36f026e2af6ed3a2e02ed3d`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:2715bb95a8cc376301a71de3e59d4d2563b22a7e4b0b410d3eabc8b9f2d59e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `nats:2.1-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull nats@sha256:7d6dc2fc9b5be7820c127bb780394be4df5edd15ead8fe4ee35111825b09fbf0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5751211970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ce5815af4bf55d474ff2df1c879f7f1c76df45820494ee959d5b15a8c06c8c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 13:13:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:51:03 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:53 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:15:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:16:54 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:18:43 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:18:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:18:47 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:18:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:18:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d9ecf24b3b7ef3e61c8b38d40e28e57a80552d6c97884f4cc142af2110ddff`  
		Last Modified: Wed, 13 May 2020 14:28:09 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356fa8d07c48624dd3553b12cafae53b1e6818e2e77c7b4ad7c5e37a6edf5f5`  
		Last Modified: Wed, 13 May 2020 14:55:20 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9053aba643e655abc4300887f89356fa95a058b168b8d3404b5627365ce052a`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39bb0a54403409eeecf7ca0af5b7256923560250ba96cf5c6559ba385ac63ff`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26a263f1c36137f9ae855980e5932549cd9ba1b2d46f835ec4436f85161680`  
		Last Modified: Fri, 15 May 2020 20:20:20 GMT  
		Size: 5.4 MB (5380243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c19479d4b0b4596257e15252e96bb469f2347136f7714e78a0392001039914a`  
		Last Modified: Fri, 15 May 2020 20:20:24 GMT  
		Size: 13.9 MB (13932166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5f6330c66b8c1505013ec5f840e8a1d49e0d2e486d31927832512fba92e373`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c740936073ba5f4006ea263354ff9fa5e0b59bc5b3945a6cbc4f7458531ad83`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f31836cddc824c6c9fbd8264bda5ec6369a6d10eb828e04528c6989a11c7a1`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4187a4d9e22eb583a18d4ff3c1c002ec90c4841754c44cf33db01ad1fe0ec26`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:e5d7a810606b2510df6dfb3c500853c9bbd32c41118b59bc6bd7e26043f42bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:b970847a4d2c22f011fa8e238804d5ddca1e5fe149b1ce98b5b89264e94fa14a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5826bdbbffbca20fb421446c8380c24d0fe9eaa58c2d3926b5b69cdfe179afa0`
-	Default Command: `["nats-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:23:38 GMT
ENV NATS_SERVER=2.1.6
# Fri, 24 Apr 2020 19:23:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 24 Apr 2020 19:23:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 24 Apr 2020 19:23:41 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Apr 2020 19:23:41 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483d71d24eb24c812955e03b49a7aefe6addd1e9a27eed62d1063ccacb1daa35`  
		Last Modified: Fri, 24 Apr 2020 19:24:18 GMT  
		Size: 4.4 MB (4371577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28ddeb70b7c98a0c730372dfa9384e654535103ec63fd67de5c666ad1ed10b8`  
		Last Modified: Fri, 24 Apr 2020 19:24:18 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:137e44204c5f787b06b0902fa7370caaec2678981aa81600aed2393409a6de96
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6719649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563e60546d1dbf482ad7632b907a661f4d1b5b4a9dc0105adb89b0545452b743`
-	Default Command: `["nats-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2020 19:50:13 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 19:50:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 15 May 2020 19:50:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 15 May 2020 19:50:27 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:50:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2da3e9f49b6c3ee3b36761ca52b69d8d5eef0937cb74cd8fddbb46850e21eea`  
		Last Modified: Fri, 15 May 2020 19:54:08 GMT  
		Size: 4.1 MB (4099154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf99cc6797b449693d5c09898c063ff989f060f8aec84ee465a356d2a45323c`  
		Last Modified: Fri, 15 May 2020 19:54:06 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:deebc7d7dc1b0429405f75d02ea6b57083cdd895d86b614a651d7623ec14a01e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6499411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f80067dd868fea84d26f61d15ffaa2122d56c7788a50d5cc07243e534c1dff`
-	Default Command: `["nats-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:02:16 GMT
ENV NATS_SERVER=2.1.6
# Fri, 24 Apr 2020 02:02:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 24 Apr 2020 02:02:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 24 Apr 2020 02:02:25 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Apr 2020 02:02:27 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6fe91083b82217baefe1a9f0ed7d83e845198f22641b4d2b3f4b3c309cbac3`  
		Last Modified: Fri, 24 Apr 2020 02:03:03 GMT  
		Size: 4.1 MB (4076790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c4bd5409f67062e55b33a74e24037fc0aed5ad5d8e37095e02415d9ea93b84`  
		Last Modified: Fri, 24 Apr 2020 02:03:03 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.11`

```console
$ docker pull nats@sha256:e5d7a810606b2510df6dfb3c500853c9bbd32c41118b59bc6bd7e26043f42bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:2-alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:b970847a4d2c22f011fa8e238804d5ddca1e5fe149b1ce98b5b89264e94fa14a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5826bdbbffbca20fb421446c8380c24d0fe9eaa58c2d3926b5b69cdfe179afa0`
-	Default Command: `["nats-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:23:38 GMT
ENV NATS_SERVER=2.1.6
# Fri, 24 Apr 2020 19:23:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 24 Apr 2020 19:23:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 24 Apr 2020 19:23:41 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Apr 2020 19:23:41 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483d71d24eb24c812955e03b49a7aefe6addd1e9a27eed62d1063ccacb1daa35`  
		Last Modified: Fri, 24 Apr 2020 19:24:18 GMT  
		Size: 4.4 MB (4371577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28ddeb70b7c98a0c730372dfa9384e654535103ec63fd67de5c666ad1ed10b8`  
		Last Modified: Fri, 24 Apr 2020 19:24:18 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:137e44204c5f787b06b0902fa7370caaec2678981aa81600aed2393409a6de96
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6719649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563e60546d1dbf482ad7632b907a661f4d1b5b4a9dc0105adb89b0545452b743`
-	Default Command: `["nats-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2020 19:50:13 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 19:50:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 15 May 2020 19:50:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 15 May 2020 19:50:27 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:50:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2da3e9f49b6c3ee3b36761ca52b69d8d5eef0937cb74cd8fddbb46850e21eea`  
		Last Modified: Fri, 15 May 2020 19:54:08 GMT  
		Size: 4.1 MB (4099154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf99cc6797b449693d5c09898c063ff989f060f8aec84ee465a356d2a45323c`  
		Last Modified: Fri, 15 May 2020 19:54:06 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:deebc7d7dc1b0429405f75d02ea6b57083cdd895d86b614a651d7623ec14a01e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6499411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f80067dd868fea84d26f61d15ffaa2122d56c7788a50d5cc07243e534c1dff`
-	Default Command: `["nats-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:02:16 GMT
ENV NATS_SERVER=2.1.6
# Fri, 24 Apr 2020 02:02:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 24 Apr 2020 02:02:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 24 Apr 2020 02:02:25 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Apr 2020 02:02:27 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6fe91083b82217baefe1a9f0ed7d83e845198f22641b4d2b3f4b3c309cbac3`  
		Last Modified: Fri, 24 Apr 2020 02:03:03 GMT  
		Size: 4.1 MB (4076790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c4bd5409f67062e55b33a74e24037fc0aed5ad5d8e37095e02415d9ea93b84`  
		Last Modified: Fri, 24 Apr 2020 02:03:03 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:22e7a4786a4a893d407d2359fd93e1332d46d2bf051596fec67a8cb1469b10d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:03f7a9538ca823f3e342254f0e0bd62fce56410fd037d70f11e208a64b9be51b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4068777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d7629fb1351a52582452f08d569ef8aa395377751df3706474cb5769e8400d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:b5fc4f9d62c474e25c56f62242c0cbb4f21e732408978c639846820bd9b440a3 in /nats-server 
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9bafc186f2720cd817d9a0dca0d2d85b62db3667b346e18ad3cedee711853463`  
		Last Modified: Wed, 01 Apr 2020 06:49:48 GMT  
		Size: 4.1 MB (4068300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99d87cfb673f46f50d4862e4486d00a26509752daa87beb60702054d53a2f8`  
		Last Modified: Wed, 01 Apr 2020 06:49:47 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bdda6b6ae6c62c1e78f902992214eca27cf00de2fc7d8d47235a663b3b35940a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7120ba5b06cdd64603f112b86a27c044b9e157fbfc6bdfad548f92351f75bbfe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:07:20 GMT
COPY file:846a74a5cdf1833ec24475ab97e1c375ea237825039dd6ad1d133be2c007faaf in /nats-server 
# Wed, 01 Apr 2020 06:07:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:07:23 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:07:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3779a152c2262214f75fbef66a9ffa608a8a92efab5ce35515692282ae11c664`  
		Last Modified: Wed, 01 Apr 2020 06:08:10 GMT  
		Size: 3.8 MB (3774441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54270160df8d1b1d48a5e855464e3400a606022608035ba66e6914d03dd235f1`  
		Last Modified: Wed, 01 Apr 2020 06:08:08 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:e93c53dfa92b3aa8a99b0b82e1e065c6180489121d90d447fbbe352bb04d4334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:983d25974e771f9316c9e4a5bb71b449518805ddb52e6c7878e171bcccecc945
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105081331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dac43460097cf1c43ccb252c52bbba61b8d41b4a7e413763329d909f5d4f89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 14:50:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:41 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Fri, 15 May 2020 20:15:43 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eafb3f3d63d93b402dfcc428e091787a4242326bc71283a6e3ad40046a60cba0`  
		Last Modified: Wed, 13 May 2020 14:55:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516b6f4ab70976d0f6eefe7345d23e3384290ec3d07e5fd84e86a38a9355f2af`  
		Last Modified: Fri, 15 May 2020 20:20:01 GMT  
		Size: 4.1 MB (4056463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63162a0c7c0aaa22ee2b6ad6d892c8fc4e3d3a0b8ddbf7bd7f2b43b97178540b`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84857e1674bb786ff63ae8a8ddc3a7af87297c5623e8649378c6cd00f404f023`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd47e8ce84e533b8e666ae64628d761d36656664b77077b25b1c1b629f37af6`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ec79ba35428ffa62bae3a80bfa890befff422d5089eed1ec724da29df0ab2`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:e93c53dfa92b3aa8a99b0b82e1e065c6180489121d90d447fbbe352bb04d4334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:983d25974e771f9316c9e4a5bb71b449518805ddb52e6c7878e171bcccecc945
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105081331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dac43460097cf1c43ccb252c52bbba61b8d41b4a7e413763329d909f5d4f89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 14:50:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:41 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Fri, 15 May 2020 20:15:43 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eafb3f3d63d93b402dfcc428e091787a4242326bc71283a6e3ad40046a60cba0`  
		Last Modified: Wed, 13 May 2020 14:55:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516b6f4ab70976d0f6eefe7345d23e3384290ec3d07e5fd84e86a38a9355f2af`  
		Last Modified: Fri, 15 May 2020 20:20:01 GMT  
		Size: 4.1 MB (4056463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63162a0c7c0aaa22ee2b6ad6d892c8fc4e3d3a0b8ddbf7bd7f2b43b97178540b`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84857e1674bb786ff63ae8a8ddc3a7af87297c5623e8649378c6cd00f404f023`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd47e8ce84e533b8e666ae64628d761d36656664b77077b25b1c1b629f37af6`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ec79ba35428ffa62bae3a80bfa890befff422d5089eed1ec724da29df0ab2`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:22e7a4786a4a893d407d2359fd93e1332d46d2bf051596fec67a8cb1469b10d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:03f7a9538ca823f3e342254f0e0bd62fce56410fd037d70f11e208a64b9be51b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4068777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d7629fb1351a52582452f08d569ef8aa395377751df3706474cb5769e8400d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:b5fc4f9d62c474e25c56f62242c0cbb4f21e732408978c639846820bd9b440a3 in /nats-server 
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9bafc186f2720cd817d9a0dca0d2d85b62db3667b346e18ad3cedee711853463`  
		Last Modified: Wed, 01 Apr 2020 06:49:48 GMT  
		Size: 4.1 MB (4068300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99d87cfb673f46f50d4862e4486d00a26509752daa87beb60702054d53a2f8`  
		Last Modified: Wed, 01 Apr 2020 06:49:47 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bdda6b6ae6c62c1e78f902992214eca27cf00de2fc7d8d47235a663b3b35940a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7120ba5b06cdd64603f112b86a27c044b9e157fbfc6bdfad548f92351f75bbfe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:07:20 GMT
COPY file:846a74a5cdf1833ec24475ab97e1c375ea237825039dd6ad1d133be2c007faaf in /nats-server 
# Wed, 01 Apr 2020 06:07:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:07:23 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:07:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3779a152c2262214f75fbef66a9ffa608a8a92efab5ce35515692282ae11c664`  
		Last Modified: Wed, 01 Apr 2020 06:08:10 GMT  
		Size: 3.8 MB (3774441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54270160df8d1b1d48a5e855464e3400a606022608035ba66e6914d03dd235f1`  
		Last Modified: Wed, 01 Apr 2020 06:08:08 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:79891322cb1d314fc48bc91e5fb81898349861c3689ba759a7ed8c9ffd0f72e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64
	-	windows version 10.0.14393.3686; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:2e808e4820850550bfe857b7882f9d2ec3770e0a77135137b715ee56f8865a3d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723094192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb5eb9524269197d09f9bfd26b36ba48e1c49a38ab8dd9c549052b31db4308d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 13:04:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:49:24 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:14:14 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:14:35 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:15:25 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:15:26 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:27 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6e220442d94ba050201e82fee90c58b5e714748e7906735032367404c473c91c`  
		Last Modified: Wed, 13 May 2020 14:27:38 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef78e6a0bb5c035fff387c2c5470bd8420babb53d74f1856b9e3ed900cd9af2`  
		Last Modified: Wed, 13 May 2020 14:54:40 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3733fe8392820a6176aabbce2fea6e7f5cef35d18d29c985b3d6d8ca530b040`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ec67b51ba3368bcc10659dea28daabcfc7f499ebfcfd842eb0225d3ef64bc3`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e950aa317a893230e32972c9029d3055b3c97b947e8edd05d14f8a8171bf4b`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 363.9 KB (363883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad60f095cd746e908ba4cbf28bf09d893d3bed31ab282e76a82fda02a2920c6a`  
		Last Modified: Fri, 15 May 2020 20:19:41 GMT  
		Size: 4.4 MB (4387713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213500fe8035d9fbefc9fc80861db0087b3faa36c0cec1fd54f1df89d563f0c5`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bad6f3a4966270bdc5ea21caec6010e5cc8fa9b5702d54af3f80bc4be10fec`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0be37cd8bdefc66402e2d1b8f176c815ab9387935ca74f36fa899efa9604b3`  
		Last Modified: Fri, 15 May 2020 20:19:35 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c352832c962e7536881277d349b432e55dda53ddb36f026e2af6ed3a2e02ed3d`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.3686; amd64

```console
$ docker pull nats@sha256:7d6dc2fc9b5be7820c127bb780394be4df5edd15ead8fe4ee35111825b09fbf0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5751211970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ce5815af4bf55d474ff2df1c879f7f1c76df45820494ee959d5b15a8c06c8c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 13:13:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:51:03 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:53 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:15:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:16:54 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:18:43 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:18:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:18:47 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:18:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:18:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d9ecf24b3b7ef3e61c8b38d40e28e57a80552d6c97884f4cc142af2110ddff`  
		Last Modified: Wed, 13 May 2020 14:28:09 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356fa8d07c48624dd3553b12cafae53b1e6818e2e77c7b4ad7c5e37a6edf5f5`  
		Last Modified: Wed, 13 May 2020 14:55:20 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9053aba643e655abc4300887f89356fa95a058b168b8d3404b5627365ce052a`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39bb0a54403409eeecf7ca0af5b7256923560250ba96cf5c6559ba385ac63ff`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26a263f1c36137f9ae855980e5932549cd9ba1b2d46f835ec4436f85161680`  
		Last Modified: Fri, 15 May 2020 20:20:20 GMT  
		Size: 5.4 MB (5380243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c19479d4b0b4596257e15252e96bb469f2347136f7714e78a0392001039914a`  
		Last Modified: Fri, 15 May 2020 20:20:24 GMT  
		Size: 13.9 MB (13932166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5f6330c66b8c1505013ec5f840e8a1d49e0d2e486d31927832512fba92e373`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c740936073ba5f4006ea263354ff9fa5e0b59bc5b3945a6cbc4f7458531ad83`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f31836cddc824c6c9fbd8264bda5ec6369a6d10eb828e04528c6989a11c7a1`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4187a4d9e22eb583a18d4ff3c1c002ec90c4841754c44cf33db01ad1fe0ec26`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:f29246f54ab87c353272363dc66d3c4c048e1509a00978c0948bf7444af6e691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:2e808e4820850550bfe857b7882f9d2ec3770e0a77135137b715ee56f8865a3d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723094192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb5eb9524269197d09f9bfd26b36ba48e1c49a38ab8dd9c549052b31db4308d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 13:04:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:49:24 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:14:14 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:14:35 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:15:25 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:15:26 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:27 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6e220442d94ba050201e82fee90c58b5e714748e7906735032367404c473c91c`  
		Last Modified: Wed, 13 May 2020 14:27:38 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef78e6a0bb5c035fff387c2c5470bd8420babb53d74f1856b9e3ed900cd9af2`  
		Last Modified: Wed, 13 May 2020 14:54:40 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3733fe8392820a6176aabbce2fea6e7f5cef35d18d29c985b3d6d8ca530b040`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ec67b51ba3368bcc10659dea28daabcfc7f499ebfcfd842eb0225d3ef64bc3`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e950aa317a893230e32972c9029d3055b3c97b947e8edd05d14f8a8171bf4b`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 363.9 KB (363883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad60f095cd746e908ba4cbf28bf09d893d3bed31ab282e76a82fda02a2920c6a`  
		Last Modified: Fri, 15 May 2020 20:19:41 GMT  
		Size: 4.4 MB (4387713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213500fe8035d9fbefc9fc80861db0087b3faa36c0cec1fd54f1df89d563f0c5`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bad6f3a4966270bdc5ea21caec6010e5cc8fa9b5702d54af3f80bc4be10fec`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0be37cd8bdefc66402e2d1b8f176c815ab9387935ca74f36fa899efa9604b3`  
		Last Modified: Fri, 15 May 2020 20:19:35 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c352832c962e7536881277d349b432e55dda53ddb36f026e2af6ed3a2e02ed3d`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:2715bb95a8cc376301a71de3e59d4d2563b22a7e4b0b410d3eabc8b9f2d59e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull nats@sha256:7d6dc2fc9b5be7820c127bb780394be4df5edd15ead8fe4ee35111825b09fbf0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5751211970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ce5815af4bf55d474ff2df1c879f7f1c76df45820494ee959d5b15a8c06c8c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 13:13:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:51:03 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:53 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:15:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:16:54 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:18:43 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:18:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:18:47 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:18:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:18:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d9ecf24b3b7ef3e61c8b38d40e28e57a80552d6c97884f4cc142af2110ddff`  
		Last Modified: Wed, 13 May 2020 14:28:09 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356fa8d07c48624dd3553b12cafae53b1e6818e2e77c7b4ad7c5e37a6edf5f5`  
		Last Modified: Wed, 13 May 2020 14:55:20 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9053aba643e655abc4300887f89356fa95a058b168b8d3404b5627365ce052a`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39bb0a54403409eeecf7ca0af5b7256923560250ba96cf5c6559ba385ac63ff`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26a263f1c36137f9ae855980e5932549cd9ba1b2d46f835ec4436f85161680`  
		Last Modified: Fri, 15 May 2020 20:20:20 GMT  
		Size: 5.4 MB (5380243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c19479d4b0b4596257e15252e96bb469f2347136f7714e78a0392001039914a`  
		Last Modified: Fri, 15 May 2020 20:20:24 GMT  
		Size: 13.9 MB (13932166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5f6330c66b8c1505013ec5f840e8a1d49e0d2e486d31927832512fba92e373`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c740936073ba5f4006ea263354ff9fa5e0b59bc5b3945a6cbc4f7458531ad83`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f31836cddc824c6c9fbd8264bda5ec6369a6d10eb828e04528c6989a11c7a1`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4187a4d9e22eb583a18d4ff3c1c002ec90c4841754c44cf33db01ad1fe0ec26`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:e5d7a810606b2510df6dfb3c500853c9bbd32c41118b59bc6bd7e26043f42bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:b970847a4d2c22f011fa8e238804d5ddca1e5fe149b1ce98b5b89264e94fa14a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5826bdbbffbca20fb421446c8380c24d0fe9eaa58c2d3926b5b69cdfe179afa0`
-	Default Command: `["nats-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:23:38 GMT
ENV NATS_SERVER=2.1.6
# Fri, 24 Apr 2020 19:23:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 24 Apr 2020 19:23:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 24 Apr 2020 19:23:41 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Apr 2020 19:23:41 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483d71d24eb24c812955e03b49a7aefe6addd1e9a27eed62d1063ccacb1daa35`  
		Last Modified: Fri, 24 Apr 2020 19:24:18 GMT  
		Size: 4.4 MB (4371577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28ddeb70b7c98a0c730372dfa9384e654535103ec63fd67de5c666ad1ed10b8`  
		Last Modified: Fri, 24 Apr 2020 19:24:18 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:137e44204c5f787b06b0902fa7370caaec2678981aa81600aed2393409a6de96
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6719649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563e60546d1dbf482ad7632b907a661f4d1b5b4a9dc0105adb89b0545452b743`
-	Default Command: `["nats-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2020 19:50:13 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 19:50:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 15 May 2020 19:50:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 15 May 2020 19:50:27 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:50:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2da3e9f49b6c3ee3b36761ca52b69d8d5eef0937cb74cd8fddbb46850e21eea`  
		Last Modified: Fri, 15 May 2020 19:54:08 GMT  
		Size: 4.1 MB (4099154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf99cc6797b449693d5c09898c063ff989f060f8aec84ee465a356d2a45323c`  
		Last Modified: Fri, 15 May 2020 19:54:06 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:deebc7d7dc1b0429405f75d02ea6b57083cdd895d86b614a651d7623ec14a01e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6499411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f80067dd868fea84d26f61d15ffaa2122d56c7788a50d5cc07243e534c1dff`
-	Default Command: `["nats-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:02:16 GMT
ENV NATS_SERVER=2.1.6
# Fri, 24 Apr 2020 02:02:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 24 Apr 2020 02:02:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 24 Apr 2020 02:02:25 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Apr 2020 02:02:27 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6fe91083b82217baefe1a9f0ed7d83e845198f22641b4d2b3f4b3c309cbac3`  
		Last Modified: Fri, 24 Apr 2020 02:03:03 GMT  
		Size: 4.1 MB (4076790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c4bd5409f67062e55b33a74e24037fc0aed5ad5d8e37095e02415d9ea93b84`  
		Last Modified: Fri, 24 Apr 2020 02:03:03 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.11`

```console
$ docker pull nats@sha256:e5d7a810606b2510df6dfb3c500853c9bbd32c41118b59bc6bd7e26043f42bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7

### `nats:alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:b970847a4d2c22f011fa8e238804d5ddca1e5fe149b1ce98b5b89264e94fa14a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5826bdbbffbca20fb421446c8380c24d0fe9eaa58c2d3926b5b69cdfe179afa0`
-	Default Command: `["nats-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:23:38 GMT
ENV NATS_SERVER=2.1.6
# Fri, 24 Apr 2020 19:23:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 24 Apr 2020 19:23:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 24 Apr 2020 19:23:41 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Apr 2020 19:23:41 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483d71d24eb24c812955e03b49a7aefe6addd1e9a27eed62d1063ccacb1daa35`  
		Last Modified: Fri, 24 Apr 2020 19:24:18 GMT  
		Size: 4.4 MB (4371577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28ddeb70b7c98a0c730372dfa9384e654535103ec63fd67de5c666ad1ed10b8`  
		Last Modified: Fri, 24 Apr 2020 19:24:18 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:137e44204c5f787b06b0902fa7370caaec2678981aa81600aed2393409a6de96
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6719649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563e60546d1dbf482ad7632b907a661f4d1b5b4a9dc0105adb89b0545452b743`
-	Default Command: `["nats-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2020 19:50:13 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 19:50:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 15 May 2020 19:50:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 15 May 2020 19:50:27 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:50:28 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2da3e9f49b6c3ee3b36761ca52b69d8d5eef0937cb74cd8fddbb46850e21eea`  
		Last Modified: Fri, 15 May 2020 19:54:08 GMT  
		Size: 4.1 MB (4099154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf99cc6797b449693d5c09898c063ff989f060f8aec84ee465a356d2a45323c`  
		Last Modified: Fri, 15 May 2020 19:54:06 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:deebc7d7dc1b0429405f75d02ea6b57083cdd895d86b614a651d7623ec14a01e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6499411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f80067dd868fea84d26f61d15ffaa2122d56c7788a50d5cc07243e534c1dff`
-	Default Command: `["nats-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 02:02:16 GMT
ENV NATS_SERVER=2.1.6
# Fri, 24 Apr 2020 02:02:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		arm64) natsArch='arm64' ;; 		armhf) natsArch='arm6' ;; 		armv7) natsArch='arm7' ;; 		x86_64) natsArch='amd64' ;; 		x86) natsArch='386' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 24 Apr 2020 02:02:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 24 Apr 2020 02:02:25 GMT
EXPOSE 4222 6222 8222
# Fri, 24 Apr 2020 02:02:27 GMT
CMD ["nats-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6fe91083b82217baefe1a9f0ed7d83e845198f22641b4d2b3f4b3c309cbac3`  
		Last Modified: Fri, 24 Apr 2020 02:03:03 GMT  
		Size: 4.1 MB (4076790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c4bd5409f67062e55b33a74e24037fc0aed5ad5d8e37095e02415d9ea93b84`  
		Last Modified: Fri, 24 Apr 2020 02:03:03 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:ea10ff7cb0c8a0289cb21f856ca42ac0c4e7441ce40fb9d79e25504b0f89a72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1217; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:03f7a9538ca823f3e342254f0e0bd62fce56410fd037d70f11e208a64b9be51b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4068777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d7629fb1351a52582452f08d569ef8aa395377751df3706474cb5769e8400d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:b5fc4f9d62c474e25c56f62242c0cbb4f21e732408978c639846820bd9b440a3 in /nats-server 
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9bafc186f2720cd817d9a0dca0d2d85b62db3667b346e18ad3cedee711853463`  
		Last Modified: Wed, 01 Apr 2020 06:49:48 GMT  
		Size: 4.1 MB (4068300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99d87cfb673f46f50d4862e4486d00a26509752daa87beb60702054d53a2f8`  
		Last Modified: Wed, 01 Apr 2020 06:49:47 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:bdda6b6ae6c62c1e78f902992214eca27cf00de2fc7d8d47235a663b3b35940a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7120ba5b06cdd64603f112b86a27c044b9e157fbfc6bdfad548f92351f75bbfe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:07:20 GMT
COPY file:846a74a5cdf1833ec24475ab97e1c375ea237825039dd6ad1d133be2c007faaf in /nats-server 
# Wed, 01 Apr 2020 06:07:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:07:23 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:07:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3779a152c2262214f75fbef66a9ffa608a8a92efab5ce35515692282ae11c664`  
		Last Modified: Wed, 01 Apr 2020 06:08:10 GMT  
		Size: 3.8 MB (3774441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54270160df8d1b1d48a5e855464e3400a606022608035ba66e6914d03dd235f1`  
		Last Modified: Wed, 01 Apr 2020 06:08:08 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:983d25974e771f9316c9e4a5bb71b449518805ddb52e6c7878e171bcccecc945
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105081331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dac43460097cf1c43ccb252c52bbba61b8d41b4a7e413763329d909f5d4f89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 14:50:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:41 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Fri, 15 May 2020 20:15:43 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eafb3f3d63d93b402dfcc428e091787a4242326bc71283a6e3ad40046a60cba0`  
		Last Modified: Wed, 13 May 2020 14:55:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516b6f4ab70976d0f6eefe7345d23e3384290ec3d07e5fd84e86a38a9355f2af`  
		Last Modified: Fri, 15 May 2020 20:20:01 GMT  
		Size: 4.1 MB (4056463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63162a0c7c0aaa22ee2b6ad6d892c8fc4e3d3a0b8ddbf7bd7f2b43b97178540b`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84857e1674bb786ff63ae8a8ddc3a7af87297c5623e8649378c6cd00f404f023`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd47e8ce84e533b8e666ae64628d761d36656664b77077b25b1c1b629f37af6`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ec79ba35428ffa62bae3a80bfa890befff422d5089eed1ec724da29df0ab2`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:22e7a4786a4a893d407d2359fd93e1332d46d2bf051596fec67a8cb1469b10d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:03f7a9538ca823f3e342254f0e0bd62fce56410fd037d70f11e208a64b9be51b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4068777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d7629fb1351a52582452f08d569ef8aa395377751df3706474cb5769e8400d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:b5fc4f9d62c474e25c56f62242c0cbb4f21e732408978c639846820bd9b440a3 in /nats-server 
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9bafc186f2720cd817d9a0dca0d2d85b62db3667b346e18ad3cedee711853463`  
		Last Modified: Wed, 01 Apr 2020 06:49:48 GMT  
		Size: 4.1 MB (4068300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99d87cfb673f46f50d4862e4486d00a26509752daa87beb60702054d53a2f8`  
		Last Modified: Wed, 01 Apr 2020 06:49:47 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:bdda6b6ae6c62c1e78f902992214eca27cf00de2fc7d8d47235a663b3b35940a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7120ba5b06cdd64603f112b86a27c044b9e157fbfc6bdfad548f92351f75bbfe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:07:20 GMT
COPY file:846a74a5cdf1833ec24475ab97e1c375ea237825039dd6ad1d133be2c007faaf in /nats-server 
# Wed, 01 Apr 2020 06:07:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:07:23 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:07:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3779a152c2262214f75fbef66a9ffa608a8a92efab5ce35515692282ae11c664`  
		Last Modified: Wed, 01 Apr 2020 06:08:10 GMT  
		Size: 3.8 MB (3774441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54270160df8d1b1d48a5e855464e3400a606022608035ba66e6914d03dd235f1`  
		Last Modified: Wed, 01 Apr 2020 06:08:08 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:e93c53dfa92b3aa8a99b0b82e1e065c6180489121d90d447fbbe352bb04d4334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `nats:nanoserver` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:983d25974e771f9316c9e4a5bb71b449518805ddb52e6c7878e171bcccecc945
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105081331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dac43460097cf1c43ccb252c52bbba61b8d41b4a7e413763329d909f5d4f89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 14:50:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:41 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Fri, 15 May 2020 20:15:43 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eafb3f3d63d93b402dfcc428e091787a4242326bc71283a6e3ad40046a60cba0`  
		Last Modified: Wed, 13 May 2020 14:55:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516b6f4ab70976d0f6eefe7345d23e3384290ec3d07e5fd84e86a38a9355f2af`  
		Last Modified: Fri, 15 May 2020 20:20:01 GMT  
		Size: 4.1 MB (4056463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63162a0c7c0aaa22ee2b6ad6d892c8fc4e3d3a0b8ddbf7bd7f2b43b97178540b`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84857e1674bb786ff63ae8a8ddc3a7af87297c5623e8649378c6cd00f404f023`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd47e8ce84e533b8e666ae64628d761d36656664b77077b25b1c1b629f37af6`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ec79ba35428ffa62bae3a80bfa890befff422d5089eed1ec724da29df0ab2`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:e93c53dfa92b3aa8a99b0b82e1e065c6180489121d90d447fbbe352bb04d4334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:983d25974e771f9316c9e4a5bb71b449518805ddb52e6c7878e171bcccecc945
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105081331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dac43460097cf1c43ccb252c52bbba61b8d41b4a7e413763329d909f5d4f89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 14:50:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:41 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Fri, 15 May 2020 20:15:43 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:45 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eafb3f3d63d93b402dfcc428e091787a4242326bc71283a6e3ad40046a60cba0`  
		Last Modified: Wed, 13 May 2020 14:55:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516b6f4ab70976d0f6eefe7345d23e3384290ec3d07e5fd84e86a38a9355f2af`  
		Last Modified: Fri, 15 May 2020 20:20:01 GMT  
		Size: 4.1 MB (4056463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63162a0c7c0aaa22ee2b6ad6d892c8fc4e3d3a0b8ddbf7bd7f2b43b97178540b`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84857e1674bb786ff63ae8a8ddc3a7af87297c5623e8649378c6cd00f404f023`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd47e8ce84e533b8e666ae64628d761d36656664b77077b25b1c1b629f37af6`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ec79ba35428ffa62bae3a80bfa890befff422d5089eed1ec724da29df0ab2`  
		Last Modified: Fri, 15 May 2020 20:19:56 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:22e7a4786a4a893d407d2359fd93e1332d46d2bf051596fec67a8cb1469b10d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:03f7a9538ca823f3e342254f0e0bd62fce56410fd037d70f11e208a64b9be51b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4068777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d7629fb1351a52582452f08d569ef8aa395377751df3706474cb5769e8400d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:b5fc4f9d62c474e25c56f62242c0cbb4f21e732408978c639846820bd9b440a3 in /nats-server 
# Wed, 01 Apr 2020 06:49:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9bafc186f2720cd817d9a0dca0d2d85b62db3667b346e18ad3cedee711853463`  
		Last Modified: Wed, 01 Apr 2020 06:49:48 GMT  
		Size: 4.1 MB (4068300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99d87cfb673f46f50d4862e4486d00a26509752daa87beb60702054d53a2f8`  
		Last Modified: Wed, 01 Apr 2020 06:49:47 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:bdda6b6ae6c62c1e78f902992214eca27cf00de2fc7d8d47235a663b3b35940a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7120ba5b06cdd64603f112b86a27c044b9e157fbfc6bdfad548f92351f75bbfe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 01 Apr 2020 06:07:20 GMT
COPY file:846a74a5cdf1833ec24475ab97e1c375ea237825039dd6ad1d133be2c007faaf in /nats-server 
# Wed, 01 Apr 2020 06:07:23 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 01 Apr 2020 06:07:23 GMT
EXPOSE 4222 6222 8222
# Wed, 01 Apr 2020 06:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 01 Apr 2020 06:07:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3779a152c2262214f75fbef66a9ffa608a8a92efab5ce35515692282ae11c664`  
		Last Modified: Wed, 01 Apr 2020 06:08:10 GMT  
		Size: 3.8 MB (3774441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54270160df8d1b1d48a5e855464e3400a606022608035ba66e6914d03dd235f1`  
		Last Modified: Wed, 01 Apr 2020 06:08:08 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:284c4850adc39c33100ab1324dbe23ddde7450c6e5bd15da874d459e68e0ea3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda44c76561e9490c8a19cffd362e26a5552c3aafd41c98b9562a6ae8a01874`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 20 Sep 2019 23:29:17 GMT
COPY file:f0dce6fb207b92a78774313458c6030a8ac0653785d2a2d54e8b5c8935d9b6b8 in /nats-server 
# Fri, 18 Oct 2019 18:04:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 18 Oct 2019 18:04:47 GMT
EXPOSE 4222 6222 8222
# Fri, 18 Oct 2019 18:04:48 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 18 Oct 2019 18:04:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:98fcb931241702ef0a04aa16bb1e4bab6b8afd06f792790462dff69dee05835c`  
		Last Modified: Fri, 20 Sep 2019 23:29:32 GMT  
		Size: 3.7 MB (3665294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e761cba9328047725686c1ed6eecd9eeef33879d348aea70fb3d219b546165`  
		Last Modified: Fri, 18 Oct 2019 18:05:08 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:79891322cb1d314fc48bc91e5fb81898349861c3689ba759a7ed8c9ffd0f72e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64
	-	windows version 10.0.14393.3686; amd64

### `nats:windowsservercore` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:2e808e4820850550bfe857b7882f9d2ec3770e0a77135137b715ee56f8865a3d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723094192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb5eb9524269197d09f9bfd26b36ba48e1c49a38ab8dd9c549052b31db4308d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 13:04:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:49:24 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:14:14 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:14:35 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:15:25 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:15:26 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:27 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6e220442d94ba050201e82fee90c58b5e714748e7906735032367404c473c91c`  
		Last Modified: Wed, 13 May 2020 14:27:38 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef78e6a0bb5c035fff387c2c5470bd8420babb53d74f1856b9e3ed900cd9af2`  
		Last Modified: Wed, 13 May 2020 14:54:40 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3733fe8392820a6176aabbce2fea6e7f5cef35d18d29c985b3d6d8ca530b040`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ec67b51ba3368bcc10659dea28daabcfc7f499ebfcfd842eb0225d3ef64bc3`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e950aa317a893230e32972c9029d3055b3c97b947e8edd05d14f8a8171bf4b`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 363.9 KB (363883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad60f095cd746e908ba4cbf28bf09d893d3bed31ab282e76a82fda02a2920c6a`  
		Last Modified: Fri, 15 May 2020 20:19:41 GMT  
		Size: 4.4 MB (4387713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213500fe8035d9fbefc9fc80861db0087b3faa36c0cec1fd54f1df89d563f0c5`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bad6f3a4966270bdc5ea21caec6010e5cc8fa9b5702d54af3f80bc4be10fec`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0be37cd8bdefc66402e2d1b8f176c815ab9387935ca74f36fa899efa9604b3`  
		Last Modified: Fri, 15 May 2020 20:19:35 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c352832c962e7536881277d349b432e55dda53ddb36f026e2af6ed3a2e02ed3d`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.3686; amd64

```console
$ docker pull nats@sha256:7d6dc2fc9b5be7820c127bb780394be4df5edd15ead8fe4ee35111825b09fbf0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5751211970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ce5815af4bf55d474ff2df1c879f7f1c76df45820494ee959d5b15a8c06c8c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 13:13:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:51:03 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:53 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:15:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:16:54 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:18:43 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:18:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:18:47 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:18:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:18:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d9ecf24b3b7ef3e61c8b38d40e28e57a80552d6c97884f4cc142af2110ddff`  
		Last Modified: Wed, 13 May 2020 14:28:09 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356fa8d07c48624dd3553b12cafae53b1e6818e2e77c7b4ad7c5e37a6edf5f5`  
		Last Modified: Wed, 13 May 2020 14:55:20 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9053aba643e655abc4300887f89356fa95a058b168b8d3404b5627365ce052a`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39bb0a54403409eeecf7ca0af5b7256923560250ba96cf5c6559ba385ac63ff`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26a263f1c36137f9ae855980e5932549cd9ba1b2d46f835ec4436f85161680`  
		Last Modified: Fri, 15 May 2020 20:20:20 GMT  
		Size: 5.4 MB (5380243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c19479d4b0b4596257e15252e96bb469f2347136f7714e78a0392001039914a`  
		Last Modified: Fri, 15 May 2020 20:20:24 GMT  
		Size: 13.9 MB (13932166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5f6330c66b8c1505013ec5f840e8a1d49e0d2e486d31927832512fba92e373`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c740936073ba5f4006ea263354ff9fa5e0b59bc5b3945a6cbc4f7458531ad83`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f31836cddc824c6c9fbd8264bda5ec6369a6d10eb828e04528c6989a11c7a1`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4187a4d9e22eb583a18d4ff3c1c002ec90c4841754c44cf33db01ad1fe0ec26`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:f29246f54ab87c353272363dc66d3c4c048e1509a00978c0948bf7444af6e691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull nats@sha256:2e808e4820850550bfe857b7882f9d2ec3770e0a77135137b715ee56f8865a3d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1723094192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb5eb9524269197d09f9bfd26b36ba48e1c49a38ab8dd9c549052b31db4308d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 13:04:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:49:24 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:14:14 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:14:15 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:14:35 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:15:25 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:15:26 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:15:27 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:15:27 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:15:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6e220442d94ba050201e82fee90c58b5e714748e7906735032367404c473c91c`  
		Last Modified: Wed, 13 May 2020 14:27:38 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef78e6a0bb5c035fff387c2c5470bd8420babb53d74f1856b9e3ed900cd9af2`  
		Last Modified: Wed, 13 May 2020 14:54:40 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3733fe8392820a6176aabbce2fea6e7f5cef35d18d29c985b3d6d8ca530b040`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ec67b51ba3368bcc10659dea28daabcfc7f499ebfcfd842eb0225d3ef64bc3`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e950aa317a893230e32972c9029d3055b3c97b947e8edd05d14f8a8171bf4b`  
		Last Modified: Fri, 15 May 2020 20:19:38 GMT  
		Size: 363.9 KB (363883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad60f095cd746e908ba4cbf28bf09d893d3bed31ab282e76a82fda02a2920c6a`  
		Last Modified: Fri, 15 May 2020 20:19:41 GMT  
		Size: 4.4 MB (4387713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213500fe8035d9fbefc9fc80861db0087b3faa36c0cec1fd54f1df89d563f0c5`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bad6f3a4966270bdc5ea21caec6010e5cc8fa9b5702d54af3f80bc4be10fec`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0be37cd8bdefc66402e2d1b8f176c815ab9387935ca74f36fa899efa9604b3`  
		Last Modified: Fri, 15 May 2020 20:19:35 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c352832c962e7536881277d349b432e55dda53ddb36f026e2af6ed3a2e02ed3d`  
		Last Modified: Fri, 15 May 2020 20:19:36 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:2715bb95a8cc376301a71de3e59d4d2563b22a7e4b0b410d3eabc8b9f2d59e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull nats@sha256:7d6dc2fc9b5be7820c127bb780394be4df5edd15ead8fe4ee35111825b09fbf0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5751211970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ce5815af4bf55d474ff2df1c879f7f1c76df45820494ee959d5b15a8c06c8c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 13:13:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2020 14:51:03 GMT
ENV NATS_DOCKERIZED=1
# Fri, 15 May 2020 20:15:53 GMT
ENV NATS_SERVER=2.1.7
# Fri, 15 May 2020 20:15:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Fri, 15 May 2020 20:16:54 GMT
RUN Set-PSDebug -Trace 2
# Fri, 15 May 2020 20:18:43 GMT
RUN Write-Host ('downloading from {0}' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*
# Fri, 15 May 2020 20:18:45 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 15 May 2020 20:18:47 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 20:18:48 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 15 May 2020 20:18:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d9ecf24b3b7ef3e61c8b38d40e28e57a80552d6c97884f4cc142af2110ddff`  
		Last Modified: Wed, 13 May 2020 14:28:09 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356fa8d07c48624dd3553b12cafae53b1e6818e2e77c7b4ad7c5e37a6edf5f5`  
		Last Modified: Wed, 13 May 2020 14:55:20 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9053aba643e655abc4300887f89356fa95a058b168b8d3404b5627365ce052a`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39bb0a54403409eeecf7ca0af5b7256923560250ba96cf5c6559ba385ac63ff`  
		Last Modified: Fri, 15 May 2020 20:20:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26a263f1c36137f9ae855980e5932549cd9ba1b2d46f835ec4436f85161680`  
		Last Modified: Fri, 15 May 2020 20:20:20 GMT  
		Size: 5.4 MB (5380243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c19479d4b0b4596257e15252e96bb469f2347136f7714e78a0392001039914a`  
		Last Modified: Fri, 15 May 2020 20:20:24 GMT  
		Size: 13.9 MB (13932166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5f6330c66b8c1505013ec5f840e8a1d49e0d2e486d31927832512fba92e373`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.7 KB (1702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c740936073ba5f4006ea263354ff9fa5e0b59bc5b3945a6cbc4f7458531ad83`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f31836cddc824c6c9fbd8264bda5ec6369a6d10eb828e04528c6989a11c7a1`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4187a4d9e22eb583a18d4ff3c1c002ec90c4841754c44cf33db01ad1fe0ec26`  
		Last Modified: Fri, 15 May 2020 20:20:16 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
