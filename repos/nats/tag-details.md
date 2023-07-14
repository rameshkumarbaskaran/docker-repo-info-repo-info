<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.18`](#nats2-alpine318)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.9`](#nats29)
-	[`nats:2.9-alpine`](#nats29-alpine)
-	[`nats:2.9-alpine3.18`](#nats29-alpine318)
-	[`nats:2.9-linux`](#nats29-linux)
-	[`nats:2.9-nanoserver`](#nats29-nanoserver)
-	[`nats:2.9-nanoserver-1809`](#nats29-nanoserver-1809)
-	[`nats:2.9-scratch`](#nats29-scratch)
-	[`nats:2.9-windowsservercore`](#nats29-windowsservercore)
-	[`nats:2.9-windowsservercore-1809`](#nats29-windowsservercore-1809)
-	[`nats:2.9.20`](#nats2920)
-	[`nats:2.9.20-alpine`](#nats2920-alpine)
-	[`nats:2.9.20-alpine3.18`](#nats2920-alpine318)
-	[`nats:2.9.20-linux`](#nats2920-linux)
-	[`nats:2.9.20-nanoserver`](#nats2920-nanoserver)
-	[`nats:2.9.20-nanoserver-1809`](#nats2920-nanoserver-1809)
-	[`nats:2.9.20-scratch`](#nats2920-scratch)
-	[`nats:2.9.20-windowsservercore`](#nats2920-windowsservercore)
-	[`nats:2.9.20-windowsservercore-1809`](#nats2920-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.18`](#natsalpine318)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:8e0fb53c305217c0f29f21e8176fce1f4f11648c96543f0970666d8596e2d69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4645; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:700a4b586eb96ff46eef5a949c50297d689f8b31d62ea1ca773dd6895c3f039d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5126531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5907f5a08f299f1dacf051a9fc09fb9189deb2b0dce45877975471766b706954`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:83ff3835bde68ad26982d2ccc535db9982a508facc29fdbcbbfb9675666fbdc6 in /nats-server 
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:29:32 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:29:33 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:29:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67e402a9bce54a5dfde340b14dba6b73ef42a3b94cb337301bf4374e77ec7040`  
		Last Modified: Thu, 13 Jul 2023 22:30:12 GMT  
		Size: 5.1 MB (5126023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a9f6e59497aefb2b8a64f61ee04f476641f2b25c8c62c37e5fdfaab68f8f7e`  
		Last Modified: Thu, 13 Jul 2023 22:30:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:6fd7bfb33bbf19e7ccb75c6ac3fcdc072b6120923fdb4e96e29492a5e7b89289
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4890101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d7fa51b81b0dcfb6ee49a1b74a5881dbf8163021afff101d2002b70686142a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:b5f9cb21b49e06d0ef4d044cf5d2fa6f64bbabb0cfb73701be4fa9d1e7c16c56 in /nats-server 
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 21:49:27 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:505fc4baba759223316e40a0109c61f162bb1d1acafb25bbc8e92b684cd58c5e`  
		Last Modified: Thu, 13 Jul 2023 21:50:07 GMT  
		Size: 4.9 MB (4889594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc06a01182930b7a494867f205f3a02b099200299bffa49031f3085b8952f64`  
		Last Modified: Thu, 13 Jul 2023 21:50:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ec4eab4197d5b340c7bcbbfda1e3bca6ac9874273362a95cb4f58157884759e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab94676f2d9fc59f778cd1526e8664a87db5a1b0741b2053991fb0fb00a2a16a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:53:11 GMT
COPY file:b1a666d296b7b01c216ccd9e1f03715958de83d192993bc8ab769d7998b1703f in /nats-server 
# Thu, 13 Jul 2023 22:53:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:53:12 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:775e6a1e06f337eb4fc74b89e37d008aac2e092d4bfd8d25f944b5b8d257bf8e`  
		Last Modified: Thu, 13 Jul 2023 22:53:52 GMT  
		Size: 4.9 MB (4880250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e8a9e7894a37f644a39457db86f9e94f7b92aadfeac1fd47ee846be3c7eb8f`  
		Last Modified: Thu, 13 Jul 2023 22:53:51 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb5aafaa1c1ada08d1342efaacdbbc72351ea5fa9ed825ec83c84c194a1793aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411f554cbcd46eb35b3ba4cd400a5e29132ded085f6ec4efaccaa6121a464db9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 23:11:18 GMT
COPY file:75a8428ab964e430ddc475b81bfe8411c8a1a8487d06f66b7b2be85ebca4c05f in /nats-server 
# Thu, 13 Jul 2023 23:11:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 23:11:19 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 23:11:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 23:11:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff35e5a1c81a5e14fcb0cddaf7b6bb7a86d01c91297fc204d6f59f81ab699f42`  
		Last Modified: Thu, 13 Jul 2023 23:11:55 GMT  
		Size: 4.7 MB (4694032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ddd8ff8791364717d428b048bce331ac51b1654fac486b5b5d64c7f9a6bd1`  
		Last Modified: Thu, 13 Jul 2023 23:11:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:63c26578744b038b074f43eb6c0b3958667480b48bfe2a74c675fa52295f6767
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109612796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7071df68a96690f5443acb6ef9a47cea84abc3e0dd4a92efaa064a3144b56ed2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Fri, 14 Jul 2023 00:03:16 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:a5074ddde966142308b669c647979e812040bd9a0280cfce51a983385df577ec in C:\nats-server.exe 
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:03:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bad9bf846d07362d8295a4479f8f2965dfb5934a9a032b335ce3cb086bdf7`  
		Last Modified: Fri, 14 Jul 2023 00:04:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b0789d7cd0ee38c3d2d6f0d8d4662e4e4f242055fa09752c571e9e0b12b25`  
		Last Modified: Fri, 14 Jul 2023 00:04:05 GMT  
		Size: 5.2 MB (5198141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7714f1d09ea353a9769c79f15345a77c802214a0d24c3ed987cf9bc90fa67933`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4710eb1eae23febe62cd19d1e08fda4c2417972b715e389b5078de0796c915f`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2187cbf833c204e29fc58f360a3c3c572ea7fe8140d088f10f16abeb6666d374`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f146e585d072cd21e48a1fd715a9e5ba5233a54652a5494c2efe8216b210ade`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:d6c6ae7df4a0c5f7aa5ec8035501b7a594d065216aa227265c89909a3c31df96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:89314efbfded0bd51e0b70966ebb7ad753245d6b680d4d999c25904838954a84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f3a7141f662bd0bab1c885fe0237733c81118613c3e2a1f041bf7d1cab81d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:29:16 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:29:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:29:18 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:29:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688e12de30012d849a08c4b3a056bf9462831be6349fedb514a9b943c5d3b038`  
		Last Modified: Thu, 13 Jul 2023 22:29:51 GMT  
		Size: 5.4 MB (5411416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcb04c9ced60dff0180f5da5e6f033545ec0a56faed6b9ea1f00c88a9ed3847`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086da10bd35caa5abb0061f428f619d8dd071a2fb7c760eead2ceb0bb7536e58`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c1cb16ffa939bd8f1601f657d500e3bd5c45005c28c448b68ec5b4b996fe430e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8318264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83f1c1fe0f07fee40eabe8e9253b5ac08578d588938045575e96a038b76964f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 21:49:19 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 21:49:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 21:49:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 21:49:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbd7a095ebb0cf47214d570aaa6e8beb1144d038098b2cc64526b8119b7a072`  
		Last Modified: Thu, 13 Jul 2023 21:49:46 GMT  
		Size: 5.2 MB (5173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc62259aed8a302b7cb52adf9701c763fb05897f5965d7873f6e27e88d4e07e`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3f8be8762d1cac21e849032e638a3ebf9bbb3957511eba1b7321783b83f23c`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:05b3018971114ff61d10e947e304f35c7bbc0abee425911c0fd58e23f7ae74e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8068141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4043b810630b65430ae04fb007b13c892d5e16ae40ea86b45712575d54868208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 22:36:15 GMT
ADD file:082f034323c559f3cb9feb6422c88b1ec8017f436d6109e238a5c5384a32a90a in / 
# Wed, 14 Jun 2023 22:36:15 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:52:54 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:52:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:52:57 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:52:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:52:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:633ba29fd335042456b6e2c073636f6fa30de56f1331c442914739b92a479974`  
		Last Modified: Wed, 14 Jun 2023 22:36:49 GMT  
		Size: 2.9 MB (2898508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b240facc4a312dbc41a0d9d2b5f34f26188edc082396407147566f4670a7bd`  
		Last Modified: Thu, 13 Jul 2023 22:53:30 GMT  
		Size: 5.2 MB (5168636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c49f0e2539269574bfe0565b74747b67dc174076c7d3b2b2c8064b2af71a80`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f69564b85401d79f11d3d0dd7775aa0dfa3d09c58f3daedcbe1f3fe676eea`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:aa93c00cb94a9cf48edbefb3fbb029b8d8187ccf4735f2eff181906d0e869854
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8309359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc0605733abd9e160812417dd92d5c4812e0640ef2a71568b2f2aed85eb6685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 23:11:00 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 23:11:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 23:11:03 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 23:11:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8d12353ca807b3f28a178dcf6ddfe80ac709c12b0da6364e48db96ab06e400`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 5.0 MB (4979109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7977030405ec12383b1b2033bc0fceb08f5c959b13d57ba18f74f11efee542ed`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041d1130902bd23c5b39754ecf01c19ed66a35c6e60064301df126b0f52259ad`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.18`

```console
$ docker pull nats@sha256:d6c6ae7df4a0c5f7aa5ec8035501b7a594d065216aa227265c89909a3c31df96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:89314efbfded0bd51e0b70966ebb7ad753245d6b680d4d999c25904838954a84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f3a7141f662bd0bab1c885fe0237733c81118613c3e2a1f041bf7d1cab81d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:29:16 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:29:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:29:18 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:29:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688e12de30012d849a08c4b3a056bf9462831be6349fedb514a9b943c5d3b038`  
		Last Modified: Thu, 13 Jul 2023 22:29:51 GMT  
		Size: 5.4 MB (5411416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcb04c9ced60dff0180f5da5e6f033545ec0a56faed6b9ea1f00c88a9ed3847`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086da10bd35caa5abb0061f428f619d8dd071a2fb7c760eead2ceb0bb7536e58`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:c1cb16ffa939bd8f1601f657d500e3bd5c45005c28c448b68ec5b4b996fe430e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8318264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83f1c1fe0f07fee40eabe8e9253b5ac08578d588938045575e96a038b76964f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 21:49:19 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 21:49:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 21:49:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 21:49:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbd7a095ebb0cf47214d570aaa6e8beb1144d038098b2cc64526b8119b7a072`  
		Last Modified: Thu, 13 Jul 2023 21:49:46 GMT  
		Size: 5.2 MB (5173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc62259aed8a302b7cb52adf9701c763fb05897f5965d7873f6e27e88d4e07e`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3f8be8762d1cac21e849032e638a3ebf9bbb3957511eba1b7321783b83f23c`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:05b3018971114ff61d10e947e304f35c7bbc0abee425911c0fd58e23f7ae74e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8068141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4043b810630b65430ae04fb007b13c892d5e16ae40ea86b45712575d54868208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 22:36:15 GMT
ADD file:082f034323c559f3cb9feb6422c88b1ec8017f436d6109e238a5c5384a32a90a in / 
# Wed, 14 Jun 2023 22:36:15 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:52:54 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:52:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:52:57 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:52:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:52:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:633ba29fd335042456b6e2c073636f6fa30de56f1331c442914739b92a479974`  
		Last Modified: Wed, 14 Jun 2023 22:36:49 GMT  
		Size: 2.9 MB (2898508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b240facc4a312dbc41a0d9d2b5f34f26188edc082396407147566f4670a7bd`  
		Last Modified: Thu, 13 Jul 2023 22:53:30 GMT  
		Size: 5.2 MB (5168636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c49f0e2539269574bfe0565b74747b67dc174076c7d3b2b2c8064b2af71a80`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f69564b85401d79f11d3d0dd7775aa0dfa3d09c58f3daedcbe1f3fe676eea`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:aa93c00cb94a9cf48edbefb3fbb029b8d8187ccf4735f2eff181906d0e869854
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8309359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc0605733abd9e160812417dd92d5c4812e0640ef2a71568b2f2aed85eb6685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 23:11:00 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 23:11:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 23:11:03 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 23:11:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8d12353ca807b3f28a178dcf6ddfe80ac709c12b0da6364e48db96ab06e400`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 5.0 MB (4979109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7977030405ec12383b1b2033bc0fceb08f5c959b13d57ba18f74f11efee542ed`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041d1130902bd23c5b39754ecf01c19ed66a35c6e60064301df126b0f52259ad`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:54beaa3c85e41593c8d7f235ac1ecea3c3dd2eeb63dc2f53e75a8094579ff7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:700a4b586eb96ff46eef5a949c50297d689f8b31d62ea1ca773dd6895c3f039d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5126531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5907f5a08f299f1dacf051a9fc09fb9189deb2b0dce45877975471766b706954`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:83ff3835bde68ad26982d2ccc535db9982a508facc29fdbcbbfb9675666fbdc6 in /nats-server 
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:29:32 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:29:33 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:29:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67e402a9bce54a5dfde340b14dba6b73ef42a3b94cb337301bf4374e77ec7040`  
		Last Modified: Thu, 13 Jul 2023 22:30:12 GMT  
		Size: 5.1 MB (5126023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a9f6e59497aefb2b8a64f61ee04f476641f2b25c8c62c37e5fdfaab68f8f7e`  
		Last Modified: Thu, 13 Jul 2023 22:30:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:6fd7bfb33bbf19e7ccb75c6ac3fcdc072b6120923fdb4e96e29492a5e7b89289
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4890101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d7fa51b81b0dcfb6ee49a1b74a5881dbf8163021afff101d2002b70686142a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:b5f9cb21b49e06d0ef4d044cf5d2fa6f64bbabb0cfb73701be4fa9d1e7c16c56 in /nats-server 
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 21:49:27 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:505fc4baba759223316e40a0109c61f162bb1d1acafb25bbc8e92b684cd58c5e`  
		Last Modified: Thu, 13 Jul 2023 21:50:07 GMT  
		Size: 4.9 MB (4889594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc06a01182930b7a494867f205f3a02b099200299bffa49031f3085b8952f64`  
		Last Modified: Thu, 13 Jul 2023 21:50:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ec4eab4197d5b340c7bcbbfda1e3bca6ac9874273362a95cb4f58157884759e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab94676f2d9fc59f778cd1526e8664a87db5a1b0741b2053991fb0fb00a2a16a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:53:11 GMT
COPY file:b1a666d296b7b01c216ccd9e1f03715958de83d192993bc8ab769d7998b1703f in /nats-server 
# Thu, 13 Jul 2023 22:53:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:53:12 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:775e6a1e06f337eb4fc74b89e37d008aac2e092d4bfd8d25f944b5b8d257bf8e`  
		Last Modified: Thu, 13 Jul 2023 22:53:52 GMT  
		Size: 4.9 MB (4880250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e8a9e7894a37f644a39457db86f9e94f7b92aadfeac1fd47ee846be3c7eb8f`  
		Last Modified: Thu, 13 Jul 2023 22:53:51 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb5aafaa1c1ada08d1342efaacdbbc72351ea5fa9ed825ec83c84c194a1793aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411f554cbcd46eb35b3ba4cd400a5e29132ded085f6ec4efaccaa6121a464db9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 23:11:18 GMT
COPY file:75a8428ab964e430ddc475b81bfe8411c8a1a8487d06f66b7b2be85ebca4c05f in /nats-server 
# Thu, 13 Jul 2023 23:11:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 23:11:19 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 23:11:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 23:11:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff35e5a1c81a5e14fcb0cddaf7b6bb7a86d01c91297fc204d6f59f81ab699f42`  
		Last Modified: Thu, 13 Jul 2023 23:11:55 GMT  
		Size: 4.7 MB (4694032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ddd8ff8791364717d428b048bce331ac51b1654fac486b5b5d64c7f9a6bd1`  
		Last Modified: Thu, 13 Jul 2023 23:11:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:bfff91215109e40d5a3d637ce8bc11a4bae8b3a555e2c79188bab93b2397278b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:63c26578744b038b074f43eb6c0b3958667480b48bfe2a74c675fa52295f6767
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109612796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7071df68a96690f5443acb6ef9a47cea84abc3e0dd4a92efaa064a3144b56ed2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Fri, 14 Jul 2023 00:03:16 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:a5074ddde966142308b669c647979e812040bd9a0280cfce51a983385df577ec in C:\nats-server.exe 
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:03:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bad9bf846d07362d8295a4479f8f2965dfb5934a9a032b335ce3cb086bdf7`  
		Last Modified: Fri, 14 Jul 2023 00:04:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b0789d7cd0ee38c3d2d6f0d8d4662e4e4f242055fa09752c571e9e0b12b25`  
		Last Modified: Fri, 14 Jul 2023 00:04:05 GMT  
		Size: 5.2 MB (5198141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7714f1d09ea353a9769c79f15345a77c802214a0d24c3ed987cf9bc90fa67933`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4710eb1eae23febe62cd19d1e08fda4c2417972b715e389b5078de0796c915f`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2187cbf833c204e29fc58f360a3c3c572ea7fe8140d088f10f16abeb6666d374`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f146e585d072cd21e48a1fd715a9e5ba5233a54652a5494c2efe8216b210ade`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:bfff91215109e40d5a3d637ce8bc11a4bae8b3a555e2c79188bab93b2397278b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:63c26578744b038b074f43eb6c0b3958667480b48bfe2a74c675fa52295f6767
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109612796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7071df68a96690f5443acb6ef9a47cea84abc3e0dd4a92efaa064a3144b56ed2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Fri, 14 Jul 2023 00:03:16 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:a5074ddde966142308b669c647979e812040bd9a0280cfce51a983385df577ec in C:\nats-server.exe 
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:03:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bad9bf846d07362d8295a4479f8f2965dfb5934a9a032b335ce3cb086bdf7`  
		Last Modified: Fri, 14 Jul 2023 00:04:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b0789d7cd0ee38c3d2d6f0d8d4662e4e4f242055fa09752c571e9e0b12b25`  
		Last Modified: Fri, 14 Jul 2023 00:04:05 GMT  
		Size: 5.2 MB (5198141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7714f1d09ea353a9769c79f15345a77c802214a0d24c3ed987cf9bc90fa67933`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4710eb1eae23febe62cd19d1e08fda4c2417972b715e389b5078de0796c915f`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2187cbf833c204e29fc58f360a3c3c572ea7fe8140d088f10f16abeb6666d374`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f146e585d072cd21e48a1fd715a9e5ba5233a54652a5494c2efe8216b210ade`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:54beaa3c85e41593c8d7f235ac1ecea3c3dd2eeb63dc2f53e75a8094579ff7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:700a4b586eb96ff46eef5a949c50297d689f8b31d62ea1ca773dd6895c3f039d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5126531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5907f5a08f299f1dacf051a9fc09fb9189deb2b0dce45877975471766b706954`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:83ff3835bde68ad26982d2ccc535db9982a508facc29fdbcbbfb9675666fbdc6 in /nats-server 
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:29:32 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:29:33 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:29:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67e402a9bce54a5dfde340b14dba6b73ef42a3b94cb337301bf4374e77ec7040`  
		Last Modified: Thu, 13 Jul 2023 22:30:12 GMT  
		Size: 5.1 MB (5126023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a9f6e59497aefb2b8a64f61ee04f476641f2b25c8c62c37e5fdfaab68f8f7e`  
		Last Modified: Thu, 13 Jul 2023 22:30:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:6fd7bfb33bbf19e7ccb75c6ac3fcdc072b6120923fdb4e96e29492a5e7b89289
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4890101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d7fa51b81b0dcfb6ee49a1b74a5881dbf8163021afff101d2002b70686142a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:b5f9cb21b49e06d0ef4d044cf5d2fa6f64bbabb0cfb73701be4fa9d1e7c16c56 in /nats-server 
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 21:49:27 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:505fc4baba759223316e40a0109c61f162bb1d1acafb25bbc8e92b684cd58c5e`  
		Last Modified: Thu, 13 Jul 2023 21:50:07 GMT  
		Size: 4.9 MB (4889594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc06a01182930b7a494867f205f3a02b099200299bffa49031f3085b8952f64`  
		Last Modified: Thu, 13 Jul 2023 21:50:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ec4eab4197d5b340c7bcbbfda1e3bca6ac9874273362a95cb4f58157884759e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab94676f2d9fc59f778cd1526e8664a87db5a1b0741b2053991fb0fb00a2a16a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:53:11 GMT
COPY file:b1a666d296b7b01c216ccd9e1f03715958de83d192993bc8ab769d7998b1703f in /nats-server 
# Thu, 13 Jul 2023 22:53:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:53:12 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:775e6a1e06f337eb4fc74b89e37d008aac2e092d4bfd8d25f944b5b8d257bf8e`  
		Last Modified: Thu, 13 Jul 2023 22:53:52 GMT  
		Size: 4.9 MB (4880250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e8a9e7894a37f644a39457db86f9e94f7b92aadfeac1fd47ee846be3c7eb8f`  
		Last Modified: Thu, 13 Jul 2023 22:53:51 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb5aafaa1c1ada08d1342efaacdbbc72351ea5fa9ed825ec83c84c194a1793aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411f554cbcd46eb35b3ba4cd400a5e29132ded085f6ec4efaccaa6121a464db9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 23:11:18 GMT
COPY file:75a8428ab964e430ddc475b81bfe8411c8a1a8487d06f66b7b2be85ebca4c05f in /nats-server 
# Thu, 13 Jul 2023 23:11:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 23:11:19 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 23:11:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 23:11:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff35e5a1c81a5e14fcb0cddaf7b6bb7a86d01c91297fc204d6f59f81ab699f42`  
		Last Modified: Thu, 13 Jul 2023 23:11:55 GMT  
		Size: 4.7 MB (4694032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ddd8ff8791364717d428b048bce331ac51b1654fac486b5b5d64c7f9a6bd1`  
		Last Modified: Thu, 13 Jul 2023 23:11:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:a8c2c33cbe248ffdf05cf1e29ce7026eefd132eb0cd15aff802e6031f5e1e6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:0fe2b83b4b22020701d93f9a59fb4fdbcfa157be7fb04e9288db445b76eaee4f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1945570306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fbdb411f499afb755df4b20ab636581d3aaed9c3a91c502ef50eeb34352001`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 22:38:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 14 Jul 2023 00:00:18 GMT
ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:00:19 GMT
ENV NATS_SERVER=2.9.20
# Fri, 14 Jul 2023 00:00:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.20/nats-server-v2.9.20-windows-amd64.zip
# Fri, 14 Jul 2023 00:00:21 GMT
ENV NATS_SERVER_SHASUM=6dd2f4648c3b5f7c0b0a2fc492ecd2263d3dfb22ea5cf2d0c018a82f0e912b35
# Fri, 14 Jul 2023 00:01:20 GMT
RUN Set-PSDebug -Trace 2
# Fri, 14 Jul 2023 00:02:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 14 Jul 2023 00:02:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:02:58 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:02:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b452db6d50a62b6e0e8dadb19715cfcf62cf73e54b5d3bac96621c1093673c`  
		Last Modified: Thu, 13 Jul 2023 23:25:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f8ca4b8d322e27c827c0ba667217bc04a39b69f5f483d5f2f9726e6d42522e`  
		Last Modified: Fri, 14 Jul 2023 00:03:50 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f33781e88272c93d82ac65b1dfc5a07ce75d4e8e04e8561f158831356e7fea4`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe631d552a5255bffd0e5aeec249b1684a7e8c75fe30b185e199fbfdecedfae`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb256a4292680f56d2092582b633530842c97891e2f740aa78403b240999c630`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb7d2753eb8c81851f9e3869d39a0947479d1411590331b94108e9cb2bef9e5`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 226.1 KB (226138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c118d6802e5d239c3513560bc388331e2aaf975937a7aa8625dc85e54015becc`  
		Last Modified: Fri, 14 Jul 2023 00:03:47 GMT  
		Size: 5.6 MB (5641748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689840dc0e8e1fb392e9005f0603c05fb29100193e9d6b8528369ce241b81dee`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5788a19b6a5a361435ec99a16308610c901b5452d1281dc9bdab065485a4ad1`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa4bedb48935e18d91878ff81f1b80d8e4ff1149700225914c54b1a6b83933c`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f710347dc06495d6660dfd5cbc8d9c4f5f4555d2ac5e26adc76ee8de42bc75ca`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:a8c2c33cbe248ffdf05cf1e29ce7026eefd132eb0cd15aff802e6031f5e1e6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:0fe2b83b4b22020701d93f9a59fb4fdbcfa157be7fb04e9288db445b76eaee4f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1945570306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fbdb411f499afb755df4b20ab636581d3aaed9c3a91c502ef50eeb34352001`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 22:38:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 14 Jul 2023 00:00:18 GMT
ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:00:19 GMT
ENV NATS_SERVER=2.9.20
# Fri, 14 Jul 2023 00:00:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.20/nats-server-v2.9.20-windows-amd64.zip
# Fri, 14 Jul 2023 00:00:21 GMT
ENV NATS_SERVER_SHASUM=6dd2f4648c3b5f7c0b0a2fc492ecd2263d3dfb22ea5cf2d0c018a82f0e912b35
# Fri, 14 Jul 2023 00:01:20 GMT
RUN Set-PSDebug -Trace 2
# Fri, 14 Jul 2023 00:02:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 14 Jul 2023 00:02:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:02:58 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:02:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b452db6d50a62b6e0e8dadb19715cfcf62cf73e54b5d3bac96621c1093673c`  
		Last Modified: Thu, 13 Jul 2023 23:25:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f8ca4b8d322e27c827c0ba667217bc04a39b69f5f483d5f2f9726e6d42522e`  
		Last Modified: Fri, 14 Jul 2023 00:03:50 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f33781e88272c93d82ac65b1dfc5a07ce75d4e8e04e8561f158831356e7fea4`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe631d552a5255bffd0e5aeec249b1684a7e8c75fe30b185e199fbfdecedfae`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb256a4292680f56d2092582b633530842c97891e2f740aa78403b240999c630`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb7d2753eb8c81851f9e3869d39a0947479d1411590331b94108e9cb2bef9e5`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 226.1 KB (226138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c118d6802e5d239c3513560bc388331e2aaf975937a7aa8625dc85e54015becc`  
		Last Modified: Fri, 14 Jul 2023 00:03:47 GMT  
		Size: 5.6 MB (5641748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689840dc0e8e1fb392e9005f0603c05fb29100193e9d6b8528369ce241b81dee`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5788a19b6a5a361435ec99a16308610c901b5452d1281dc9bdab065485a4ad1`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa4bedb48935e18d91878ff81f1b80d8e4ff1149700225914c54b1a6b83933c`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f710347dc06495d6660dfd5cbc8d9c4f5f4555d2ac5e26adc76ee8de42bc75ca`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:8e0fb53c305217c0f29f21e8176fce1f4f11648c96543f0970666d8596e2d69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4645; amd64

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:700a4b586eb96ff46eef5a949c50297d689f8b31d62ea1ca773dd6895c3f039d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5126531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5907f5a08f299f1dacf051a9fc09fb9189deb2b0dce45877975471766b706954`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:83ff3835bde68ad26982d2ccc535db9982a508facc29fdbcbbfb9675666fbdc6 in /nats-server 
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:29:32 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:29:33 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:29:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67e402a9bce54a5dfde340b14dba6b73ef42a3b94cb337301bf4374e77ec7040`  
		Last Modified: Thu, 13 Jul 2023 22:30:12 GMT  
		Size: 5.1 MB (5126023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a9f6e59497aefb2b8a64f61ee04f476641f2b25c8c62c37e5fdfaab68f8f7e`  
		Last Modified: Thu, 13 Jul 2023 22:30:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:6fd7bfb33bbf19e7ccb75c6ac3fcdc072b6120923fdb4e96e29492a5e7b89289
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4890101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d7fa51b81b0dcfb6ee49a1b74a5881dbf8163021afff101d2002b70686142a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:b5f9cb21b49e06d0ef4d044cf5d2fa6f64bbabb0cfb73701be4fa9d1e7c16c56 in /nats-server 
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 21:49:27 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:505fc4baba759223316e40a0109c61f162bb1d1acafb25bbc8e92b684cd58c5e`  
		Last Modified: Thu, 13 Jul 2023 21:50:07 GMT  
		Size: 4.9 MB (4889594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc06a01182930b7a494867f205f3a02b099200299bffa49031f3085b8952f64`  
		Last Modified: Thu, 13 Jul 2023 21:50:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ec4eab4197d5b340c7bcbbfda1e3bca6ac9874273362a95cb4f58157884759e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab94676f2d9fc59f778cd1526e8664a87db5a1b0741b2053991fb0fb00a2a16a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:53:11 GMT
COPY file:b1a666d296b7b01c216ccd9e1f03715958de83d192993bc8ab769d7998b1703f in /nats-server 
# Thu, 13 Jul 2023 22:53:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:53:12 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:775e6a1e06f337eb4fc74b89e37d008aac2e092d4bfd8d25f944b5b8d257bf8e`  
		Last Modified: Thu, 13 Jul 2023 22:53:52 GMT  
		Size: 4.9 MB (4880250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e8a9e7894a37f644a39457db86f9e94f7b92aadfeac1fd47ee846be3c7eb8f`  
		Last Modified: Thu, 13 Jul 2023 22:53:51 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb5aafaa1c1ada08d1342efaacdbbc72351ea5fa9ed825ec83c84c194a1793aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411f554cbcd46eb35b3ba4cd400a5e29132ded085f6ec4efaccaa6121a464db9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 23:11:18 GMT
COPY file:75a8428ab964e430ddc475b81bfe8411c8a1a8487d06f66b7b2be85ebca4c05f in /nats-server 
# Thu, 13 Jul 2023 23:11:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 23:11:19 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 23:11:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 23:11:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff35e5a1c81a5e14fcb0cddaf7b6bb7a86d01c91297fc204d6f59f81ab699f42`  
		Last Modified: Thu, 13 Jul 2023 23:11:55 GMT  
		Size: 4.7 MB (4694032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ddd8ff8791364717d428b048bce331ac51b1654fac486b5b5d64c7f9a6bd1`  
		Last Modified: Thu, 13 Jul 2023 23:11:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:63c26578744b038b074f43eb6c0b3958667480b48bfe2a74c675fa52295f6767
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109612796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7071df68a96690f5443acb6ef9a47cea84abc3e0dd4a92efaa064a3144b56ed2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Fri, 14 Jul 2023 00:03:16 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:a5074ddde966142308b669c647979e812040bd9a0280cfce51a983385df577ec in C:\nats-server.exe 
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:03:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bad9bf846d07362d8295a4479f8f2965dfb5934a9a032b335ce3cb086bdf7`  
		Last Modified: Fri, 14 Jul 2023 00:04:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b0789d7cd0ee38c3d2d6f0d8d4662e4e4f242055fa09752c571e9e0b12b25`  
		Last Modified: Fri, 14 Jul 2023 00:04:05 GMT  
		Size: 5.2 MB (5198141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7714f1d09ea353a9769c79f15345a77c802214a0d24c3ed987cf9bc90fa67933`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4710eb1eae23febe62cd19d1e08fda4c2417972b715e389b5078de0796c915f`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2187cbf833c204e29fc58f360a3c3c572ea7fe8140d088f10f16abeb6666d374`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f146e585d072cd21e48a1fd715a9e5ba5233a54652a5494c2efe8216b210ade`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:d6c6ae7df4a0c5f7aa5ec8035501b7a594d065216aa227265c89909a3c31df96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:89314efbfded0bd51e0b70966ebb7ad753245d6b680d4d999c25904838954a84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f3a7141f662bd0bab1c885fe0237733c81118613c3e2a1f041bf7d1cab81d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:29:16 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:29:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:29:18 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:29:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688e12de30012d849a08c4b3a056bf9462831be6349fedb514a9b943c5d3b038`  
		Last Modified: Thu, 13 Jul 2023 22:29:51 GMT  
		Size: 5.4 MB (5411416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcb04c9ced60dff0180f5da5e6f033545ec0a56faed6b9ea1f00c88a9ed3847`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086da10bd35caa5abb0061f428f619d8dd071a2fb7c760eead2ceb0bb7536e58`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c1cb16ffa939bd8f1601f657d500e3bd5c45005c28c448b68ec5b4b996fe430e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8318264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83f1c1fe0f07fee40eabe8e9253b5ac08578d588938045575e96a038b76964f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 21:49:19 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 21:49:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 21:49:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 21:49:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbd7a095ebb0cf47214d570aaa6e8beb1144d038098b2cc64526b8119b7a072`  
		Last Modified: Thu, 13 Jul 2023 21:49:46 GMT  
		Size: 5.2 MB (5173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc62259aed8a302b7cb52adf9701c763fb05897f5965d7873f6e27e88d4e07e`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3f8be8762d1cac21e849032e638a3ebf9bbb3957511eba1b7321783b83f23c`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:05b3018971114ff61d10e947e304f35c7bbc0abee425911c0fd58e23f7ae74e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8068141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4043b810630b65430ae04fb007b13c892d5e16ae40ea86b45712575d54868208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 22:36:15 GMT
ADD file:082f034323c559f3cb9feb6422c88b1ec8017f436d6109e238a5c5384a32a90a in / 
# Wed, 14 Jun 2023 22:36:15 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:52:54 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:52:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:52:57 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:52:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:52:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:633ba29fd335042456b6e2c073636f6fa30de56f1331c442914739b92a479974`  
		Last Modified: Wed, 14 Jun 2023 22:36:49 GMT  
		Size: 2.9 MB (2898508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b240facc4a312dbc41a0d9d2b5f34f26188edc082396407147566f4670a7bd`  
		Last Modified: Thu, 13 Jul 2023 22:53:30 GMT  
		Size: 5.2 MB (5168636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c49f0e2539269574bfe0565b74747b67dc174076c7d3b2b2c8064b2af71a80`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f69564b85401d79f11d3d0dd7775aa0dfa3d09c58f3daedcbe1f3fe676eea`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:aa93c00cb94a9cf48edbefb3fbb029b8d8187ccf4735f2eff181906d0e869854
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8309359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc0605733abd9e160812417dd92d5c4812e0640ef2a71568b2f2aed85eb6685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 23:11:00 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 23:11:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 23:11:03 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 23:11:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8d12353ca807b3f28a178dcf6ddfe80ac709c12b0da6364e48db96ab06e400`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 5.0 MB (4979109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7977030405ec12383b1b2033bc0fceb08f5c959b13d57ba18f74f11efee542ed`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041d1130902bd23c5b39754ecf01c19ed66a35c6e60064301df126b0f52259ad`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.18`

```console
$ docker pull nats@sha256:d6c6ae7df4a0c5f7aa5ec8035501b7a594d065216aa227265c89909a3c31df96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:89314efbfded0bd51e0b70966ebb7ad753245d6b680d4d999c25904838954a84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f3a7141f662bd0bab1c885fe0237733c81118613c3e2a1f041bf7d1cab81d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:29:16 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:29:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:29:18 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:29:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688e12de30012d849a08c4b3a056bf9462831be6349fedb514a9b943c5d3b038`  
		Last Modified: Thu, 13 Jul 2023 22:29:51 GMT  
		Size: 5.4 MB (5411416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcb04c9ced60dff0180f5da5e6f033545ec0a56faed6b9ea1f00c88a9ed3847`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086da10bd35caa5abb0061f428f619d8dd071a2fb7c760eead2ceb0bb7536e58`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:c1cb16ffa939bd8f1601f657d500e3bd5c45005c28c448b68ec5b4b996fe430e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8318264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83f1c1fe0f07fee40eabe8e9253b5ac08578d588938045575e96a038b76964f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 21:49:19 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 21:49:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 21:49:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 21:49:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbd7a095ebb0cf47214d570aaa6e8beb1144d038098b2cc64526b8119b7a072`  
		Last Modified: Thu, 13 Jul 2023 21:49:46 GMT  
		Size: 5.2 MB (5173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc62259aed8a302b7cb52adf9701c763fb05897f5965d7873f6e27e88d4e07e`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3f8be8762d1cac21e849032e638a3ebf9bbb3957511eba1b7321783b83f23c`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:05b3018971114ff61d10e947e304f35c7bbc0abee425911c0fd58e23f7ae74e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8068141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4043b810630b65430ae04fb007b13c892d5e16ae40ea86b45712575d54868208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 22:36:15 GMT
ADD file:082f034323c559f3cb9feb6422c88b1ec8017f436d6109e238a5c5384a32a90a in / 
# Wed, 14 Jun 2023 22:36:15 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:52:54 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:52:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:52:57 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:52:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:52:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:633ba29fd335042456b6e2c073636f6fa30de56f1331c442914739b92a479974`  
		Last Modified: Wed, 14 Jun 2023 22:36:49 GMT  
		Size: 2.9 MB (2898508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b240facc4a312dbc41a0d9d2b5f34f26188edc082396407147566f4670a7bd`  
		Last Modified: Thu, 13 Jul 2023 22:53:30 GMT  
		Size: 5.2 MB (5168636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c49f0e2539269574bfe0565b74747b67dc174076c7d3b2b2c8064b2af71a80`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f69564b85401d79f11d3d0dd7775aa0dfa3d09c58f3daedcbe1f3fe676eea`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:aa93c00cb94a9cf48edbefb3fbb029b8d8187ccf4735f2eff181906d0e869854
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8309359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc0605733abd9e160812417dd92d5c4812e0640ef2a71568b2f2aed85eb6685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 23:11:00 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 23:11:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 23:11:03 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 23:11:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8d12353ca807b3f28a178dcf6ddfe80ac709c12b0da6364e48db96ab06e400`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 5.0 MB (4979109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7977030405ec12383b1b2033bc0fceb08f5c959b13d57ba18f74f11efee542ed`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041d1130902bd23c5b39754ecf01c19ed66a35c6e60064301df126b0f52259ad`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:54beaa3c85e41593c8d7f235ac1ecea3c3dd2eeb63dc2f53e75a8094579ff7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:700a4b586eb96ff46eef5a949c50297d689f8b31d62ea1ca773dd6895c3f039d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5126531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5907f5a08f299f1dacf051a9fc09fb9189deb2b0dce45877975471766b706954`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:83ff3835bde68ad26982d2ccc535db9982a508facc29fdbcbbfb9675666fbdc6 in /nats-server 
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:29:32 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:29:33 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:29:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67e402a9bce54a5dfde340b14dba6b73ef42a3b94cb337301bf4374e77ec7040`  
		Last Modified: Thu, 13 Jul 2023 22:30:12 GMT  
		Size: 5.1 MB (5126023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a9f6e59497aefb2b8a64f61ee04f476641f2b25c8c62c37e5fdfaab68f8f7e`  
		Last Modified: Thu, 13 Jul 2023 22:30:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:6fd7bfb33bbf19e7ccb75c6ac3fcdc072b6120923fdb4e96e29492a5e7b89289
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4890101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d7fa51b81b0dcfb6ee49a1b74a5881dbf8163021afff101d2002b70686142a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:b5f9cb21b49e06d0ef4d044cf5d2fa6f64bbabb0cfb73701be4fa9d1e7c16c56 in /nats-server 
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 21:49:27 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:505fc4baba759223316e40a0109c61f162bb1d1acafb25bbc8e92b684cd58c5e`  
		Last Modified: Thu, 13 Jul 2023 21:50:07 GMT  
		Size: 4.9 MB (4889594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc06a01182930b7a494867f205f3a02b099200299bffa49031f3085b8952f64`  
		Last Modified: Thu, 13 Jul 2023 21:50:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ec4eab4197d5b340c7bcbbfda1e3bca6ac9874273362a95cb4f58157884759e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab94676f2d9fc59f778cd1526e8664a87db5a1b0741b2053991fb0fb00a2a16a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:53:11 GMT
COPY file:b1a666d296b7b01c216ccd9e1f03715958de83d192993bc8ab769d7998b1703f in /nats-server 
# Thu, 13 Jul 2023 22:53:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:53:12 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:775e6a1e06f337eb4fc74b89e37d008aac2e092d4bfd8d25f944b5b8d257bf8e`  
		Last Modified: Thu, 13 Jul 2023 22:53:52 GMT  
		Size: 4.9 MB (4880250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e8a9e7894a37f644a39457db86f9e94f7b92aadfeac1fd47ee846be3c7eb8f`  
		Last Modified: Thu, 13 Jul 2023 22:53:51 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb5aafaa1c1ada08d1342efaacdbbc72351ea5fa9ed825ec83c84c194a1793aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411f554cbcd46eb35b3ba4cd400a5e29132ded085f6ec4efaccaa6121a464db9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 23:11:18 GMT
COPY file:75a8428ab964e430ddc475b81bfe8411c8a1a8487d06f66b7b2be85ebca4c05f in /nats-server 
# Thu, 13 Jul 2023 23:11:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 23:11:19 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 23:11:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 23:11:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff35e5a1c81a5e14fcb0cddaf7b6bb7a86d01c91297fc204d6f59f81ab699f42`  
		Last Modified: Thu, 13 Jul 2023 23:11:55 GMT  
		Size: 4.7 MB (4694032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ddd8ff8791364717d428b048bce331ac51b1654fac486b5b5d64c7f9a6bd1`  
		Last Modified: Thu, 13 Jul 2023 23:11:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:bfff91215109e40d5a3d637ce8bc11a4bae8b3a555e2c79188bab93b2397278b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:63c26578744b038b074f43eb6c0b3958667480b48bfe2a74c675fa52295f6767
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109612796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7071df68a96690f5443acb6ef9a47cea84abc3e0dd4a92efaa064a3144b56ed2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Fri, 14 Jul 2023 00:03:16 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:a5074ddde966142308b669c647979e812040bd9a0280cfce51a983385df577ec in C:\nats-server.exe 
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:03:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bad9bf846d07362d8295a4479f8f2965dfb5934a9a032b335ce3cb086bdf7`  
		Last Modified: Fri, 14 Jul 2023 00:04:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b0789d7cd0ee38c3d2d6f0d8d4662e4e4f242055fa09752c571e9e0b12b25`  
		Last Modified: Fri, 14 Jul 2023 00:04:05 GMT  
		Size: 5.2 MB (5198141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7714f1d09ea353a9769c79f15345a77c802214a0d24c3ed987cf9bc90fa67933`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4710eb1eae23febe62cd19d1e08fda4c2417972b715e389b5078de0796c915f`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2187cbf833c204e29fc58f360a3c3c572ea7fe8140d088f10f16abeb6666d374`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f146e585d072cd21e48a1fd715a9e5ba5233a54652a5494c2efe8216b210ade`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:bfff91215109e40d5a3d637ce8bc11a4bae8b3a555e2c79188bab93b2397278b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:63c26578744b038b074f43eb6c0b3958667480b48bfe2a74c675fa52295f6767
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109612796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7071df68a96690f5443acb6ef9a47cea84abc3e0dd4a92efaa064a3144b56ed2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Fri, 14 Jul 2023 00:03:16 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:a5074ddde966142308b669c647979e812040bd9a0280cfce51a983385df577ec in C:\nats-server.exe 
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:03:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bad9bf846d07362d8295a4479f8f2965dfb5934a9a032b335ce3cb086bdf7`  
		Last Modified: Fri, 14 Jul 2023 00:04:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b0789d7cd0ee38c3d2d6f0d8d4662e4e4f242055fa09752c571e9e0b12b25`  
		Last Modified: Fri, 14 Jul 2023 00:04:05 GMT  
		Size: 5.2 MB (5198141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7714f1d09ea353a9769c79f15345a77c802214a0d24c3ed987cf9bc90fa67933`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4710eb1eae23febe62cd19d1e08fda4c2417972b715e389b5078de0796c915f`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2187cbf833c204e29fc58f360a3c3c572ea7fe8140d088f10f16abeb6666d374`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f146e585d072cd21e48a1fd715a9e5ba5233a54652a5494c2efe8216b210ade`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:54beaa3c85e41593c8d7f235ac1ecea3c3dd2eeb63dc2f53e75a8094579ff7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:700a4b586eb96ff46eef5a949c50297d689f8b31d62ea1ca773dd6895c3f039d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5126531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5907f5a08f299f1dacf051a9fc09fb9189deb2b0dce45877975471766b706954`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:83ff3835bde68ad26982d2ccc535db9982a508facc29fdbcbbfb9675666fbdc6 in /nats-server 
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:29:32 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:29:33 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:29:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67e402a9bce54a5dfde340b14dba6b73ef42a3b94cb337301bf4374e77ec7040`  
		Last Modified: Thu, 13 Jul 2023 22:30:12 GMT  
		Size: 5.1 MB (5126023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a9f6e59497aefb2b8a64f61ee04f476641f2b25c8c62c37e5fdfaab68f8f7e`  
		Last Modified: Thu, 13 Jul 2023 22:30:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:6fd7bfb33bbf19e7ccb75c6ac3fcdc072b6120923fdb4e96e29492a5e7b89289
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4890101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d7fa51b81b0dcfb6ee49a1b74a5881dbf8163021afff101d2002b70686142a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:b5f9cb21b49e06d0ef4d044cf5d2fa6f64bbabb0cfb73701be4fa9d1e7c16c56 in /nats-server 
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 21:49:27 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:505fc4baba759223316e40a0109c61f162bb1d1acafb25bbc8e92b684cd58c5e`  
		Last Modified: Thu, 13 Jul 2023 21:50:07 GMT  
		Size: 4.9 MB (4889594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc06a01182930b7a494867f205f3a02b099200299bffa49031f3085b8952f64`  
		Last Modified: Thu, 13 Jul 2023 21:50:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ec4eab4197d5b340c7bcbbfda1e3bca6ac9874273362a95cb4f58157884759e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab94676f2d9fc59f778cd1526e8664a87db5a1b0741b2053991fb0fb00a2a16a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:53:11 GMT
COPY file:b1a666d296b7b01c216ccd9e1f03715958de83d192993bc8ab769d7998b1703f in /nats-server 
# Thu, 13 Jul 2023 22:53:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:53:12 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:775e6a1e06f337eb4fc74b89e37d008aac2e092d4bfd8d25f944b5b8d257bf8e`  
		Last Modified: Thu, 13 Jul 2023 22:53:52 GMT  
		Size: 4.9 MB (4880250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e8a9e7894a37f644a39457db86f9e94f7b92aadfeac1fd47ee846be3c7eb8f`  
		Last Modified: Thu, 13 Jul 2023 22:53:51 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb5aafaa1c1ada08d1342efaacdbbc72351ea5fa9ed825ec83c84c194a1793aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411f554cbcd46eb35b3ba4cd400a5e29132ded085f6ec4efaccaa6121a464db9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 23:11:18 GMT
COPY file:75a8428ab964e430ddc475b81bfe8411c8a1a8487d06f66b7b2be85ebca4c05f in /nats-server 
# Thu, 13 Jul 2023 23:11:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 23:11:19 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 23:11:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 23:11:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff35e5a1c81a5e14fcb0cddaf7b6bb7a86d01c91297fc204d6f59f81ab699f42`  
		Last Modified: Thu, 13 Jul 2023 23:11:55 GMT  
		Size: 4.7 MB (4694032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ddd8ff8791364717d428b048bce331ac51b1654fac486b5b5d64c7f9a6bd1`  
		Last Modified: Thu, 13 Jul 2023 23:11:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:a8c2c33cbe248ffdf05cf1e29ce7026eefd132eb0cd15aff802e6031f5e1e6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:0fe2b83b4b22020701d93f9a59fb4fdbcfa157be7fb04e9288db445b76eaee4f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1945570306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fbdb411f499afb755df4b20ab636581d3aaed9c3a91c502ef50eeb34352001`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 22:38:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 14 Jul 2023 00:00:18 GMT
ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:00:19 GMT
ENV NATS_SERVER=2.9.20
# Fri, 14 Jul 2023 00:00:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.20/nats-server-v2.9.20-windows-amd64.zip
# Fri, 14 Jul 2023 00:00:21 GMT
ENV NATS_SERVER_SHASUM=6dd2f4648c3b5f7c0b0a2fc492ecd2263d3dfb22ea5cf2d0c018a82f0e912b35
# Fri, 14 Jul 2023 00:01:20 GMT
RUN Set-PSDebug -Trace 2
# Fri, 14 Jul 2023 00:02:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 14 Jul 2023 00:02:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:02:58 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:02:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b452db6d50a62b6e0e8dadb19715cfcf62cf73e54b5d3bac96621c1093673c`  
		Last Modified: Thu, 13 Jul 2023 23:25:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f8ca4b8d322e27c827c0ba667217bc04a39b69f5f483d5f2f9726e6d42522e`  
		Last Modified: Fri, 14 Jul 2023 00:03:50 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f33781e88272c93d82ac65b1dfc5a07ce75d4e8e04e8561f158831356e7fea4`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe631d552a5255bffd0e5aeec249b1684a7e8c75fe30b185e199fbfdecedfae`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb256a4292680f56d2092582b633530842c97891e2f740aa78403b240999c630`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb7d2753eb8c81851f9e3869d39a0947479d1411590331b94108e9cb2bef9e5`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 226.1 KB (226138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c118d6802e5d239c3513560bc388331e2aaf975937a7aa8625dc85e54015becc`  
		Last Modified: Fri, 14 Jul 2023 00:03:47 GMT  
		Size: 5.6 MB (5641748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689840dc0e8e1fb392e9005f0603c05fb29100193e9d6b8528369ce241b81dee`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5788a19b6a5a361435ec99a16308610c901b5452d1281dc9bdab065485a4ad1`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa4bedb48935e18d91878ff81f1b80d8e4ff1149700225914c54b1a6b83933c`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f710347dc06495d6660dfd5cbc8d9c4f5f4555d2ac5e26adc76ee8de42bc75ca`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:a8c2c33cbe248ffdf05cf1e29ce7026eefd132eb0cd15aff802e6031f5e1e6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:0fe2b83b4b22020701d93f9a59fb4fdbcfa157be7fb04e9288db445b76eaee4f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1945570306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fbdb411f499afb755df4b20ab636581d3aaed9c3a91c502ef50eeb34352001`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 22:38:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 14 Jul 2023 00:00:18 GMT
ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:00:19 GMT
ENV NATS_SERVER=2.9.20
# Fri, 14 Jul 2023 00:00:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.20/nats-server-v2.9.20-windows-amd64.zip
# Fri, 14 Jul 2023 00:00:21 GMT
ENV NATS_SERVER_SHASUM=6dd2f4648c3b5f7c0b0a2fc492ecd2263d3dfb22ea5cf2d0c018a82f0e912b35
# Fri, 14 Jul 2023 00:01:20 GMT
RUN Set-PSDebug -Trace 2
# Fri, 14 Jul 2023 00:02:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 14 Jul 2023 00:02:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:02:58 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:02:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b452db6d50a62b6e0e8dadb19715cfcf62cf73e54b5d3bac96621c1093673c`  
		Last Modified: Thu, 13 Jul 2023 23:25:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f8ca4b8d322e27c827c0ba667217bc04a39b69f5f483d5f2f9726e6d42522e`  
		Last Modified: Fri, 14 Jul 2023 00:03:50 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f33781e88272c93d82ac65b1dfc5a07ce75d4e8e04e8561f158831356e7fea4`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe631d552a5255bffd0e5aeec249b1684a7e8c75fe30b185e199fbfdecedfae`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb256a4292680f56d2092582b633530842c97891e2f740aa78403b240999c630`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb7d2753eb8c81851f9e3869d39a0947479d1411590331b94108e9cb2bef9e5`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 226.1 KB (226138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c118d6802e5d239c3513560bc388331e2aaf975937a7aa8625dc85e54015becc`  
		Last Modified: Fri, 14 Jul 2023 00:03:47 GMT  
		Size: 5.6 MB (5641748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689840dc0e8e1fb392e9005f0603c05fb29100193e9d6b8528369ce241b81dee`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5788a19b6a5a361435ec99a16308610c901b5452d1281dc9bdab065485a4ad1`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa4bedb48935e18d91878ff81f1b80d8e4ff1149700225914c54b1a6b83933c`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f710347dc06495d6660dfd5cbc8d9c4f5f4555d2ac5e26adc76ee8de42bc75ca`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.20`

```console
$ docker pull nats@sha256:8e0fb53c305217c0f29f21e8176fce1f4f11648c96543f0970666d8596e2d69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4645; amd64

### `nats:2.9.20` - linux; amd64

```console
$ docker pull nats@sha256:700a4b586eb96ff46eef5a949c50297d689f8b31d62ea1ca773dd6895c3f039d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5126531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5907f5a08f299f1dacf051a9fc09fb9189deb2b0dce45877975471766b706954`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:83ff3835bde68ad26982d2ccc535db9982a508facc29fdbcbbfb9675666fbdc6 in /nats-server 
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:29:32 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:29:33 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:29:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67e402a9bce54a5dfde340b14dba6b73ef42a3b94cb337301bf4374e77ec7040`  
		Last Modified: Thu, 13 Jul 2023 22:30:12 GMT  
		Size: 5.1 MB (5126023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a9f6e59497aefb2b8a64f61ee04f476641f2b25c8c62c37e5fdfaab68f8f7e`  
		Last Modified: Thu, 13 Jul 2023 22:30:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:6fd7bfb33bbf19e7ccb75c6ac3fcdc072b6120923fdb4e96e29492a5e7b89289
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4890101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d7fa51b81b0dcfb6ee49a1b74a5881dbf8163021afff101d2002b70686142a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:b5f9cb21b49e06d0ef4d044cf5d2fa6f64bbabb0cfb73701be4fa9d1e7c16c56 in /nats-server 
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 21:49:27 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:505fc4baba759223316e40a0109c61f162bb1d1acafb25bbc8e92b684cd58c5e`  
		Last Modified: Thu, 13 Jul 2023 21:50:07 GMT  
		Size: 4.9 MB (4889594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc06a01182930b7a494867f205f3a02b099200299bffa49031f3085b8952f64`  
		Last Modified: Thu, 13 Jul 2023 21:50:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ec4eab4197d5b340c7bcbbfda1e3bca6ac9874273362a95cb4f58157884759e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab94676f2d9fc59f778cd1526e8664a87db5a1b0741b2053991fb0fb00a2a16a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:53:11 GMT
COPY file:b1a666d296b7b01c216ccd9e1f03715958de83d192993bc8ab769d7998b1703f in /nats-server 
# Thu, 13 Jul 2023 22:53:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:53:12 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:775e6a1e06f337eb4fc74b89e37d008aac2e092d4bfd8d25f944b5b8d257bf8e`  
		Last Modified: Thu, 13 Jul 2023 22:53:52 GMT  
		Size: 4.9 MB (4880250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e8a9e7894a37f644a39457db86f9e94f7b92aadfeac1fd47ee846be3c7eb8f`  
		Last Modified: Thu, 13 Jul 2023 22:53:51 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb5aafaa1c1ada08d1342efaacdbbc72351ea5fa9ed825ec83c84c194a1793aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411f554cbcd46eb35b3ba4cd400a5e29132ded085f6ec4efaccaa6121a464db9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 23:11:18 GMT
COPY file:75a8428ab964e430ddc475b81bfe8411c8a1a8487d06f66b7b2be85ebca4c05f in /nats-server 
# Thu, 13 Jul 2023 23:11:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 23:11:19 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 23:11:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 23:11:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff35e5a1c81a5e14fcb0cddaf7b6bb7a86d01c91297fc204d6f59f81ab699f42`  
		Last Modified: Thu, 13 Jul 2023 23:11:55 GMT  
		Size: 4.7 MB (4694032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ddd8ff8791364717d428b048bce331ac51b1654fac486b5b5d64c7f9a6bd1`  
		Last Modified: Thu, 13 Jul 2023 23:11:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.20` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:63c26578744b038b074f43eb6c0b3958667480b48bfe2a74c675fa52295f6767
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109612796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7071df68a96690f5443acb6ef9a47cea84abc3e0dd4a92efaa064a3144b56ed2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Fri, 14 Jul 2023 00:03:16 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:a5074ddde966142308b669c647979e812040bd9a0280cfce51a983385df577ec in C:\nats-server.exe 
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:03:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bad9bf846d07362d8295a4479f8f2965dfb5934a9a032b335ce3cb086bdf7`  
		Last Modified: Fri, 14 Jul 2023 00:04:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b0789d7cd0ee38c3d2d6f0d8d4662e4e4f242055fa09752c571e9e0b12b25`  
		Last Modified: Fri, 14 Jul 2023 00:04:05 GMT  
		Size: 5.2 MB (5198141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7714f1d09ea353a9769c79f15345a77c802214a0d24c3ed987cf9bc90fa67933`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4710eb1eae23febe62cd19d1e08fda4c2417972b715e389b5078de0796c915f`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2187cbf833c204e29fc58f360a3c3c572ea7fe8140d088f10f16abeb6666d374`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f146e585d072cd21e48a1fd715a9e5ba5233a54652a5494c2efe8216b210ade`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.20-alpine`

```console
$ docker pull nats@sha256:d6c6ae7df4a0c5f7aa5ec8035501b7a594d065216aa227265c89909a3c31df96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.20-alpine` - linux; amd64

```console
$ docker pull nats@sha256:89314efbfded0bd51e0b70966ebb7ad753245d6b680d4d999c25904838954a84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f3a7141f662bd0bab1c885fe0237733c81118613c3e2a1f041bf7d1cab81d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:29:16 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:29:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:29:18 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:29:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688e12de30012d849a08c4b3a056bf9462831be6349fedb514a9b943c5d3b038`  
		Last Modified: Thu, 13 Jul 2023 22:29:51 GMT  
		Size: 5.4 MB (5411416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcb04c9ced60dff0180f5da5e6f033545ec0a56faed6b9ea1f00c88a9ed3847`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086da10bd35caa5abb0061f428f619d8dd071a2fb7c760eead2ceb0bb7536e58`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.20-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c1cb16ffa939bd8f1601f657d500e3bd5c45005c28c448b68ec5b4b996fe430e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8318264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83f1c1fe0f07fee40eabe8e9253b5ac08578d588938045575e96a038b76964f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 21:49:19 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 21:49:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 21:49:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 21:49:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbd7a095ebb0cf47214d570aaa6e8beb1144d038098b2cc64526b8119b7a072`  
		Last Modified: Thu, 13 Jul 2023 21:49:46 GMT  
		Size: 5.2 MB (5173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc62259aed8a302b7cb52adf9701c763fb05897f5965d7873f6e27e88d4e07e`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3f8be8762d1cac21e849032e638a3ebf9bbb3957511eba1b7321783b83f23c`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.20-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:05b3018971114ff61d10e947e304f35c7bbc0abee425911c0fd58e23f7ae74e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8068141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4043b810630b65430ae04fb007b13c892d5e16ae40ea86b45712575d54868208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 22:36:15 GMT
ADD file:082f034323c559f3cb9feb6422c88b1ec8017f436d6109e238a5c5384a32a90a in / 
# Wed, 14 Jun 2023 22:36:15 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:52:54 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:52:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:52:57 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:52:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:52:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:633ba29fd335042456b6e2c073636f6fa30de56f1331c442914739b92a479974`  
		Last Modified: Wed, 14 Jun 2023 22:36:49 GMT  
		Size: 2.9 MB (2898508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b240facc4a312dbc41a0d9d2b5f34f26188edc082396407147566f4670a7bd`  
		Last Modified: Thu, 13 Jul 2023 22:53:30 GMT  
		Size: 5.2 MB (5168636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c49f0e2539269574bfe0565b74747b67dc174076c7d3b2b2c8064b2af71a80`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f69564b85401d79f11d3d0dd7775aa0dfa3d09c58f3daedcbe1f3fe676eea`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.20-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:aa93c00cb94a9cf48edbefb3fbb029b8d8187ccf4735f2eff181906d0e869854
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8309359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc0605733abd9e160812417dd92d5c4812e0640ef2a71568b2f2aed85eb6685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 23:11:00 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 23:11:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 23:11:03 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 23:11:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8d12353ca807b3f28a178dcf6ddfe80ac709c12b0da6364e48db96ab06e400`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 5.0 MB (4979109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7977030405ec12383b1b2033bc0fceb08f5c959b13d57ba18f74f11efee542ed`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041d1130902bd23c5b39754ecf01c19ed66a35c6e60064301df126b0f52259ad`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.20-alpine3.18`

```console
$ docker pull nats@sha256:d6c6ae7df4a0c5f7aa5ec8035501b7a594d065216aa227265c89909a3c31df96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.20-alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:89314efbfded0bd51e0b70966ebb7ad753245d6b680d4d999c25904838954a84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f3a7141f662bd0bab1c885fe0237733c81118613c3e2a1f041bf7d1cab81d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:29:16 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:29:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:29:18 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:29:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688e12de30012d849a08c4b3a056bf9462831be6349fedb514a9b943c5d3b038`  
		Last Modified: Thu, 13 Jul 2023 22:29:51 GMT  
		Size: 5.4 MB (5411416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcb04c9ced60dff0180f5da5e6f033545ec0a56faed6b9ea1f00c88a9ed3847`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086da10bd35caa5abb0061f428f619d8dd071a2fb7c760eead2ceb0bb7536e58`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.20-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:c1cb16ffa939bd8f1601f657d500e3bd5c45005c28c448b68ec5b4b996fe430e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8318264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83f1c1fe0f07fee40eabe8e9253b5ac08578d588938045575e96a038b76964f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 21:49:19 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 21:49:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 21:49:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 21:49:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbd7a095ebb0cf47214d570aaa6e8beb1144d038098b2cc64526b8119b7a072`  
		Last Modified: Thu, 13 Jul 2023 21:49:46 GMT  
		Size: 5.2 MB (5173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc62259aed8a302b7cb52adf9701c763fb05897f5965d7873f6e27e88d4e07e`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3f8be8762d1cac21e849032e638a3ebf9bbb3957511eba1b7321783b83f23c`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.20-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:05b3018971114ff61d10e947e304f35c7bbc0abee425911c0fd58e23f7ae74e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8068141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4043b810630b65430ae04fb007b13c892d5e16ae40ea86b45712575d54868208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 22:36:15 GMT
ADD file:082f034323c559f3cb9feb6422c88b1ec8017f436d6109e238a5c5384a32a90a in / 
# Wed, 14 Jun 2023 22:36:15 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:52:54 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:52:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:52:57 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:52:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:52:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:633ba29fd335042456b6e2c073636f6fa30de56f1331c442914739b92a479974`  
		Last Modified: Wed, 14 Jun 2023 22:36:49 GMT  
		Size: 2.9 MB (2898508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b240facc4a312dbc41a0d9d2b5f34f26188edc082396407147566f4670a7bd`  
		Last Modified: Thu, 13 Jul 2023 22:53:30 GMT  
		Size: 5.2 MB (5168636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c49f0e2539269574bfe0565b74747b67dc174076c7d3b2b2c8064b2af71a80`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f69564b85401d79f11d3d0dd7775aa0dfa3d09c58f3daedcbe1f3fe676eea`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.20-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:aa93c00cb94a9cf48edbefb3fbb029b8d8187ccf4735f2eff181906d0e869854
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8309359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc0605733abd9e160812417dd92d5c4812e0640ef2a71568b2f2aed85eb6685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 23:11:00 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 23:11:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 23:11:03 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 23:11:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8d12353ca807b3f28a178dcf6ddfe80ac709c12b0da6364e48db96ab06e400`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 5.0 MB (4979109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7977030405ec12383b1b2033bc0fceb08f5c959b13d57ba18f74f11efee542ed`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041d1130902bd23c5b39754ecf01c19ed66a35c6e60064301df126b0f52259ad`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.20-linux`

```console
$ docker pull nats@sha256:54beaa3c85e41593c8d7f235ac1ecea3c3dd2eeb63dc2f53e75a8094579ff7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.20-linux` - linux; amd64

```console
$ docker pull nats@sha256:700a4b586eb96ff46eef5a949c50297d689f8b31d62ea1ca773dd6895c3f039d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5126531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5907f5a08f299f1dacf051a9fc09fb9189deb2b0dce45877975471766b706954`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:83ff3835bde68ad26982d2ccc535db9982a508facc29fdbcbbfb9675666fbdc6 in /nats-server 
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:29:32 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:29:33 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:29:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67e402a9bce54a5dfde340b14dba6b73ef42a3b94cb337301bf4374e77ec7040`  
		Last Modified: Thu, 13 Jul 2023 22:30:12 GMT  
		Size: 5.1 MB (5126023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a9f6e59497aefb2b8a64f61ee04f476641f2b25c8c62c37e5fdfaab68f8f7e`  
		Last Modified: Thu, 13 Jul 2023 22:30:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.20-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:6fd7bfb33bbf19e7ccb75c6ac3fcdc072b6120923fdb4e96e29492a5e7b89289
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4890101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d7fa51b81b0dcfb6ee49a1b74a5881dbf8163021afff101d2002b70686142a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:b5f9cb21b49e06d0ef4d044cf5d2fa6f64bbabb0cfb73701be4fa9d1e7c16c56 in /nats-server 
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 21:49:27 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:505fc4baba759223316e40a0109c61f162bb1d1acafb25bbc8e92b684cd58c5e`  
		Last Modified: Thu, 13 Jul 2023 21:50:07 GMT  
		Size: 4.9 MB (4889594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc06a01182930b7a494867f205f3a02b099200299bffa49031f3085b8952f64`  
		Last Modified: Thu, 13 Jul 2023 21:50:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.20-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ec4eab4197d5b340c7bcbbfda1e3bca6ac9874273362a95cb4f58157884759e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab94676f2d9fc59f778cd1526e8664a87db5a1b0741b2053991fb0fb00a2a16a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:53:11 GMT
COPY file:b1a666d296b7b01c216ccd9e1f03715958de83d192993bc8ab769d7998b1703f in /nats-server 
# Thu, 13 Jul 2023 22:53:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:53:12 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:775e6a1e06f337eb4fc74b89e37d008aac2e092d4bfd8d25f944b5b8d257bf8e`  
		Last Modified: Thu, 13 Jul 2023 22:53:52 GMT  
		Size: 4.9 MB (4880250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e8a9e7894a37f644a39457db86f9e94f7b92aadfeac1fd47ee846be3c7eb8f`  
		Last Modified: Thu, 13 Jul 2023 22:53:51 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.20-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb5aafaa1c1ada08d1342efaacdbbc72351ea5fa9ed825ec83c84c194a1793aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411f554cbcd46eb35b3ba4cd400a5e29132ded085f6ec4efaccaa6121a464db9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 23:11:18 GMT
COPY file:75a8428ab964e430ddc475b81bfe8411c8a1a8487d06f66b7b2be85ebca4c05f in /nats-server 
# Thu, 13 Jul 2023 23:11:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 23:11:19 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 23:11:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 23:11:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff35e5a1c81a5e14fcb0cddaf7b6bb7a86d01c91297fc204d6f59f81ab699f42`  
		Last Modified: Thu, 13 Jul 2023 23:11:55 GMT  
		Size: 4.7 MB (4694032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ddd8ff8791364717d428b048bce331ac51b1654fac486b5b5d64c7f9a6bd1`  
		Last Modified: Thu, 13 Jul 2023 23:11:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.20-nanoserver`

```console
$ docker pull nats@sha256:bfff91215109e40d5a3d637ce8bc11a4bae8b3a555e2c79188bab93b2397278b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:2.9.20-nanoserver` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:63c26578744b038b074f43eb6c0b3958667480b48bfe2a74c675fa52295f6767
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109612796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7071df68a96690f5443acb6ef9a47cea84abc3e0dd4a92efaa064a3144b56ed2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Fri, 14 Jul 2023 00:03:16 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:a5074ddde966142308b669c647979e812040bd9a0280cfce51a983385df577ec in C:\nats-server.exe 
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:03:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bad9bf846d07362d8295a4479f8f2965dfb5934a9a032b335ce3cb086bdf7`  
		Last Modified: Fri, 14 Jul 2023 00:04:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b0789d7cd0ee38c3d2d6f0d8d4662e4e4f242055fa09752c571e9e0b12b25`  
		Last Modified: Fri, 14 Jul 2023 00:04:05 GMT  
		Size: 5.2 MB (5198141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7714f1d09ea353a9769c79f15345a77c802214a0d24c3ed987cf9bc90fa67933`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4710eb1eae23febe62cd19d1e08fda4c2417972b715e389b5078de0796c915f`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2187cbf833c204e29fc58f360a3c3c572ea7fe8140d088f10f16abeb6666d374`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f146e585d072cd21e48a1fd715a9e5ba5233a54652a5494c2efe8216b210ade`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.20-nanoserver-1809`

```console
$ docker pull nats@sha256:bfff91215109e40d5a3d637ce8bc11a4bae8b3a555e2c79188bab93b2397278b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:2.9.20-nanoserver-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:63c26578744b038b074f43eb6c0b3958667480b48bfe2a74c675fa52295f6767
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109612796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7071df68a96690f5443acb6ef9a47cea84abc3e0dd4a92efaa064a3144b56ed2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Fri, 14 Jul 2023 00:03:16 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:a5074ddde966142308b669c647979e812040bd9a0280cfce51a983385df577ec in C:\nats-server.exe 
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:03:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bad9bf846d07362d8295a4479f8f2965dfb5934a9a032b335ce3cb086bdf7`  
		Last Modified: Fri, 14 Jul 2023 00:04:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b0789d7cd0ee38c3d2d6f0d8d4662e4e4f242055fa09752c571e9e0b12b25`  
		Last Modified: Fri, 14 Jul 2023 00:04:05 GMT  
		Size: 5.2 MB (5198141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7714f1d09ea353a9769c79f15345a77c802214a0d24c3ed987cf9bc90fa67933`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4710eb1eae23febe62cd19d1e08fda4c2417972b715e389b5078de0796c915f`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2187cbf833c204e29fc58f360a3c3c572ea7fe8140d088f10f16abeb6666d374`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f146e585d072cd21e48a1fd715a9e5ba5233a54652a5494c2efe8216b210ade`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.20-scratch`

```console
$ docker pull nats@sha256:54beaa3c85e41593c8d7f235ac1ecea3c3dd2eeb63dc2f53e75a8094579ff7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.20-scratch` - linux; amd64

```console
$ docker pull nats@sha256:700a4b586eb96ff46eef5a949c50297d689f8b31d62ea1ca773dd6895c3f039d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5126531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5907f5a08f299f1dacf051a9fc09fb9189deb2b0dce45877975471766b706954`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:83ff3835bde68ad26982d2ccc535db9982a508facc29fdbcbbfb9675666fbdc6 in /nats-server 
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:29:32 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:29:33 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:29:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67e402a9bce54a5dfde340b14dba6b73ef42a3b94cb337301bf4374e77ec7040`  
		Last Modified: Thu, 13 Jul 2023 22:30:12 GMT  
		Size: 5.1 MB (5126023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a9f6e59497aefb2b8a64f61ee04f476641f2b25c8c62c37e5fdfaab68f8f7e`  
		Last Modified: Thu, 13 Jul 2023 22:30:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.20-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:6fd7bfb33bbf19e7ccb75c6ac3fcdc072b6120923fdb4e96e29492a5e7b89289
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4890101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d7fa51b81b0dcfb6ee49a1b74a5881dbf8163021afff101d2002b70686142a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:b5f9cb21b49e06d0ef4d044cf5d2fa6f64bbabb0cfb73701be4fa9d1e7c16c56 in /nats-server 
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 21:49:27 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:505fc4baba759223316e40a0109c61f162bb1d1acafb25bbc8e92b684cd58c5e`  
		Last Modified: Thu, 13 Jul 2023 21:50:07 GMT  
		Size: 4.9 MB (4889594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc06a01182930b7a494867f205f3a02b099200299bffa49031f3085b8952f64`  
		Last Modified: Thu, 13 Jul 2023 21:50:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.20-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ec4eab4197d5b340c7bcbbfda1e3bca6ac9874273362a95cb4f58157884759e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab94676f2d9fc59f778cd1526e8664a87db5a1b0741b2053991fb0fb00a2a16a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:53:11 GMT
COPY file:b1a666d296b7b01c216ccd9e1f03715958de83d192993bc8ab769d7998b1703f in /nats-server 
# Thu, 13 Jul 2023 22:53:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:53:12 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:775e6a1e06f337eb4fc74b89e37d008aac2e092d4bfd8d25f944b5b8d257bf8e`  
		Last Modified: Thu, 13 Jul 2023 22:53:52 GMT  
		Size: 4.9 MB (4880250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e8a9e7894a37f644a39457db86f9e94f7b92aadfeac1fd47ee846be3c7eb8f`  
		Last Modified: Thu, 13 Jul 2023 22:53:51 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.20-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb5aafaa1c1ada08d1342efaacdbbc72351ea5fa9ed825ec83c84c194a1793aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411f554cbcd46eb35b3ba4cd400a5e29132ded085f6ec4efaccaa6121a464db9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 23:11:18 GMT
COPY file:75a8428ab964e430ddc475b81bfe8411c8a1a8487d06f66b7b2be85ebca4c05f in /nats-server 
# Thu, 13 Jul 2023 23:11:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 23:11:19 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 23:11:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 23:11:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff35e5a1c81a5e14fcb0cddaf7b6bb7a86d01c91297fc204d6f59f81ab699f42`  
		Last Modified: Thu, 13 Jul 2023 23:11:55 GMT  
		Size: 4.7 MB (4694032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ddd8ff8791364717d428b048bce331ac51b1654fac486b5b5d64c7f9a6bd1`  
		Last Modified: Thu, 13 Jul 2023 23:11:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.20-windowsservercore`

```console
$ docker pull nats@sha256:a8c2c33cbe248ffdf05cf1e29ce7026eefd132eb0cd15aff802e6031f5e1e6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:2.9.20-windowsservercore` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:0fe2b83b4b22020701d93f9a59fb4fdbcfa157be7fb04e9288db445b76eaee4f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1945570306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fbdb411f499afb755df4b20ab636581d3aaed9c3a91c502ef50eeb34352001`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 22:38:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 14 Jul 2023 00:00:18 GMT
ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:00:19 GMT
ENV NATS_SERVER=2.9.20
# Fri, 14 Jul 2023 00:00:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.20/nats-server-v2.9.20-windows-amd64.zip
# Fri, 14 Jul 2023 00:00:21 GMT
ENV NATS_SERVER_SHASUM=6dd2f4648c3b5f7c0b0a2fc492ecd2263d3dfb22ea5cf2d0c018a82f0e912b35
# Fri, 14 Jul 2023 00:01:20 GMT
RUN Set-PSDebug -Trace 2
# Fri, 14 Jul 2023 00:02:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 14 Jul 2023 00:02:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:02:58 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:02:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b452db6d50a62b6e0e8dadb19715cfcf62cf73e54b5d3bac96621c1093673c`  
		Last Modified: Thu, 13 Jul 2023 23:25:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f8ca4b8d322e27c827c0ba667217bc04a39b69f5f483d5f2f9726e6d42522e`  
		Last Modified: Fri, 14 Jul 2023 00:03:50 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f33781e88272c93d82ac65b1dfc5a07ce75d4e8e04e8561f158831356e7fea4`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe631d552a5255bffd0e5aeec249b1684a7e8c75fe30b185e199fbfdecedfae`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb256a4292680f56d2092582b633530842c97891e2f740aa78403b240999c630`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb7d2753eb8c81851f9e3869d39a0947479d1411590331b94108e9cb2bef9e5`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 226.1 KB (226138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c118d6802e5d239c3513560bc388331e2aaf975937a7aa8625dc85e54015becc`  
		Last Modified: Fri, 14 Jul 2023 00:03:47 GMT  
		Size: 5.6 MB (5641748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689840dc0e8e1fb392e9005f0603c05fb29100193e9d6b8528369ce241b81dee`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5788a19b6a5a361435ec99a16308610c901b5452d1281dc9bdab065485a4ad1`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa4bedb48935e18d91878ff81f1b80d8e4ff1149700225914c54b1a6b83933c`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f710347dc06495d6660dfd5cbc8d9c4f5f4555d2ac5e26adc76ee8de42bc75ca`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.20-windowsservercore-1809`

```console
$ docker pull nats@sha256:a8c2c33cbe248ffdf05cf1e29ce7026eefd132eb0cd15aff802e6031f5e1e6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:2.9.20-windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:0fe2b83b4b22020701d93f9a59fb4fdbcfa157be7fb04e9288db445b76eaee4f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1945570306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fbdb411f499afb755df4b20ab636581d3aaed9c3a91c502ef50eeb34352001`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 22:38:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 14 Jul 2023 00:00:18 GMT
ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:00:19 GMT
ENV NATS_SERVER=2.9.20
# Fri, 14 Jul 2023 00:00:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.20/nats-server-v2.9.20-windows-amd64.zip
# Fri, 14 Jul 2023 00:00:21 GMT
ENV NATS_SERVER_SHASUM=6dd2f4648c3b5f7c0b0a2fc492ecd2263d3dfb22ea5cf2d0c018a82f0e912b35
# Fri, 14 Jul 2023 00:01:20 GMT
RUN Set-PSDebug -Trace 2
# Fri, 14 Jul 2023 00:02:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 14 Jul 2023 00:02:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:02:58 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:02:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b452db6d50a62b6e0e8dadb19715cfcf62cf73e54b5d3bac96621c1093673c`  
		Last Modified: Thu, 13 Jul 2023 23:25:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f8ca4b8d322e27c827c0ba667217bc04a39b69f5f483d5f2f9726e6d42522e`  
		Last Modified: Fri, 14 Jul 2023 00:03:50 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f33781e88272c93d82ac65b1dfc5a07ce75d4e8e04e8561f158831356e7fea4`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe631d552a5255bffd0e5aeec249b1684a7e8c75fe30b185e199fbfdecedfae`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb256a4292680f56d2092582b633530842c97891e2f740aa78403b240999c630`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb7d2753eb8c81851f9e3869d39a0947479d1411590331b94108e9cb2bef9e5`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 226.1 KB (226138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c118d6802e5d239c3513560bc388331e2aaf975937a7aa8625dc85e54015becc`  
		Last Modified: Fri, 14 Jul 2023 00:03:47 GMT  
		Size: 5.6 MB (5641748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689840dc0e8e1fb392e9005f0603c05fb29100193e9d6b8528369ce241b81dee`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5788a19b6a5a361435ec99a16308610c901b5452d1281dc9bdab065485a4ad1`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa4bedb48935e18d91878ff81f1b80d8e4ff1149700225914c54b1a6b83933c`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f710347dc06495d6660dfd5cbc8d9c4f5f4555d2ac5e26adc76ee8de42bc75ca`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:d6c6ae7df4a0c5f7aa5ec8035501b7a594d065216aa227265c89909a3c31df96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:89314efbfded0bd51e0b70966ebb7ad753245d6b680d4d999c25904838954a84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f3a7141f662bd0bab1c885fe0237733c81118613c3e2a1f041bf7d1cab81d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:29:16 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:29:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:29:18 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:29:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688e12de30012d849a08c4b3a056bf9462831be6349fedb514a9b943c5d3b038`  
		Last Modified: Thu, 13 Jul 2023 22:29:51 GMT  
		Size: 5.4 MB (5411416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcb04c9ced60dff0180f5da5e6f033545ec0a56faed6b9ea1f00c88a9ed3847`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086da10bd35caa5abb0061f428f619d8dd071a2fb7c760eead2ceb0bb7536e58`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c1cb16ffa939bd8f1601f657d500e3bd5c45005c28c448b68ec5b4b996fe430e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8318264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83f1c1fe0f07fee40eabe8e9253b5ac08578d588938045575e96a038b76964f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 21:49:19 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 21:49:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 21:49:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 21:49:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbd7a095ebb0cf47214d570aaa6e8beb1144d038098b2cc64526b8119b7a072`  
		Last Modified: Thu, 13 Jul 2023 21:49:46 GMT  
		Size: 5.2 MB (5173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc62259aed8a302b7cb52adf9701c763fb05897f5965d7873f6e27e88d4e07e`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3f8be8762d1cac21e849032e638a3ebf9bbb3957511eba1b7321783b83f23c`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:05b3018971114ff61d10e947e304f35c7bbc0abee425911c0fd58e23f7ae74e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8068141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4043b810630b65430ae04fb007b13c892d5e16ae40ea86b45712575d54868208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 22:36:15 GMT
ADD file:082f034323c559f3cb9feb6422c88b1ec8017f436d6109e238a5c5384a32a90a in / 
# Wed, 14 Jun 2023 22:36:15 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:52:54 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:52:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:52:57 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:52:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:52:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:633ba29fd335042456b6e2c073636f6fa30de56f1331c442914739b92a479974`  
		Last Modified: Wed, 14 Jun 2023 22:36:49 GMT  
		Size: 2.9 MB (2898508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b240facc4a312dbc41a0d9d2b5f34f26188edc082396407147566f4670a7bd`  
		Last Modified: Thu, 13 Jul 2023 22:53:30 GMT  
		Size: 5.2 MB (5168636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c49f0e2539269574bfe0565b74747b67dc174076c7d3b2b2c8064b2af71a80`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f69564b85401d79f11d3d0dd7775aa0dfa3d09c58f3daedcbe1f3fe676eea`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:aa93c00cb94a9cf48edbefb3fbb029b8d8187ccf4735f2eff181906d0e869854
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8309359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc0605733abd9e160812417dd92d5c4812e0640ef2a71568b2f2aed85eb6685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 23:11:00 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 23:11:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 23:11:03 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 23:11:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8d12353ca807b3f28a178dcf6ddfe80ac709c12b0da6364e48db96ab06e400`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 5.0 MB (4979109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7977030405ec12383b1b2033bc0fceb08f5c959b13d57ba18f74f11efee542ed`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041d1130902bd23c5b39754ecf01c19ed66a35c6e60064301df126b0f52259ad`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.18`

```console
$ docker pull nats@sha256:d6c6ae7df4a0c5f7aa5ec8035501b7a594d065216aa227265c89909a3c31df96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.18` - linux; amd64

```console
$ docker pull nats@sha256:89314efbfded0bd51e0b70966ebb7ad753245d6b680d4d999c25904838954a84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5f3a7141f662bd0bab1c885fe0237733c81118613c3e2a1f041bf7d1cab81d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:29:16 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:29:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:29:18 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:29:18 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:29:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688e12de30012d849a08c4b3a056bf9462831be6349fedb514a9b943c5d3b038`  
		Last Modified: Thu, 13 Jul 2023 22:29:51 GMT  
		Size: 5.4 MB (5411416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcb04c9ced60dff0180f5da5e6f033545ec0a56faed6b9ea1f00c88a9ed3847`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086da10bd35caa5abb0061f428f619d8dd071a2fb7c760eead2ceb0bb7536e58`  
		Last Modified: Thu, 13 Jul 2023 22:29:50 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.18` - linux; arm variant v6

```console
$ docker pull nats@sha256:c1cb16ffa939bd8f1601f657d500e3bd5c45005c28c448b68ec5b4b996fe430e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8318264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83f1c1fe0f07fee40eabe8e9253b5ac08578d588938045575e96a038b76964f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 21:49:19 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 21:49:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 21:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 21:49:22 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 21:49:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbd7a095ebb0cf47214d570aaa6e8beb1144d038098b2cc64526b8119b7a072`  
		Last Modified: Thu, 13 Jul 2023 21:49:46 GMT  
		Size: 5.2 MB (5173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc62259aed8a302b7cb52adf9701c763fb05897f5965d7873f6e27e88d4e07e`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3f8be8762d1cac21e849032e638a3ebf9bbb3957511eba1b7321783b83f23c`  
		Last Modified: Thu, 13 Jul 2023 21:49:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.18` - linux; arm variant v7

```console
$ docker pull nats@sha256:05b3018971114ff61d10e947e304f35c7bbc0abee425911c0fd58e23f7ae74e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8068141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4043b810630b65430ae04fb007b13c892d5e16ae40ea86b45712575d54868208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 22:36:15 GMT
ADD file:082f034323c559f3cb9feb6422c88b1ec8017f436d6109e238a5c5384a32a90a in / 
# Wed, 14 Jun 2023 22:36:15 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 22:52:54 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 22:52:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 22:52:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 22:52:57 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:52:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 22:52:57 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:633ba29fd335042456b6e2c073636f6fa30de56f1331c442914739b92a479974`  
		Last Modified: Wed, 14 Jun 2023 22:36:49 GMT  
		Size: 2.9 MB (2898508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b240facc4a312dbc41a0d9d2b5f34f26188edc082396407147566f4670a7bd`  
		Last Modified: Thu, 13 Jul 2023 22:53:30 GMT  
		Size: 5.2 MB (5168636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c49f0e2539269574bfe0565b74747b67dc174076c7d3b2b2c8064b2af71a80`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52f69564b85401d79f11d3d0dd7775aa0dfa3d09c58f3daedcbe1f3fe676eea`  
		Last Modified: Thu, 13 Jul 2023 22:53:28 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:aa93c00cb94a9cf48edbefb3fbb029b8d8187ccf4735f2eff181906d0e869854
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8309359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc0605733abd9e160812417dd92d5c4812e0640ef2a71568b2f2aed85eb6685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 13 Jul 2023 23:11:00 GMT
ENV NATS_SERVER=2.9.20
# Thu, 13 Jul 2023 23:11:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59ebc51e99fd97f92b8ecf3d0ee566aef9e133c2fc0a981e0522c105490c2e99' ;; 		armhf) natsArch='arm6'; sha256='c27abedca49baf59799630505f9e37ae22dc9ec644f0a645537e1b5d33221491' ;; 		armv7) natsArch='arm7'; sha256='fdd51a5c3ed7d47ef5efae1e9861e317df37e385205e45df63c35968650e59e4' ;; 		x86_64) natsArch='amd64'; sha256='626288430030b63a05b1fa79aa6ed84344c29ae78808e62b078add906d77f138' ;; 		x86) natsArch='386'; sha256='7db99a9d9e2b87304dab0745409b51dbb1a366705b0d08bc7da5ad025e30140e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 13 Jul 2023 23:11:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 Jul 2023 23:11:03 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Jul 2023 23:11:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8d12353ca807b3f28a178dcf6ddfe80ac709c12b0da6364e48db96ab06e400`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 5.0 MB (4979109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7977030405ec12383b1b2033bc0fceb08f5c959b13d57ba18f74f11efee542ed`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041d1130902bd23c5b39754ecf01c19ed66a35c6e60064301df126b0f52259ad`  
		Last Modified: Thu, 13 Jul 2023 23:11:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:8e0fb53c305217c0f29f21e8176fce1f4f11648c96543f0970666d8596e2d69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4645; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:700a4b586eb96ff46eef5a949c50297d689f8b31d62ea1ca773dd6895c3f039d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5126531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5907f5a08f299f1dacf051a9fc09fb9189deb2b0dce45877975471766b706954`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:83ff3835bde68ad26982d2ccc535db9982a508facc29fdbcbbfb9675666fbdc6 in /nats-server 
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:29:32 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:29:33 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:29:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67e402a9bce54a5dfde340b14dba6b73ef42a3b94cb337301bf4374e77ec7040`  
		Last Modified: Thu, 13 Jul 2023 22:30:12 GMT  
		Size: 5.1 MB (5126023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a9f6e59497aefb2b8a64f61ee04f476641f2b25c8c62c37e5fdfaab68f8f7e`  
		Last Modified: Thu, 13 Jul 2023 22:30:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:6fd7bfb33bbf19e7ccb75c6ac3fcdc072b6120923fdb4e96e29492a5e7b89289
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4890101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d7fa51b81b0dcfb6ee49a1b74a5881dbf8163021afff101d2002b70686142a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:b5f9cb21b49e06d0ef4d044cf5d2fa6f64bbabb0cfb73701be4fa9d1e7c16c56 in /nats-server 
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 21:49:27 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:505fc4baba759223316e40a0109c61f162bb1d1acafb25bbc8e92b684cd58c5e`  
		Last Modified: Thu, 13 Jul 2023 21:50:07 GMT  
		Size: 4.9 MB (4889594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc06a01182930b7a494867f205f3a02b099200299bffa49031f3085b8952f64`  
		Last Modified: Thu, 13 Jul 2023 21:50:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ec4eab4197d5b340c7bcbbfda1e3bca6ac9874273362a95cb4f58157884759e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab94676f2d9fc59f778cd1526e8664a87db5a1b0741b2053991fb0fb00a2a16a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:53:11 GMT
COPY file:b1a666d296b7b01c216ccd9e1f03715958de83d192993bc8ab769d7998b1703f in /nats-server 
# Thu, 13 Jul 2023 22:53:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:53:12 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:775e6a1e06f337eb4fc74b89e37d008aac2e092d4bfd8d25f944b5b8d257bf8e`  
		Last Modified: Thu, 13 Jul 2023 22:53:52 GMT  
		Size: 4.9 MB (4880250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e8a9e7894a37f644a39457db86f9e94f7b92aadfeac1fd47ee846be3c7eb8f`  
		Last Modified: Thu, 13 Jul 2023 22:53:51 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb5aafaa1c1ada08d1342efaacdbbc72351ea5fa9ed825ec83c84c194a1793aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411f554cbcd46eb35b3ba4cd400a5e29132ded085f6ec4efaccaa6121a464db9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 23:11:18 GMT
COPY file:75a8428ab964e430ddc475b81bfe8411c8a1a8487d06f66b7b2be85ebca4c05f in /nats-server 
# Thu, 13 Jul 2023 23:11:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 23:11:19 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 23:11:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 23:11:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff35e5a1c81a5e14fcb0cddaf7b6bb7a86d01c91297fc204d6f59f81ab699f42`  
		Last Modified: Thu, 13 Jul 2023 23:11:55 GMT  
		Size: 4.7 MB (4694032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ddd8ff8791364717d428b048bce331ac51b1654fac486b5b5d64c7f9a6bd1`  
		Last Modified: Thu, 13 Jul 2023 23:11:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:63c26578744b038b074f43eb6c0b3958667480b48bfe2a74c675fa52295f6767
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109612796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7071df68a96690f5443acb6ef9a47cea84abc3e0dd4a92efaa064a3144b56ed2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Fri, 14 Jul 2023 00:03:16 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:a5074ddde966142308b669c647979e812040bd9a0280cfce51a983385df577ec in C:\nats-server.exe 
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:03:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bad9bf846d07362d8295a4479f8f2965dfb5934a9a032b335ce3cb086bdf7`  
		Last Modified: Fri, 14 Jul 2023 00:04:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b0789d7cd0ee38c3d2d6f0d8d4662e4e4f242055fa09752c571e9e0b12b25`  
		Last Modified: Fri, 14 Jul 2023 00:04:05 GMT  
		Size: 5.2 MB (5198141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7714f1d09ea353a9769c79f15345a77c802214a0d24c3ed987cf9bc90fa67933`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4710eb1eae23febe62cd19d1e08fda4c2417972b715e389b5078de0796c915f`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2187cbf833c204e29fc58f360a3c3c572ea7fe8140d088f10f16abeb6666d374`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f146e585d072cd21e48a1fd715a9e5ba5233a54652a5494c2efe8216b210ade`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:54beaa3c85e41593c8d7f235ac1ecea3c3dd2eeb63dc2f53e75a8094579ff7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:700a4b586eb96ff46eef5a949c50297d689f8b31d62ea1ca773dd6895c3f039d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5126531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5907f5a08f299f1dacf051a9fc09fb9189deb2b0dce45877975471766b706954`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:83ff3835bde68ad26982d2ccc535db9982a508facc29fdbcbbfb9675666fbdc6 in /nats-server 
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:29:32 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:29:33 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:29:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67e402a9bce54a5dfde340b14dba6b73ef42a3b94cb337301bf4374e77ec7040`  
		Last Modified: Thu, 13 Jul 2023 22:30:12 GMT  
		Size: 5.1 MB (5126023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a9f6e59497aefb2b8a64f61ee04f476641f2b25c8c62c37e5fdfaab68f8f7e`  
		Last Modified: Thu, 13 Jul 2023 22:30:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:6fd7bfb33bbf19e7ccb75c6ac3fcdc072b6120923fdb4e96e29492a5e7b89289
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4890101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d7fa51b81b0dcfb6ee49a1b74a5881dbf8163021afff101d2002b70686142a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:b5f9cb21b49e06d0ef4d044cf5d2fa6f64bbabb0cfb73701be4fa9d1e7c16c56 in /nats-server 
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 21:49:27 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:505fc4baba759223316e40a0109c61f162bb1d1acafb25bbc8e92b684cd58c5e`  
		Last Modified: Thu, 13 Jul 2023 21:50:07 GMT  
		Size: 4.9 MB (4889594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc06a01182930b7a494867f205f3a02b099200299bffa49031f3085b8952f64`  
		Last Modified: Thu, 13 Jul 2023 21:50:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ec4eab4197d5b340c7bcbbfda1e3bca6ac9874273362a95cb4f58157884759e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab94676f2d9fc59f778cd1526e8664a87db5a1b0741b2053991fb0fb00a2a16a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:53:11 GMT
COPY file:b1a666d296b7b01c216ccd9e1f03715958de83d192993bc8ab769d7998b1703f in /nats-server 
# Thu, 13 Jul 2023 22:53:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:53:12 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:775e6a1e06f337eb4fc74b89e37d008aac2e092d4bfd8d25f944b5b8d257bf8e`  
		Last Modified: Thu, 13 Jul 2023 22:53:52 GMT  
		Size: 4.9 MB (4880250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e8a9e7894a37f644a39457db86f9e94f7b92aadfeac1fd47ee846be3c7eb8f`  
		Last Modified: Thu, 13 Jul 2023 22:53:51 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb5aafaa1c1ada08d1342efaacdbbc72351ea5fa9ed825ec83c84c194a1793aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411f554cbcd46eb35b3ba4cd400a5e29132ded085f6ec4efaccaa6121a464db9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 23:11:18 GMT
COPY file:75a8428ab964e430ddc475b81bfe8411c8a1a8487d06f66b7b2be85ebca4c05f in /nats-server 
# Thu, 13 Jul 2023 23:11:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 23:11:19 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 23:11:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 23:11:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff35e5a1c81a5e14fcb0cddaf7b6bb7a86d01c91297fc204d6f59f81ab699f42`  
		Last Modified: Thu, 13 Jul 2023 23:11:55 GMT  
		Size: 4.7 MB (4694032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ddd8ff8791364717d428b048bce331ac51b1654fac486b5b5d64c7f9a6bd1`  
		Last Modified: Thu, 13 Jul 2023 23:11:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:bfff91215109e40d5a3d637ce8bc11a4bae8b3a555e2c79188bab93b2397278b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:nanoserver` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:63c26578744b038b074f43eb6c0b3958667480b48bfe2a74c675fa52295f6767
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109612796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7071df68a96690f5443acb6ef9a47cea84abc3e0dd4a92efaa064a3144b56ed2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Fri, 14 Jul 2023 00:03:16 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:a5074ddde966142308b669c647979e812040bd9a0280cfce51a983385df577ec in C:\nats-server.exe 
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:03:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bad9bf846d07362d8295a4479f8f2965dfb5934a9a032b335ce3cb086bdf7`  
		Last Modified: Fri, 14 Jul 2023 00:04:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b0789d7cd0ee38c3d2d6f0d8d4662e4e4f242055fa09752c571e9e0b12b25`  
		Last Modified: Fri, 14 Jul 2023 00:04:05 GMT  
		Size: 5.2 MB (5198141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7714f1d09ea353a9769c79f15345a77c802214a0d24c3ed987cf9bc90fa67933`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4710eb1eae23febe62cd19d1e08fda4c2417972b715e389b5078de0796c915f`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2187cbf833c204e29fc58f360a3c3c572ea7fe8140d088f10f16abeb6666d374`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f146e585d072cd21e48a1fd715a9e5ba5233a54652a5494c2efe8216b210ade`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:bfff91215109e40d5a3d637ce8bc11a4bae8b3a555e2c79188bab93b2397278b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:63c26578744b038b074f43eb6c0b3958667480b48bfe2a74c675fa52295f6767
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109612796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7071df68a96690f5443acb6ef9a47cea84abc3e0dd4a92efaa064a3144b56ed2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Fri, 14 Jul 2023 00:03:16 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:a5074ddde966142308b669c647979e812040bd9a0280cfce51a983385df577ec in C:\nats-server.exe 
# Fri, 14 Jul 2023 00:03:18 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:03:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:20 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bad9bf846d07362d8295a4479f8f2965dfb5934a9a032b335ce3cb086bdf7`  
		Last Modified: Fri, 14 Jul 2023 00:04:06 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b0789d7cd0ee38c3d2d6f0d8d4662e4e4f242055fa09752c571e9e0b12b25`  
		Last Modified: Fri, 14 Jul 2023 00:04:05 GMT  
		Size: 5.2 MB (5198141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7714f1d09ea353a9769c79f15345a77c802214a0d24c3ed987cf9bc90fa67933`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4710eb1eae23febe62cd19d1e08fda4c2417972b715e389b5078de0796c915f`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2187cbf833c204e29fc58f360a3c3c572ea7fe8140d088f10f16abeb6666d374`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f146e585d072cd21e48a1fd715a9e5ba5233a54652a5494c2efe8216b210ade`  
		Last Modified: Fri, 14 Jul 2023 00:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:54beaa3c85e41593c8d7f235ac1ecea3c3dd2eeb63dc2f53e75a8094579ff7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:700a4b586eb96ff46eef5a949c50297d689f8b31d62ea1ca773dd6895c3f039d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5126531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5907f5a08f299f1dacf051a9fc09fb9189deb2b0dce45877975471766b706954`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:83ff3835bde68ad26982d2ccc535db9982a508facc29fdbcbbfb9675666fbdc6 in /nats-server 
# Thu, 13 Jul 2023 22:29:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:29:32 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:29:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:29:33 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:29:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67e402a9bce54a5dfde340b14dba6b73ef42a3b94cb337301bf4374e77ec7040`  
		Last Modified: Thu, 13 Jul 2023 22:30:12 GMT  
		Size: 5.1 MB (5126023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a9f6e59497aefb2b8a64f61ee04f476641f2b25c8c62c37e5fdfaab68f8f7e`  
		Last Modified: Thu, 13 Jul 2023 22:30:11 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:6fd7bfb33bbf19e7ccb75c6ac3fcdc072b6120923fdb4e96e29492a5e7b89289
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4890101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d7fa51b81b0dcfb6ee49a1b74a5881dbf8163021afff101d2002b70686142a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:b5f9cb21b49e06d0ef4d044cf5d2fa6f64bbabb0cfb73701be4fa9d1e7c16c56 in /nats-server 
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 21:49:27 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:505fc4baba759223316e40a0109c61f162bb1d1acafb25bbc8e92b684cd58c5e`  
		Last Modified: Thu, 13 Jul 2023 21:50:07 GMT  
		Size: 4.9 MB (4889594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc06a01182930b7a494867f205f3a02b099200299bffa49031f3085b8952f64`  
		Last Modified: Thu, 13 Jul 2023 21:50:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:5ec4eab4197d5b340c7bcbbfda1e3bca6ac9874273362a95cb4f58157884759e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab94676f2d9fc59f778cd1526e8664a87db5a1b0741b2053991fb0fb00a2a16a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 22:53:11 GMT
COPY file:b1a666d296b7b01c216ccd9e1f03715958de83d192993bc8ab769d7998b1703f in /nats-server 
# Thu, 13 Jul 2023 22:53:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 22:53:12 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 22:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 22:53:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 22:53:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:775e6a1e06f337eb4fc74b89e37d008aac2e092d4bfd8d25f944b5b8d257bf8e`  
		Last Modified: Thu, 13 Jul 2023 22:53:52 GMT  
		Size: 4.9 MB (4880250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e8a9e7894a37f644a39457db86f9e94f7b92aadfeac1fd47ee846be3c7eb8f`  
		Last Modified: Thu, 13 Jul 2023 22:53:51 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb5aafaa1c1ada08d1342efaacdbbc72351ea5fa9ed825ec83c84c194a1793aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411f554cbcd46eb35b3ba4cd400a5e29132ded085f6ec4efaccaa6121a464db9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 23:11:18 GMT
COPY file:75a8428ab964e430ddc475b81bfe8411c8a1a8487d06f66b7b2be85ebca4c05f in /nats-server 
# Thu, 13 Jul 2023 23:11:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 23:11:19 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 23:11:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 23:11:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 23:11:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff35e5a1c81a5e14fcb0cddaf7b6bb7a86d01c91297fc204d6f59f81ab699f42`  
		Last Modified: Thu, 13 Jul 2023 23:11:55 GMT  
		Size: 4.7 MB (4694032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ddd8ff8791364717d428b048bce331ac51b1654fac486b5b5d64c7f9a6bd1`  
		Last Modified: Thu, 13 Jul 2023 23:11:54 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:a8c2c33cbe248ffdf05cf1e29ce7026eefd132eb0cd15aff802e6031f5e1e6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:windowsservercore` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:0fe2b83b4b22020701d93f9a59fb4fdbcfa157be7fb04e9288db445b76eaee4f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1945570306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fbdb411f499afb755df4b20ab636581d3aaed9c3a91c502ef50eeb34352001`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 22:38:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 14 Jul 2023 00:00:18 GMT
ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:00:19 GMT
ENV NATS_SERVER=2.9.20
# Fri, 14 Jul 2023 00:00:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.20/nats-server-v2.9.20-windows-amd64.zip
# Fri, 14 Jul 2023 00:00:21 GMT
ENV NATS_SERVER_SHASUM=6dd2f4648c3b5f7c0b0a2fc492ecd2263d3dfb22ea5cf2d0c018a82f0e912b35
# Fri, 14 Jul 2023 00:01:20 GMT
RUN Set-PSDebug -Trace 2
# Fri, 14 Jul 2023 00:02:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 14 Jul 2023 00:02:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:02:58 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:02:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b452db6d50a62b6e0e8dadb19715cfcf62cf73e54b5d3bac96621c1093673c`  
		Last Modified: Thu, 13 Jul 2023 23:25:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f8ca4b8d322e27c827c0ba667217bc04a39b69f5f483d5f2f9726e6d42522e`  
		Last Modified: Fri, 14 Jul 2023 00:03:50 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f33781e88272c93d82ac65b1dfc5a07ce75d4e8e04e8561f158831356e7fea4`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe631d552a5255bffd0e5aeec249b1684a7e8c75fe30b185e199fbfdecedfae`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb256a4292680f56d2092582b633530842c97891e2f740aa78403b240999c630`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb7d2753eb8c81851f9e3869d39a0947479d1411590331b94108e9cb2bef9e5`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 226.1 KB (226138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c118d6802e5d239c3513560bc388331e2aaf975937a7aa8625dc85e54015becc`  
		Last Modified: Fri, 14 Jul 2023 00:03:47 GMT  
		Size: 5.6 MB (5641748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689840dc0e8e1fb392e9005f0603c05fb29100193e9d6b8528369ce241b81dee`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5788a19b6a5a361435ec99a16308610c901b5452d1281dc9bdab065485a4ad1`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa4bedb48935e18d91878ff81f1b80d8e4ff1149700225914c54b1a6b83933c`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f710347dc06495d6660dfd5cbc8d9c4f5f4555d2ac5e26adc76ee8de42bc75ca`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:a8c2c33cbe248ffdf05cf1e29ce7026eefd132eb0cd15aff802e6031f5e1e6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:0fe2b83b4b22020701d93f9a59fb4fdbcfa157be7fb04e9288db445b76eaee4f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1945570306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fbdb411f499afb755df4b20ab636581d3aaed9c3a91c502ef50eeb34352001`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 22:38:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 14 Jul 2023 00:00:18 GMT
ENV NATS_DOCKERIZED=1
# Fri, 14 Jul 2023 00:00:19 GMT
ENV NATS_SERVER=2.9.20
# Fri, 14 Jul 2023 00:00:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.20/nats-server-v2.9.20-windows-amd64.zip
# Fri, 14 Jul 2023 00:00:21 GMT
ENV NATS_SERVER_SHASUM=6dd2f4648c3b5f7c0b0a2fc492ecd2263d3dfb22ea5cf2d0c018a82f0e912b35
# Fri, 14 Jul 2023 00:01:20 GMT
RUN Set-PSDebug -Trace 2
# Fri, 14 Jul 2023 00:02:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 14 Jul 2023 00:02:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 14 Jul 2023 00:02:58 GMT
EXPOSE 4222 6222 8222
# Fri, 14 Jul 2023 00:02:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 14 Jul 2023 00:03:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b452db6d50a62b6e0e8dadb19715cfcf62cf73e54b5d3bac96621c1093673c`  
		Last Modified: Thu, 13 Jul 2023 23:25:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f8ca4b8d322e27c827c0ba667217bc04a39b69f5f483d5f2f9726e6d42522e`  
		Last Modified: Fri, 14 Jul 2023 00:03:50 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f33781e88272c93d82ac65b1dfc5a07ce75d4e8e04e8561f158831356e7fea4`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe631d552a5255bffd0e5aeec249b1684a7e8c75fe30b185e199fbfdecedfae`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb256a4292680f56d2092582b633530842c97891e2f740aa78403b240999c630`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb7d2753eb8c81851f9e3869d39a0947479d1411590331b94108e9cb2bef9e5`  
		Last Modified: Fri, 14 Jul 2023 00:03:48 GMT  
		Size: 226.1 KB (226138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c118d6802e5d239c3513560bc388331e2aaf975937a7aa8625dc85e54015becc`  
		Last Modified: Fri, 14 Jul 2023 00:03:47 GMT  
		Size: 5.6 MB (5641748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689840dc0e8e1fb392e9005f0603c05fb29100193e9d6b8528369ce241b81dee`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5788a19b6a5a361435ec99a16308610c901b5452d1281dc9bdab065485a4ad1`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa4bedb48935e18d91878ff81f1b80d8e4ff1149700225914c54b1a6b83933c`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f710347dc06495d6660dfd5cbc8d9c4f5f4555d2ac5e26adc76ee8de42bc75ca`  
		Last Modified: Fri, 14 Jul 2023 00:03:46 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
