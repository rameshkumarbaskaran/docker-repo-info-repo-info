<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.16`](#nats2-alpine316)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.9`](#nats29)
-	[`nats:2.9-alpine`](#nats29-alpine)
-	[`nats:2.9-alpine3.16`](#nats29-alpine316)
-	[`nats:2.9-linux`](#nats29-linux)
-	[`nats:2.9-nanoserver`](#nats29-nanoserver)
-	[`nats:2.9-nanoserver-1809`](#nats29-nanoserver-1809)
-	[`nats:2.9-scratch`](#nats29-scratch)
-	[`nats:2.9-windowsservercore`](#nats29-windowsservercore)
-	[`nats:2.9-windowsservercore-1809`](#nats29-windowsservercore-1809)
-	[`nats:2.9.4`](#nats294)
-	[`nats:2.9.4-alpine`](#nats294-alpine)
-	[`nats:2.9.4-alpine3.16`](#nats294-alpine316)
-	[`nats:2.9.4-linux`](#nats294-linux)
-	[`nats:2.9.4-nanoserver`](#nats294-nanoserver)
-	[`nats:2.9.4-nanoserver-1809`](#nats294-nanoserver-1809)
-	[`nats:2.9.4-scratch`](#nats294-scratch)
-	[`nats:2.9.4-windowsservercore`](#nats294-windowsservercore)
-	[`nats:2.9.4-windowsservercore-1809`](#nats294-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.16`](#natsalpine316)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:34942deb3974eeb9aba6ad97a4ab5407ec2e93cf847dcf4a77117261364b0443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3532; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:05a4c0bc8897ddeeb9ddb1473028d9e1c9a0a2cb389516b11578c02f9ec8720f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4911098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c9c625dbef5ec34ca7dceca2ce480b3eb978932e2254e6cfe95c15eb9bb28b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:b9e75e481ae9d301a798308347b654037f5ea8bd8ce2eb3b62d56f1d0fb9aa31 in /nats-server 
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:19:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:19:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:19:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de750ae4d2f684dc52058ab61a992122d85ea9cd1a2c7d449a42ea52d637ca18`  
		Last Modified: Fri, 28 Oct 2022 00:20:46 GMT  
		Size: 4.9 MB (4910589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b72f1a5adda7df074f0eb3d095e5b1300624cd78ef32ff0c78927402b93d0e`  
		Last Modified: Fri, 28 Oct 2022 00:20:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:6a348db5fdde022e586e4fe00252f5207f73386b543dad2b9c791c926472bf98
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4678079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d212b3f530fd382de8872a80b70481fc4db336913a9a59a503f67eac93938faa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:0fb4e969033ab88575e23537c015c04681107529d9128dd4fb94d4f441cf13ea in /nats-server 
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:34:37 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:34:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:34:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ce7e3dd39763e6d0dc795d5534c1a6b6e722fda5cf6cbea372a78489a04f27e`  
		Last Modified: Fri, 28 Oct 2022 00:36:14 GMT  
		Size: 4.7 MB (4677570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c4367ae4414051a0ffbe623600d5fedcab0f7b5110c0a0d95e8bf78c93cfad`  
		Last Modified: Fri, 28 Oct 2022 00:36:13 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:8cf5bcc23025af97af872f1e5fc8e37f60ef5ce1b99163e840515dbc515c735c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4669750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef35e6a4f18c95e20350eca6fd4dd61d948dce45a42d73088f65d880c4dde5f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 01:12:28 GMT
COPY file:c324c9ced487df787b815eb06f1de7520b3f2f3c23cb313b6b6e692d30dce518 in /nats-server 
# Fri, 28 Oct 2022 01:12:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 01:12:29 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:493666cecebad3f9973ea93e7811c9fb15f833a53618a7c6abc12abc16a828b6`  
		Last Modified: Fri, 28 Oct 2022 01:14:05 GMT  
		Size: 4.7 MB (4669243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b13ae6ba1b3faf170714cacd52b2535f8aaf0f18ea5f16479b9a3a9e2e89159`  
		Last Modified: Fri, 28 Oct 2022 01:14:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:eebe621bb4c2136c03d0ede2969549480d42c0faa54935450acdaa9b90dcd474
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6feb88b2953948859fb8aeb942da3d4917625a55916e864e7d1995f816a108`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:4a2b1fa0bbd909bf79b017ae360815907a983b7b2c3b158abf0ed8a95668fb78 in /nats-server 
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:40:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:40:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca262f3c33011e42391f6b52c9727d27cd46c6b5a6a5ed69851d60e703606850`  
		Last Modified: Fri, 28 Oct 2022 00:40:59 GMT  
		Size: 4.5 MB (4498479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e4d79c576957d7c047001eb103698d3be1cb4784790f6947b14d39851bf550`  
		Last Modified: Fri, 28 Oct 2022 00:40:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:2223d534de4b168e93ee5731584939fef6069904b42e09ca39e4ef46358dd54f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111744859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05e32726d6a3eb6cd30c7f3cfd15eac77097a00adac44dc185b61d03b58e62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Oct 2022 00:17:42 GMT
RUN cmd /S /C #(nop) COPY file:5cda9aa918fe992fe978c90843552eede9fe664f92442d3068d77fa07c27682b in C:\nats-server.exe 
# Fri, 28 Oct 2022 00:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce29f4214f0fb0200b149c387d5e94ee47d5705e9bc7b884331390782282065f`  
		Last Modified: Thu, 27 Oct 2022 21:23:38 GMT  
		Size: 106.8 MB (106773776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4388e47ca696927a8eab713d6e9905f0069a119b2029c0ddc2d6c8c0f1094157`  
		Last Modified: Fri, 28 Oct 2022 00:18:37 GMT  
		Size: 5.0 MB (4965105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d567bc025c016fe1b38a5f2463f1deb5986fed52de265a356d96e4f782ea04d`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147121d4056552beb6f6f5c897e57e7a81fe46d490dddeb6c410461807b6bf78`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20911c0814537b45d8c70b48e190f3b0a68c11a97b5b3d2745ce9e4d96f4b42`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b8f3033a8d06c06f6986ee485dc4c2f6ee159f98545da2612b238b6c716fcc`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:f8db1a71f146a719842c8d851894fec6e543183c2da4c400f5a2a960ca352102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:03761b5d6c59b37faca88bbd8c37d96613f7ee26012573cc86feb34504bd0051
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8006885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd9e2b47f06b7e327bbbfb1f8baba520cad84321648cf3c142908a9551d86e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:19:47 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:19:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:19:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:19:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:19:49 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:19:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d00bd5b211d6d2259e1123fc716bc7778fb4f2ef8140aebc9a600e7691d7251`  
		Last Modified: Fri, 28 Oct 2022 00:20:23 GMT  
		Size: 5.2 MB (5199832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa3b3a919296293971047f3b55bab13f38c874ad3ee595a4ee9de57c4e1e176`  
		Last Modified: Fri, 28 Oct 2022 00:20:22 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9fdb9eee2a7eda4133115ecd218dd98b7afa1de02bda16dfc85a1f544b5a14`  
		Last Modified: Fri, 28 Oct 2022 00:20:22 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:48c4cd343809a6f219ca8643b99ee9540ee1018c6b6108e1056188c0d54b0910
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7574875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c98fab4f18b0ccd35c5999b24a1e85fc4e09ee832ec2941809c47a74708517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:34:22 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:34:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:34:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:34:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:34:25 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:34:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bec236bdb0c174a608728f09fa7bb201e34846e10c96aa0a3cb0da4ce0e064`  
		Last Modified: Fri, 28 Oct 2022 00:35:40 GMT  
		Size: 5.0 MB (4959934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e35b5ff49cea58009b9004b126d99f234f6932652392dd2b286ad2cddc6453`  
		Last Modified: Fri, 28 Oct 2022 00:35:39 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013802adfa3f871235a505bf256abffbaa8ee6af1dd143af6e427e542f1cec3c`  
		Last Modified: Fri, 28 Oct 2022 00:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:fafa9ed028325662750ff07f25939a66aac303a0b50bca635cd6b33f48683f3d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7372975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f22484361778a7e488b1496ff292a52b4bfb779267fee6dc8a99d5171b119b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 01:12:12 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 01:12:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 01:12:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 01:12:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 01:12:14 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 01:12:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01440488995de9af5b51ae28a139872013b93eda267a46f001cd2615ba9ab0f8`  
		Last Modified: Fri, 28 Oct 2022 01:13:32 GMT  
		Size: 5.0 MB (4954939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aac9b75327e61f497ade56035d2515d5a15073ab8c1a4b1345c46f39e394844`  
		Last Modified: Fri, 28 Oct 2022 01:13:31 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebb5d7ec0dd8b480bcba44b32f9ae5b43d529140b1b68be2d5b1bce9cc8c257`  
		Last Modified: Fri, 28 Oct 2022 01:13:31 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:879ce95c8afa3059b0b8858ce8ad18ada3bb72700c6e6ff296efc6ffebd7e20d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c212d4563965c7102edd4e79355e3907e054df45a0d2df3c1a9c2e73d28c6bc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:40:01 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:40:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:40:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:40:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:40:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:40:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbcbe919967004774a1fa79409186b285f24a7e631c6fb2e6bbf2a95cda9caf`  
		Last Modified: Fri, 28 Oct 2022 00:40:35 GMT  
		Size: 4.8 MB (4782894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659a3f4a00fc9e66e3816eb4310fdbbc3c1e488c97b2b3a780cc4b3fbc9ae486`  
		Last Modified: Fri, 28 Oct 2022 00:40:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a64ad8526321dd00599ac40ef36787222c36b765f37a5a446005c6b31b6862`  
		Last Modified: Fri, 28 Oct 2022 00:40:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.16`

```console
$ docker pull nats@sha256:f8db1a71f146a719842c8d851894fec6e543183c2da4c400f5a2a960ca352102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:03761b5d6c59b37faca88bbd8c37d96613f7ee26012573cc86feb34504bd0051
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8006885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd9e2b47f06b7e327bbbfb1f8baba520cad84321648cf3c142908a9551d86e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:19:47 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:19:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:19:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:19:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:19:49 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:19:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d00bd5b211d6d2259e1123fc716bc7778fb4f2ef8140aebc9a600e7691d7251`  
		Last Modified: Fri, 28 Oct 2022 00:20:23 GMT  
		Size: 5.2 MB (5199832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa3b3a919296293971047f3b55bab13f38c874ad3ee595a4ee9de57c4e1e176`  
		Last Modified: Fri, 28 Oct 2022 00:20:22 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9fdb9eee2a7eda4133115ecd218dd98b7afa1de02bda16dfc85a1f544b5a14`  
		Last Modified: Fri, 28 Oct 2022 00:20:22 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:48c4cd343809a6f219ca8643b99ee9540ee1018c6b6108e1056188c0d54b0910
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7574875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c98fab4f18b0ccd35c5999b24a1e85fc4e09ee832ec2941809c47a74708517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:34:22 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:34:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:34:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:34:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:34:25 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:34:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bec236bdb0c174a608728f09fa7bb201e34846e10c96aa0a3cb0da4ce0e064`  
		Last Modified: Fri, 28 Oct 2022 00:35:40 GMT  
		Size: 5.0 MB (4959934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e35b5ff49cea58009b9004b126d99f234f6932652392dd2b286ad2cddc6453`  
		Last Modified: Fri, 28 Oct 2022 00:35:39 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013802adfa3f871235a505bf256abffbaa8ee6af1dd143af6e427e542f1cec3c`  
		Last Modified: Fri, 28 Oct 2022 00:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:fafa9ed028325662750ff07f25939a66aac303a0b50bca635cd6b33f48683f3d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7372975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f22484361778a7e488b1496ff292a52b4bfb779267fee6dc8a99d5171b119b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 01:12:12 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 01:12:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 01:12:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 01:12:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 01:12:14 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 01:12:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01440488995de9af5b51ae28a139872013b93eda267a46f001cd2615ba9ab0f8`  
		Last Modified: Fri, 28 Oct 2022 01:13:32 GMT  
		Size: 5.0 MB (4954939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aac9b75327e61f497ade56035d2515d5a15073ab8c1a4b1345c46f39e394844`  
		Last Modified: Fri, 28 Oct 2022 01:13:31 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebb5d7ec0dd8b480bcba44b32f9ae5b43d529140b1b68be2d5b1bce9cc8c257`  
		Last Modified: Fri, 28 Oct 2022 01:13:31 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:879ce95c8afa3059b0b8858ce8ad18ada3bb72700c6e6ff296efc6ffebd7e20d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c212d4563965c7102edd4e79355e3907e054df45a0d2df3c1a9c2e73d28c6bc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:40:01 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:40:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:40:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:40:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:40:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:40:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbcbe919967004774a1fa79409186b285f24a7e631c6fb2e6bbf2a95cda9caf`  
		Last Modified: Fri, 28 Oct 2022 00:40:35 GMT  
		Size: 4.8 MB (4782894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659a3f4a00fc9e66e3816eb4310fdbbc3c1e488c97b2b3a780cc4b3fbc9ae486`  
		Last Modified: Fri, 28 Oct 2022 00:40:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a64ad8526321dd00599ac40ef36787222c36b765f37a5a446005c6b31b6862`  
		Last Modified: Fri, 28 Oct 2022 00:40:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:806d56dd55acbc6497c5cc9ff5916b36ba091212c7308b3a23a1098876e686f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:05a4c0bc8897ddeeb9ddb1473028d9e1c9a0a2cb389516b11578c02f9ec8720f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4911098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c9c625dbef5ec34ca7dceca2ce480b3eb978932e2254e6cfe95c15eb9bb28b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:b9e75e481ae9d301a798308347b654037f5ea8bd8ce2eb3b62d56f1d0fb9aa31 in /nats-server 
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:19:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:19:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:19:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de750ae4d2f684dc52058ab61a992122d85ea9cd1a2c7d449a42ea52d637ca18`  
		Last Modified: Fri, 28 Oct 2022 00:20:46 GMT  
		Size: 4.9 MB (4910589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b72f1a5adda7df074f0eb3d095e5b1300624cd78ef32ff0c78927402b93d0e`  
		Last Modified: Fri, 28 Oct 2022 00:20:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:6a348db5fdde022e586e4fe00252f5207f73386b543dad2b9c791c926472bf98
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4678079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d212b3f530fd382de8872a80b70481fc4db336913a9a59a503f67eac93938faa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:0fb4e969033ab88575e23537c015c04681107529d9128dd4fb94d4f441cf13ea in /nats-server 
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:34:37 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:34:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:34:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ce7e3dd39763e6d0dc795d5534c1a6b6e722fda5cf6cbea372a78489a04f27e`  
		Last Modified: Fri, 28 Oct 2022 00:36:14 GMT  
		Size: 4.7 MB (4677570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c4367ae4414051a0ffbe623600d5fedcab0f7b5110c0a0d95e8bf78c93cfad`  
		Last Modified: Fri, 28 Oct 2022 00:36:13 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:8cf5bcc23025af97af872f1e5fc8e37f60ef5ce1b99163e840515dbc515c735c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4669750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef35e6a4f18c95e20350eca6fd4dd61d948dce45a42d73088f65d880c4dde5f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 01:12:28 GMT
COPY file:c324c9ced487df787b815eb06f1de7520b3f2f3c23cb313b6b6e692d30dce518 in /nats-server 
# Fri, 28 Oct 2022 01:12:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 01:12:29 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:493666cecebad3f9973ea93e7811c9fb15f833a53618a7c6abc12abc16a828b6`  
		Last Modified: Fri, 28 Oct 2022 01:14:05 GMT  
		Size: 4.7 MB (4669243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b13ae6ba1b3faf170714cacd52b2535f8aaf0f18ea5f16479b9a3a9e2e89159`  
		Last Modified: Fri, 28 Oct 2022 01:14:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:eebe621bb4c2136c03d0ede2969549480d42c0faa54935450acdaa9b90dcd474
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6feb88b2953948859fb8aeb942da3d4917625a55916e864e7d1995f816a108`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:4a2b1fa0bbd909bf79b017ae360815907a983b7b2c3b158abf0ed8a95668fb78 in /nats-server 
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:40:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:40:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca262f3c33011e42391f6b52c9727d27cd46c6b5a6a5ed69851d60e703606850`  
		Last Modified: Fri, 28 Oct 2022 00:40:59 GMT  
		Size: 4.5 MB (4498479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e4d79c576957d7c047001eb103698d3be1cb4784790f6947b14d39851bf550`  
		Last Modified: Fri, 28 Oct 2022 00:40:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:fafc6597b93f9cbe091b8309cf8ae5f413fcdac1263da3b9c407becbb4edf56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:2223d534de4b168e93ee5731584939fef6069904b42e09ca39e4ef46358dd54f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111744859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05e32726d6a3eb6cd30c7f3cfd15eac77097a00adac44dc185b61d03b58e62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Oct 2022 00:17:42 GMT
RUN cmd /S /C #(nop) COPY file:5cda9aa918fe992fe978c90843552eede9fe664f92442d3068d77fa07c27682b in C:\nats-server.exe 
# Fri, 28 Oct 2022 00:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce29f4214f0fb0200b149c387d5e94ee47d5705e9bc7b884331390782282065f`  
		Last Modified: Thu, 27 Oct 2022 21:23:38 GMT  
		Size: 106.8 MB (106773776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4388e47ca696927a8eab713d6e9905f0069a119b2029c0ddc2d6c8c0f1094157`  
		Last Modified: Fri, 28 Oct 2022 00:18:37 GMT  
		Size: 5.0 MB (4965105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d567bc025c016fe1b38a5f2463f1deb5986fed52de265a356d96e4f782ea04d`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147121d4056552beb6f6f5c897e57e7a81fe46d490dddeb6c410461807b6bf78`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20911c0814537b45d8c70b48e190f3b0a68c11a97b5b3d2745ce9e4d96f4b42`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b8f3033a8d06c06f6986ee485dc4c2f6ee159f98545da2612b238b6c716fcc`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:fafc6597b93f9cbe091b8309cf8ae5f413fcdac1263da3b9c407becbb4edf56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:2223d534de4b168e93ee5731584939fef6069904b42e09ca39e4ef46358dd54f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111744859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05e32726d6a3eb6cd30c7f3cfd15eac77097a00adac44dc185b61d03b58e62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Oct 2022 00:17:42 GMT
RUN cmd /S /C #(nop) COPY file:5cda9aa918fe992fe978c90843552eede9fe664f92442d3068d77fa07c27682b in C:\nats-server.exe 
# Fri, 28 Oct 2022 00:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce29f4214f0fb0200b149c387d5e94ee47d5705e9bc7b884331390782282065f`  
		Last Modified: Thu, 27 Oct 2022 21:23:38 GMT  
		Size: 106.8 MB (106773776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4388e47ca696927a8eab713d6e9905f0069a119b2029c0ddc2d6c8c0f1094157`  
		Last Modified: Fri, 28 Oct 2022 00:18:37 GMT  
		Size: 5.0 MB (4965105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d567bc025c016fe1b38a5f2463f1deb5986fed52de265a356d96e4f782ea04d`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147121d4056552beb6f6f5c897e57e7a81fe46d490dddeb6c410461807b6bf78`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20911c0814537b45d8c70b48e190f3b0a68c11a97b5b3d2745ce9e4d96f4b42`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b8f3033a8d06c06f6986ee485dc4c2f6ee159f98545da2612b238b6c716fcc`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:806d56dd55acbc6497c5cc9ff5916b36ba091212c7308b3a23a1098876e686f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:05a4c0bc8897ddeeb9ddb1473028d9e1c9a0a2cb389516b11578c02f9ec8720f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4911098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c9c625dbef5ec34ca7dceca2ce480b3eb978932e2254e6cfe95c15eb9bb28b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:b9e75e481ae9d301a798308347b654037f5ea8bd8ce2eb3b62d56f1d0fb9aa31 in /nats-server 
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:19:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:19:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:19:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de750ae4d2f684dc52058ab61a992122d85ea9cd1a2c7d449a42ea52d637ca18`  
		Last Modified: Fri, 28 Oct 2022 00:20:46 GMT  
		Size: 4.9 MB (4910589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b72f1a5adda7df074f0eb3d095e5b1300624cd78ef32ff0c78927402b93d0e`  
		Last Modified: Fri, 28 Oct 2022 00:20:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:6a348db5fdde022e586e4fe00252f5207f73386b543dad2b9c791c926472bf98
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4678079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d212b3f530fd382de8872a80b70481fc4db336913a9a59a503f67eac93938faa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:0fb4e969033ab88575e23537c015c04681107529d9128dd4fb94d4f441cf13ea in /nats-server 
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:34:37 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:34:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:34:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ce7e3dd39763e6d0dc795d5534c1a6b6e722fda5cf6cbea372a78489a04f27e`  
		Last Modified: Fri, 28 Oct 2022 00:36:14 GMT  
		Size: 4.7 MB (4677570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c4367ae4414051a0ffbe623600d5fedcab0f7b5110c0a0d95e8bf78c93cfad`  
		Last Modified: Fri, 28 Oct 2022 00:36:13 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:8cf5bcc23025af97af872f1e5fc8e37f60ef5ce1b99163e840515dbc515c735c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4669750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef35e6a4f18c95e20350eca6fd4dd61d948dce45a42d73088f65d880c4dde5f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 01:12:28 GMT
COPY file:c324c9ced487df787b815eb06f1de7520b3f2f3c23cb313b6b6e692d30dce518 in /nats-server 
# Fri, 28 Oct 2022 01:12:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 01:12:29 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:493666cecebad3f9973ea93e7811c9fb15f833a53618a7c6abc12abc16a828b6`  
		Last Modified: Fri, 28 Oct 2022 01:14:05 GMT  
		Size: 4.7 MB (4669243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b13ae6ba1b3faf170714cacd52b2535f8aaf0f18ea5f16479b9a3a9e2e89159`  
		Last Modified: Fri, 28 Oct 2022 01:14:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:eebe621bb4c2136c03d0ede2969549480d42c0faa54935450acdaa9b90dcd474
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6feb88b2953948859fb8aeb942da3d4917625a55916e864e7d1995f816a108`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:4a2b1fa0bbd909bf79b017ae360815907a983b7b2c3b158abf0ed8a95668fb78 in /nats-server 
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:40:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:40:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca262f3c33011e42391f6b52c9727d27cd46c6b5a6a5ed69851d60e703606850`  
		Last Modified: Fri, 28 Oct 2022 00:40:59 GMT  
		Size: 4.5 MB (4498479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e4d79c576957d7c047001eb103698d3be1cb4784790f6947b14d39851bf550`  
		Last Modified: Fri, 28 Oct 2022 00:40:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:fdb8994491270872284ca4358bc66e164b2f6fa02e5189163b51cb8df71bc276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:43e84da881b4607236ff0f9158fe2215c782c94b01effb76af5fb9831a594fcb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2779174179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab33aded854a32b758ffbe80d2425e85d79fe5e68257d305b54bf4661ce0ab5f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Fri, 28 Oct 2022 00:14:59 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:14:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.4/nats-server-v2.9.4-windows-amd64.zip
# Fri, 28 Oct 2022 00:15:01 GMT
ENV NATS_SERVER_SHASUM=ba5d135b14bb4f4c106639c6f0b3fe5530b4e9ec4dd2c4e3b83f78c0e808e435
# Fri, 28 Oct 2022 00:15:53 GMT
RUN Set-PSDebug -Trace 2
# Fri, 28 Oct 2022 00:17:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 28 Oct 2022 00:17:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:24 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6193ab94a0498ba6454e2a35e189837b37a2eb01403e8b62654bdc28a4569c`  
		Last Modified: Mon, 17 Oct 2022 21:52:22 GMT  
		Size: 849.2 MB (849228999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777120ea710a4a6c96e29b0896d6ba5301aeabc76ebc7746bdaf630026ceb3dd`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178f4f6f90f6bab4aaf8342187d088536e8a65bce5b71a78c8775ab21d57dc39`  
		Last Modified: Fri, 28 Oct 2022 00:18:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64be820df0d316e845aeaa24d9714941dc6038fb96c3af1ae68ce7de1304a0b`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7711c2ad12dd348b7559e313bb366a27c48900fb880fc0e18562ab742ce5e6`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 357.8 KB (357788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d41267dcad8d27b3da89455553106bf0cafab939c7e8ba37b7aa2a3c7bfb46d`  
		Last Modified: Fri, 28 Oct 2022 00:18:18 GMT  
		Size: 5.3 MB (5305490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7434c9c183776b09625ce99d06e361a904e516542812ffb699420f5a5a150394`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a4aaaadc6896c5cdcd54e586dc2512c4925eff8b4545ab14d6b23f33aaf1ec`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56300ead49ee511a9bd2dd1eb8849af5673a6f85d81158b22a3ab7349dbd4be4`  
		Last Modified: Fri, 28 Oct 2022 00:18:17 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1e5f72226f5d2f9b0094bf2b7fa505f3ebcea3bea5157a66f1fdce6147bb07`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:fdb8994491270872284ca4358bc66e164b2f6fa02e5189163b51cb8df71bc276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:43e84da881b4607236ff0f9158fe2215c782c94b01effb76af5fb9831a594fcb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2779174179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab33aded854a32b758ffbe80d2425e85d79fe5e68257d305b54bf4661ce0ab5f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Fri, 28 Oct 2022 00:14:59 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:14:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.4/nats-server-v2.9.4-windows-amd64.zip
# Fri, 28 Oct 2022 00:15:01 GMT
ENV NATS_SERVER_SHASUM=ba5d135b14bb4f4c106639c6f0b3fe5530b4e9ec4dd2c4e3b83f78c0e808e435
# Fri, 28 Oct 2022 00:15:53 GMT
RUN Set-PSDebug -Trace 2
# Fri, 28 Oct 2022 00:17:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 28 Oct 2022 00:17:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:24 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6193ab94a0498ba6454e2a35e189837b37a2eb01403e8b62654bdc28a4569c`  
		Last Modified: Mon, 17 Oct 2022 21:52:22 GMT  
		Size: 849.2 MB (849228999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777120ea710a4a6c96e29b0896d6ba5301aeabc76ebc7746bdaf630026ceb3dd`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178f4f6f90f6bab4aaf8342187d088536e8a65bce5b71a78c8775ab21d57dc39`  
		Last Modified: Fri, 28 Oct 2022 00:18:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64be820df0d316e845aeaa24d9714941dc6038fb96c3af1ae68ce7de1304a0b`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7711c2ad12dd348b7559e313bb366a27c48900fb880fc0e18562ab742ce5e6`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 357.8 KB (357788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d41267dcad8d27b3da89455553106bf0cafab939c7e8ba37b7aa2a3c7bfb46d`  
		Last Modified: Fri, 28 Oct 2022 00:18:18 GMT  
		Size: 5.3 MB (5305490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7434c9c183776b09625ce99d06e361a904e516542812ffb699420f5a5a150394`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a4aaaadc6896c5cdcd54e586dc2512c4925eff8b4545ab14d6b23f33aaf1ec`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56300ead49ee511a9bd2dd1eb8849af5673a6f85d81158b22a3ab7349dbd4be4`  
		Last Modified: Fri, 28 Oct 2022 00:18:17 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1e5f72226f5d2f9b0094bf2b7fa505f3ebcea3bea5157a66f1fdce6147bb07`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:34942deb3974eeb9aba6ad97a4ab5407ec2e93cf847dcf4a77117261364b0443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:05a4c0bc8897ddeeb9ddb1473028d9e1c9a0a2cb389516b11578c02f9ec8720f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4911098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c9c625dbef5ec34ca7dceca2ce480b3eb978932e2254e6cfe95c15eb9bb28b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:b9e75e481ae9d301a798308347b654037f5ea8bd8ce2eb3b62d56f1d0fb9aa31 in /nats-server 
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:19:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:19:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:19:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de750ae4d2f684dc52058ab61a992122d85ea9cd1a2c7d449a42ea52d637ca18`  
		Last Modified: Fri, 28 Oct 2022 00:20:46 GMT  
		Size: 4.9 MB (4910589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b72f1a5adda7df074f0eb3d095e5b1300624cd78ef32ff0c78927402b93d0e`  
		Last Modified: Fri, 28 Oct 2022 00:20:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:6a348db5fdde022e586e4fe00252f5207f73386b543dad2b9c791c926472bf98
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4678079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d212b3f530fd382de8872a80b70481fc4db336913a9a59a503f67eac93938faa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:0fb4e969033ab88575e23537c015c04681107529d9128dd4fb94d4f441cf13ea in /nats-server 
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:34:37 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:34:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:34:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ce7e3dd39763e6d0dc795d5534c1a6b6e722fda5cf6cbea372a78489a04f27e`  
		Last Modified: Fri, 28 Oct 2022 00:36:14 GMT  
		Size: 4.7 MB (4677570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c4367ae4414051a0ffbe623600d5fedcab0f7b5110c0a0d95e8bf78c93cfad`  
		Last Modified: Fri, 28 Oct 2022 00:36:13 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:8cf5bcc23025af97af872f1e5fc8e37f60ef5ce1b99163e840515dbc515c735c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4669750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef35e6a4f18c95e20350eca6fd4dd61d948dce45a42d73088f65d880c4dde5f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 01:12:28 GMT
COPY file:c324c9ced487df787b815eb06f1de7520b3f2f3c23cb313b6b6e692d30dce518 in /nats-server 
# Fri, 28 Oct 2022 01:12:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 01:12:29 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:493666cecebad3f9973ea93e7811c9fb15f833a53618a7c6abc12abc16a828b6`  
		Last Modified: Fri, 28 Oct 2022 01:14:05 GMT  
		Size: 4.7 MB (4669243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b13ae6ba1b3faf170714cacd52b2535f8aaf0f18ea5f16479b9a3a9e2e89159`  
		Last Modified: Fri, 28 Oct 2022 01:14:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:eebe621bb4c2136c03d0ede2969549480d42c0faa54935450acdaa9b90dcd474
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6feb88b2953948859fb8aeb942da3d4917625a55916e864e7d1995f816a108`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:4a2b1fa0bbd909bf79b017ae360815907a983b7b2c3b158abf0ed8a95668fb78 in /nats-server 
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:40:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:40:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca262f3c33011e42391f6b52c9727d27cd46c6b5a6a5ed69851d60e703606850`  
		Last Modified: Fri, 28 Oct 2022 00:40:59 GMT  
		Size: 4.5 MB (4498479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e4d79c576957d7c047001eb103698d3be1cb4784790f6947b14d39851bf550`  
		Last Modified: Fri, 28 Oct 2022 00:40:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:2223d534de4b168e93ee5731584939fef6069904b42e09ca39e4ef46358dd54f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111744859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05e32726d6a3eb6cd30c7f3cfd15eac77097a00adac44dc185b61d03b58e62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Oct 2022 00:17:42 GMT
RUN cmd /S /C #(nop) COPY file:5cda9aa918fe992fe978c90843552eede9fe664f92442d3068d77fa07c27682b in C:\nats-server.exe 
# Fri, 28 Oct 2022 00:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce29f4214f0fb0200b149c387d5e94ee47d5705e9bc7b884331390782282065f`  
		Last Modified: Thu, 27 Oct 2022 21:23:38 GMT  
		Size: 106.8 MB (106773776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4388e47ca696927a8eab713d6e9905f0069a119b2029c0ddc2d6c8c0f1094157`  
		Last Modified: Fri, 28 Oct 2022 00:18:37 GMT  
		Size: 5.0 MB (4965105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d567bc025c016fe1b38a5f2463f1deb5986fed52de265a356d96e4f782ea04d`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147121d4056552beb6f6f5c897e57e7a81fe46d490dddeb6c410461807b6bf78`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20911c0814537b45d8c70b48e190f3b0a68c11a97b5b3d2745ce9e4d96f4b42`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b8f3033a8d06c06f6986ee485dc4c2f6ee159f98545da2612b238b6c716fcc`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:f8db1a71f146a719842c8d851894fec6e543183c2da4c400f5a2a960ca352102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:03761b5d6c59b37faca88bbd8c37d96613f7ee26012573cc86feb34504bd0051
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8006885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd9e2b47f06b7e327bbbfb1f8baba520cad84321648cf3c142908a9551d86e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:19:47 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:19:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:19:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:19:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:19:49 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:19:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d00bd5b211d6d2259e1123fc716bc7778fb4f2ef8140aebc9a600e7691d7251`  
		Last Modified: Fri, 28 Oct 2022 00:20:23 GMT  
		Size: 5.2 MB (5199832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa3b3a919296293971047f3b55bab13f38c874ad3ee595a4ee9de57c4e1e176`  
		Last Modified: Fri, 28 Oct 2022 00:20:22 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9fdb9eee2a7eda4133115ecd218dd98b7afa1de02bda16dfc85a1f544b5a14`  
		Last Modified: Fri, 28 Oct 2022 00:20:22 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:48c4cd343809a6f219ca8643b99ee9540ee1018c6b6108e1056188c0d54b0910
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7574875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c98fab4f18b0ccd35c5999b24a1e85fc4e09ee832ec2941809c47a74708517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:34:22 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:34:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:34:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:34:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:34:25 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:34:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bec236bdb0c174a608728f09fa7bb201e34846e10c96aa0a3cb0da4ce0e064`  
		Last Modified: Fri, 28 Oct 2022 00:35:40 GMT  
		Size: 5.0 MB (4959934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e35b5ff49cea58009b9004b126d99f234f6932652392dd2b286ad2cddc6453`  
		Last Modified: Fri, 28 Oct 2022 00:35:39 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013802adfa3f871235a505bf256abffbaa8ee6af1dd143af6e427e542f1cec3c`  
		Last Modified: Fri, 28 Oct 2022 00:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:fafa9ed028325662750ff07f25939a66aac303a0b50bca635cd6b33f48683f3d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7372975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f22484361778a7e488b1496ff292a52b4bfb779267fee6dc8a99d5171b119b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 01:12:12 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 01:12:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 01:12:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 01:12:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 01:12:14 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 01:12:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01440488995de9af5b51ae28a139872013b93eda267a46f001cd2615ba9ab0f8`  
		Last Modified: Fri, 28 Oct 2022 01:13:32 GMT  
		Size: 5.0 MB (4954939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aac9b75327e61f497ade56035d2515d5a15073ab8c1a4b1345c46f39e394844`  
		Last Modified: Fri, 28 Oct 2022 01:13:31 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebb5d7ec0dd8b480bcba44b32f9ae5b43d529140b1b68be2d5b1bce9cc8c257`  
		Last Modified: Fri, 28 Oct 2022 01:13:31 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:879ce95c8afa3059b0b8858ce8ad18ada3bb72700c6e6ff296efc6ffebd7e20d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c212d4563965c7102edd4e79355e3907e054df45a0d2df3c1a9c2e73d28c6bc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:40:01 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:40:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:40:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:40:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:40:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:40:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbcbe919967004774a1fa79409186b285f24a7e631c6fb2e6bbf2a95cda9caf`  
		Last Modified: Fri, 28 Oct 2022 00:40:35 GMT  
		Size: 4.8 MB (4782894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659a3f4a00fc9e66e3816eb4310fdbbc3c1e488c97b2b3a780cc4b3fbc9ae486`  
		Last Modified: Fri, 28 Oct 2022 00:40:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a64ad8526321dd00599ac40ef36787222c36b765f37a5a446005c6b31b6862`  
		Last Modified: Fri, 28 Oct 2022 00:40:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.16`

```console
$ docker pull nats@sha256:f8db1a71f146a719842c8d851894fec6e543183c2da4c400f5a2a960ca352102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:03761b5d6c59b37faca88bbd8c37d96613f7ee26012573cc86feb34504bd0051
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8006885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd9e2b47f06b7e327bbbfb1f8baba520cad84321648cf3c142908a9551d86e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:19:47 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:19:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:19:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:19:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:19:49 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:19:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d00bd5b211d6d2259e1123fc716bc7778fb4f2ef8140aebc9a600e7691d7251`  
		Last Modified: Fri, 28 Oct 2022 00:20:23 GMT  
		Size: 5.2 MB (5199832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa3b3a919296293971047f3b55bab13f38c874ad3ee595a4ee9de57c4e1e176`  
		Last Modified: Fri, 28 Oct 2022 00:20:22 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9fdb9eee2a7eda4133115ecd218dd98b7afa1de02bda16dfc85a1f544b5a14`  
		Last Modified: Fri, 28 Oct 2022 00:20:22 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:48c4cd343809a6f219ca8643b99ee9540ee1018c6b6108e1056188c0d54b0910
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7574875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c98fab4f18b0ccd35c5999b24a1e85fc4e09ee832ec2941809c47a74708517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:34:22 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:34:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:34:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:34:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:34:25 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:34:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bec236bdb0c174a608728f09fa7bb201e34846e10c96aa0a3cb0da4ce0e064`  
		Last Modified: Fri, 28 Oct 2022 00:35:40 GMT  
		Size: 5.0 MB (4959934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e35b5ff49cea58009b9004b126d99f234f6932652392dd2b286ad2cddc6453`  
		Last Modified: Fri, 28 Oct 2022 00:35:39 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013802adfa3f871235a505bf256abffbaa8ee6af1dd143af6e427e542f1cec3c`  
		Last Modified: Fri, 28 Oct 2022 00:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:fafa9ed028325662750ff07f25939a66aac303a0b50bca635cd6b33f48683f3d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7372975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f22484361778a7e488b1496ff292a52b4bfb779267fee6dc8a99d5171b119b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 01:12:12 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 01:12:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 01:12:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 01:12:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 01:12:14 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 01:12:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01440488995de9af5b51ae28a139872013b93eda267a46f001cd2615ba9ab0f8`  
		Last Modified: Fri, 28 Oct 2022 01:13:32 GMT  
		Size: 5.0 MB (4954939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aac9b75327e61f497ade56035d2515d5a15073ab8c1a4b1345c46f39e394844`  
		Last Modified: Fri, 28 Oct 2022 01:13:31 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebb5d7ec0dd8b480bcba44b32f9ae5b43d529140b1b68be2d5b1bce9cc8c257`  
		Last Modified: Fri, 28 Oct 2022 01:13:31 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:879ce95c8afa3059b0b8858ce8ad18ada3bb72700c6e6ff296efc6ffebd7e20d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c212d4563965c7102edd4e79355e3907e054df45a0d2df3c1a9c2e73d28c6bc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:40:01 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:40:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:40:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:40:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:40:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:40:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbcbe919967004774a1fa79409186b285f24a7e631c6fb2e6bbf2a95cda9caf`  
		Last Modified: Fri, 28 Oct 2022 00:40:35 GMT  
		Size: 4.8 MB (4782894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659a3f4a00fc9e66e3816eb4310fdbbc3c1e488c97b2b3a780cc4b3fbc9ae486`  
		Last Modified: Fri, 28 Oct 2022 00:40:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a64ad8526321dd00599ac40ef36787222c36b765f37a5a446005c6b31b6862`  
		Last Modified: Fri, 28 Oct 2022 00:40:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:806d56dd55acbc6497c5cc9ff5916b36ba091212c7308b3a23a1098876e686f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:05a4c0bc8897ddeeb9ddb1473028d9e1c9a0a2cb389516b11578c02f9ec8720f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4911098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c9c625dbef5ec34ca7dceca2ce480b3eb978932e2254e6cfe95c15eb9bb28b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:b9e75e481ae9d301a798308347b654037f5ea8bd8ce2eb3b62d56f1d0fb9aa31 in /nats-server 
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:19:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:19:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:19:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de750ae4d2f684dc52058ab61a992122d85ea9cd1a2c7d449a42ea52d637ca18`  
		Last Modified: Fri, 28 Oct 2022 00:20:46 GMT  
		Size: 4.9 MB (4910589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b72f1a5adda7df074f0eb3d095e5b1300624cd78ef32ff0c78927402b93d0e`  
		Last Modified: Fri, 28 Oct 2022 00:20:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:6a348db5fdde022e586e4fe00252f5207f73386b543dad2b9c791c926472bf98
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4678079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d212b3f530fd382de8872a80b70481fc4db336913a9a59a503f67eac93938faa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:0fb4e969033ab88575e23537c015c04681107529d9128dd4fb94d4f441cf13ea in /nats-server 
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:34:37 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:34:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:34:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ce7e3dd39763e6d0dc795d5534c1a6b6e722fda5cf6cbea372a78489a04f27e`  
		Last Modified: Fri, 28 Oct 2022 00:36:14 GMT  
		Size: 4.7 MB (4677570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c4367ae4414051a0ffbe623600d5fedcab0f7b5110c0a0d95e8bf78c93cfad`  
		Last Modified: Fri, 28 Oct 2022 00:36:13 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:8cf5bcc23025af97af872f1e5fc8e37f60ef5ce1b99163e840515dbc515c735c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4669750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef35e6a4f18c95e20350eca6fd4dd61d948dce45a42d73088f65d880c4dde5f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 01:12:28 GMT
COPY file:c324c9ced487df787b815eb06f1de7520b3f2f3c23cb313b6b6e692d30dce518 in /nats-server 
# Fri, 28 Oct 2022 01:12:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 01:12:29 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:493666cecebad3f9973ea93e7811c9fb15f833a53618a7c6abc12abc16a828b6`  
		Last Modified: Fri, 28 Oct 2022 01:14:05 GMT  
		Size: 4.7 MB (4669243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b13ae6ba1b3faf170714cacd52b2535f8aaf0f18ea5f16479b9a3a9e2e89159`  
		Last Modified: Fri, 28 Oct 2022 01:14:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:eebe621bb4c2136c03d0ede2969549480d42c0faa54935450acdaa9b90dcd474
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6feb88b2953948859fb8aeb942da3d4917625a55916e864e7d1995f816a108`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:4a2b1fa0bbd909bf79b017ae360815907a983b7b2c3b158abf0ed8a95668fb78 in /nats-server 
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:40:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:40:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca262f3c33011e42391f6b52c9727d27cd46c6b5a6a5ed69851d60e703606850`  
		Last Modified: Fri, 28 Oct 2022 00:40:59 GMT  
		Size: 4.5 MB (4498479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e4d79c576957d7c047001eb103698d3be1cb4784790f6947b14d39851bf550`  
		Last Modified: Fri, 28 Oct 2022 00:40:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:fafc6597b93f9cbe091b8309cf8ae5f413fcdac1263da3b9c407becbb4edf56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:2223d534de4b168e93ee5731584939fef6069904b42e09ca39e4ef46358dd54f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111744859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05e32726d6a3eb6cd30c7f3cfd15eac77097a00adac44dc185b61d03b58e62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Oct 2022 00:17:42 GMT
RUN cmd /S /C #(nop) COPY file:5cda9aa918fe992fe978c90843552eede9fe664f92442d3068d77fa07c27682b in C:\nats-server.exe 
# Fri, 28 Oct 2022 00:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce29f4214f0fb0200b149c387d5e94ee47d5705e9bc7b884331390782282065f`  
		Last Modified: Thu, 27 Oct 2022 21:23:38 GMT  
		Size: 106.8 MB (106773776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4388e47ca696927a8eab713d6e9905f0069a119b2029c0ddc2d6c8c0f1094157`  
		Last Modified: Fri, 28 Oct 2022 00:18:37 GMT  
		Size: 5.0 MB (4965105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d567bc025c016fe1b38a5f2463f1deb5986fed52de265a356d96e4f782ea04d`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147121d4056552beb6f6f5c897e57e7a81fe46d490dddeb6c410461807b6bf78`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20911c0814537b45d8c70b48e190f3b0a68c11a97b5b3d2745ce9e4d96f4b42`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b8f3033a8d06c06f6986ee485dc4c2f6ee159f98545da2612b238b6c716fcc`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:fafc6597b93f9cbe091b8309cf8ae5f413fcdac1263da3b9c407becbb4edf56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:2223d534de4b168e93ee5731584939fef6069904b42e09ca39e4ef46358dd54f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111744859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05e32726d6a3eb6cd30c7f3cfd15eac77097a00adac44dc185b61d03b58e62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Oct 2022 00:17:42 GMT
RUN cmd /S /C #(nop) COPY file:5cda9aa918fe992fe978c90843552eede9fe664f92442d3068d77fa07c27682b in C:\nats-server.exe 
# Fri, 28 Oct 2022 00:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce29f4214f0fb0200b149c387d5e94ee47d5705e9bc7b884331390782282065f`  
		Last Modified: Thu, 27 Oct 2022 21:23:38 GMT  
		Size: 106.8 MB (106773776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4388e47ca696927a8eab713d6e9905f0069a119b2029c0ddc2d6c8c0f1094157`  
		Last Modified: Fri, 28 Oct 2022 00:18:37 GMT  
		Size: 5.0 MB (4965105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d567bc025c016fe1b38a5f2463f1deb5986fed52de265a356d96e4f782ea04d`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147121d4056552beb6f6f5c897e57e7a81fe46d490dddeb6c410461807b6bf78`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20911c0814537b45d8c70b48e190f3b0a68c11a97b5b3d2745ce9e4d96f4b42`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b8f3033a8d06c06f6986ee485dc4c2f6ee159f98545da2612b238b6c716fcc`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:806d56dd55acbc6497c5cc9ff5916b36ba091212c7308b3a23a1098876e686f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:05a4c0bc8897ddeeb9ddb1473028d9e1c9a0a2cb389516b11578c02f9ec8720f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4911098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c9c625dbef5ec34ca7dceca2ce480b3eb978932e2254e6cfe95c15eb9bb28b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:b9e75e481ae9d301a798308347b654037f5ea8bd8ce2eb3b62d56f1d0fb9aa31 in /nats-server 
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:19:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:19:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:19:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de750ae4d2f684dc52058ab61a992122d85ea9cd1a2c7d449a42ea52d637ca18`  
		Last Modified: Fri, 28 Oct 2022 00:20:46 GMT  
		Size: 4.9 MB (4910589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b72f1a5adda7df074f0eb3d095e5b1300624cd78ef32ff0c78927402b93d0e`  
		Last Modified: Fri, 28 Oct 2022 00:20:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:6a348db5fdde022e586e4fe00252f5207f73386b543dad2b9c791c926472bf98
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4678079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d212b3f530fd382de8872a80b70481fc4db336913a9a59a503f67eac93938faa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:0fb4e969033ab88575e23537c015c04681107529d9128dd4fb94d4f441cf13ea in /nats-server 
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:34:37 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:34:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:34:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ce7e3dd39763e6d0dc795d5534c1a6b6e722fda5cf6cbea372a78489a04f27e`  
		Last Modified: Fri, 28 Oct 2022 00:36:14 GMT  
		Size: 4.7 MB (4677570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c4367ae4414051a0ffbe623600d5fedcab0f7b5110c0a0d95e8bf78c93cfad`  
		Last Modified: Fri, 28 Oct 2022 00:36:13 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:8cf5bcc23025af97af872f1e5fc8e37f60ef5ce1b99163e840515dbc515c735c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4669750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef35e6a4f18c95e20350eca6fd4dd61d948dce45a42d73088f65d880c4dde5f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 01:12:28 GMT
COPY file:c324c9ced487df787b815eb06f1de7520b3f2f3c23cb313b6b6e692d30dce518 in /nats-server 
# Fri, 28 Oct 2022 01:12:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 01:12:29 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:493666cecebad3f9973ea93e7811c9fb15f833a53618a7c6abc12abc16a828b6`  
		Last Modified: Fri, 28 Oct 2022 01:14:05 GMT  
		Size: 4.7 MB (4669243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b13ae6ba1b3faf170714cacd52b2535f8aaf0f18ea5f16479b9a3a9e2e89159`  
		Last Modified: Fri, 28 Oct 2022 01:14:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:eebe621bb4c2136c03d0ede2969549480d42c0faa54935450acdaa9b90dcd474
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6feb88b2953948859fb8aeb942da3d4917625a55916e864e7d1995f816a108`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:4a2b1fa0bbd909bf79b017ae360815907a983b7b2c3b158abf0ed8a95668fb78 in /nats-server 
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:40:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:40:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca262f3c33011e42391f6b52c9727d27cd46c6b5a6a5ed69851d60e703606850`  
		Last Modified: Fri, 28 Oct 2022 00:40:59 GMT  
		Size: 4.5 MB (4498479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e4d79c576957d7c047001eb103698d3be1cb4784790f6947b14d39851bf550`  
		Last Modified: Fri, 28 Oct 2022 00:40:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:fdb8994491270872284ca4358bc66e164b2f6fa02e5189163b51cb8df71bc276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:43e84da881b4607236ff0f9158fe2215c782c94b01effb76af5fb9831a594fcb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2779174179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab33aded854a32b758ffbe80d2425e85d79fe5e68257d305b54bf4661ce0ab5f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Fri, 28 Oct 2022 00:14:59 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:14:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.4/nats-server-v2.9.4-windows-amd64.zip
# Fri, 28 Oct 2022 00:15:01 GMT
ENV NATS_SERVER_SHASUM=ba5d135b14bb4f4c106639c6f0b3fe5530b4e9ec4dd2c4e3b83f78c0e808e435
# Fri, 28 Oct 2022 00:15:53 GMT
RUN Set-PSDebug -Trace 2
# Fri, 28 Oct 2022 00:17:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 28 Oct 2022 00:17:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:24 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6193ab94a0498ba6454e2a35e189837b37a2eb01403e8b62654bdc28a4569c`  
		Last Modified: Mon, 17 Oct 2022 21:52:22 GMT  
		Size: 849.2 MB (849228999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777120ea710a4a6c96e29b0896d6ba5301aeabc76ebc7746bdaf630026ceb3dd`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178f4f6f90f6bab4aaf8342187d088536e8a65bce5b71a78c8775ab21d57dc39`  
		Last Modified: Fri, 28 Oct 2022 00:18:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64be820df0d316e845aeaa24d9714941dc6038fb96c3af1ae68ce7de1304a0b`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7711c2ad12dd348b7559e313bb366a27c48900fb880fc0e18562ab742ce5e6`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 357.8 KB (357788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d41267dcad8d27b3da89455553106bf0cafab939c7e8ba37b7aa2a3c7bfb46d`  
		Last Modified: Fri, 28 Oct 2022 00:18:18 GMT  
		Size: 5.3 MB (5305490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7434c9c183776b09625ce99d06e361a904e516542812ffb699420f5a5a150394`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a4aaaadc6896c5cdcd54e586dc2512c4925eff8b4545ab14d6b23f33aaf1ec`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56300ead49ee511a9bd2dd1eb8849af5673a6f85d81158b22a3ab7349dbd4be4`  
		Last Modified: Fri, 28 Oct 2022 00:18:17 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1e5f72226f5d2f9b0094bf2b7fa505f3ebcea3bea5157a66f1fdce6147bb07`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:fdb8994491270872284ca4358bc66e164b2f6fa02e5189163b51cb8df71bc276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:43e84da881b4607236ff0f9158fe2215c782c94b01effb76af5fb9831a594fcb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2779174179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab33aded854a32b758ffbe80d2425e85d79fe5e68257d305b54bf4661ce0ab5f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Fri, 28 Oct 2022 00:14:59 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:14:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.4/nats-server-v2.9.4-windows-amd64.zip
# Fri, 28 Oct 2022 00:15:01 GMT
ENV NATS_SERVER_SHASUM=ba5d135b14bb4f4c106639c6f0b3fe5530b4e9ec4dd2c4e3b83f78c0e808e435
# Fri, 28 Oct 2022 00:15:53 GMT
RUN Set-PSDebug -Trace 2
# Fri, 28 Oct 2022 00:17:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 28 Oct 2022 00:17:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:24 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6193ab94a0498ba6454e2a35e189837b37a2eb01403e8b62654bdc28a4569c`  
		Last Modified: Mon, 17 Oct 2022 21:52:22 GMT  
		Size: 849.2 MB (849228999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777120ea710a4a6c96e29b0896d6ba5301aeabc76ebc7746bdaf630026ceb3dd`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178f4f6f90f6bab4aaf8342187d088536e8a65bce5b71a78c8775ab21d57dc39`  
		Last Modified: Fri, 28 Oct 2022 00:18:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64be820df0d316e845aeaa24d9714941dc6038fb96c3af1ae68ce7de1304a0b`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7711c2ad12dd348b7559e313bb366a27c48900fb880fc0e18562ab742ce5e6`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 357.8 KB (357788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d41267dcad8d27b3da89455553106bf0cafab939c7e8ba37b7aa2a3c7bfb46d`  
		Last Modified: Fri, 28 Oct 2022 00:18:18 GMT  
		Size: 5.3 MB (5305490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7434c9c183776b09625ce99d06e361a904e516542812ffb699420f5a5a150394`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a4aaaadc6896c5cdcd54e586dc2512c4925eff8b4545ab14d6b23f33aaf1ec`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56300ead49ee511a9bd2dd1eb8849af5673a6f85d81158b22a3ab7349dbd4be4`  
		Last Modified: Fri, 28 Oct 2022 00:18:17 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1e5f72226f5d2f9b0094bf2b7fa505f3ebcea3bea5157a66f1fdce6147bb07`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.4`

```console
$ docker pull nats@sha256:34942deb3974eeb9aba6ad97a4ab5407ec2e93cf847dcf4a77117261364b0443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9.4` - linux; amd64

```console
$ docker pull nats@sha256:05a4c0bc8897ddeeb9ddb1473028d9e1c9a0a2cb389516b11578c02f9ec8720f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4911098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c9c625dbef5ec34ca7dceca2ce480b3eb978932e2254e6cfe95c15eb9bb28b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:b9e75e481ae9d301a798308347b654037f5ea8bd8ce2eb3b62d56f1d0fb9aa31 in /nats-server 
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:19:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:19:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:19:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de750ae4d2f684dc52058ab61a992122d85ea9cd1a2c7d449a42ea52d637ca18`  
		Last Modified: Fri, 28 Oct 2022 00:20:46 GMT  
		Size: 4.9 MB (4910589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b72f1a5adda7df074f0eb3d095e5b1300624cd78ef32ff0c78927402b93d0e`  
		Last Modified: Fri, 28 Oct 2022 00:20:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.4` - linux; arm variant v6

```console
$ docker pull nats@sha256:6a348db5fdde022e586e4fe00252f5207f73386b543dad2b9c791c926472bf98
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4678079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d212b3f530fd382de8872a80b70481fc4db336913a9a59a503f67eac93938faa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:0fb4e969033ab88575e23537c015c04681107529d9128dd4fb94d4f441cf13ea in /nats-server 
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:34:37 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:34:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:34:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ce7e3dd39763e6d0dc795d5534c1a6b6e722fda5cf6cbea372a78489a04f27e`  
		Last Modified: Fri, 28 Oct 2022 00:36:14 GMT  
		Size: 4.7 MB (4677570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c4367ae4414051a0ffbe623600d5fedcab0f7b5110c0a0d95e8bf78c93cfad`  
		Last Modified: Fri, 28 Oct 2022 00:36:13 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.4` - linux; arm variant v7

```console
$ docker pull nats@sha256:8cf5bcc23025af97af872f1e5fc8e37f60ef5ce1b99163e840515dbc515c735c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4669750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef35e6a4f18c95e20350eca6fd4dd61d948dce45a42d73088f65d880c4dde5f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 01:12:28 GMT
COPY file:c324c9ced487df787b815eb06f1de7520b3f2f3c23cb313b6b6e692d30dce518 in /nats-server 
# Fri, 28 Oct 2022 01:12:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 01:12:29 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:493666cecebad3f9973ea93e7811c9fb15f833a53618a7c6abc12abc16a828b6`  
		Last Modified: Fri, 28 Oct 2022 01:14:05 GMT  
		Size: 4.7 MB (4669243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b13ae6ba1b3faf170714cacd52b2535f8aaf0f18ea5f16479b9a3a9e2e89159`  
		Last Modified: Fri, 28 Oct 2022 01:14:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.4` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:eebe621bb4c2136c03d0ede2969549480d42c0faa54935450acdaa9b90dcd474
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6feb88b2953948859fb8aeb942da3d4917625a55916e864e7d1995f816a108`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:4a2b1fa0bbd909bf79b017ae360815907a983b7b2c3b158abf0ed8a95668fb78 in /nats-server 
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:40:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:40:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca262f3c33011e42391f6b52c9727d27cd46c6b5a6a5ed69851d60e703606850`  
		Last Modified: Fri, 28 Oct 2022 00:40:59 GMT  
		Size: 4.5 MB (4498479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e4d79c576957d7c047001eb103698d3be1cb4784790f6947b14d39851bf550`  
		Last Modified: Fri, 28 Oct 2022 00:40:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.4` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:2223d534de4b168e93ee5731584939fef6069904b42e09ca39e4ef46358dd54f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111744859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05e32726d6a3eb6cd30c7f3cfd15eac77097a00adac44dc185b61d03b58e62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Oct 2022 00:17:42 GMT
RUN cmd /S /C #(nop) COPY file:5cda9aa918fe992fe978c90843552eede9fe664f92442d3068d77fa07c27682b in C:\nats-server.exe 
# Fri, 28 Oct 2022 00:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce29f4214f0fb0200b149c387d5e94ee47d5705e9bc7b884331390782282065f`  
		Last Modified: Thu, 27 Oct 2022 21:23:38 GMT  
		Size: 106.8 MB (106773776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4388e47ca696927a8eab713d6e9905f0069a119b2029c0ddc2d6c8c0f1094157`  
		Last Modified: Fri, 28 Oct 2022 00:18:37 GMT  
		Size: 5.0 MB (4965105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d567bc025c016fe1b38a5f2463f1deb5986fed52de265a356d96e4f782ea04d`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147121d4056552beb6f6f5c897e57e7a81fe46d490dddeb6c410461807b6bf78`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20911c0814537b45d8c70b48e190f3b0a68c11a97b5b3d2745ce9e4d96f4b42`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b8f3033a8d06c06f6986ee485dc4c2f6ee159f98545da2612b238b6c716fcc`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.4-alpine`

```console
$ docker pull nats@sha256:f8db1a71f146a719842c8d851894fec6e543183c2da4c400f5a2a960ca352102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.4-alpine` - linux; amd64

```console
$ docker pull nats@sha256:03761b5d6c59b37faca88bbd8c37d96613f7ee26012573cc86feb34504bd0051
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8006885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd9e2b47f06b7e327bbbfb1f8baba520cad84321648cf3c142908a9551d86e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:19:47 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:19:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:19:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:19:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:19:49 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:19:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d00bd5b211d6d2259e1123fc716bc7778fb4f2ef8140aebc9a600e7691d7251`  
		Last Modified: Fri, 28 Oct 2022 00:20:23 GMT  
		Size: 5.2 MB (5199832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa3b3a919296293971047f3b55bab13f38c874ad3ee595a4ee9de57c4e1e176`  
		Last Modified: Fri, 28 Oct 2022 00:20:22 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9fdb9eee2a7eda4133115ecd218dd98b7afa1de02bda16dfc85a1f544b5a14`  
		Last Modified: Fri, 28 Oct 2022 00:20:22 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.4-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:48c4cd343809a6f219ca8643b99ee9540ee1018c6b6108e1056188c0d54b0910
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7574875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c98fab4f18b0ccd35c5999b24a1e85fc4e09ee832ec2941809c47a74708517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:34:22 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:34:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:34:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:34:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:34:25 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:34:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bec236bdb0c174a608728f09fa7bb201e34846e10c96aa0a3cb0da4ce0e064`  
		Last Modified: Fri, 28 Oct 2022 00:35:40 GMT  
		Size: 5.0 MB (4959934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e35b5ff49cea58009b9004b126d99f234f6932652392dd2b286ad2cddc6453`  
		Last Modified: Fri, 28 Oct 2022 00:35:39 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013802adfa3f871235a505bf256abffbaa8ee6af1dd143af6e427e542f1cec3c`  
		Last Modified: Fri, 28 Oct 2022 00:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.4-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:fafa9ed028325662750ff07f25939a66aac303a0b50bca635cd6b33f48683f3d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7372975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f22484361778a7e488b1496ff292a52b4bfb779267fee6dc8a99d5171b119b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 01:12:12 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 01:12:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 01:12:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 01:12:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 01:12:14 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 01:12:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01440488995de9af5b51ae28a139872013b93eda267a46f001cd2615ba9ab0f8`  
		Last Modified: Fri, 28 Oct 2022 01:13:32 GMT  
		Size: 5.0 MB (4954939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aac9b75327e61f497ade56035d2515d5a15073ab8c1a4b1345c46f39e394844`  
		Last Modified: Fri, 28 Oct 2022 01:13:31 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebb5d7ec0dd8b480bcba44b32f9ae5b43d529140b1b68be2d5b1bce9cc8c257`  
		Last Modified: Fri, 28 Oct 2022 01:13:31 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.4-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:879ce95c8afa3059b0b8858ce8ad18ada3bb72700c6e6ff296efc6ffebd7e20d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c212d4563965c7102edd4e79355e3907e054df45a0d2df3c1a9c2e73d28c6bc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:40:01 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:40:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:40:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:40:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:40:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:40:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbcbe919967004774a1fa79409186b285f24a7e631c6fb2e6bbf2a95cda9caf`  
		Last Modified: Fri, 28 Oct 2022 00:40:35 GMT  
		Size: 4.8 MB (4782894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659a3f4a00fc9e66e3816eb4310fdbbc3c1e488c97b2b3a780cc4b3fbc9ae486`  
		Last Modified: Fri, 28 Oct 2022 00:40:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a64ad8526321dd00599ac40ef36787222c36b765f37a5a446005c6b31b6862`  
		Last Modified: Fri, 28 Oct 2022 00:40:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.4-alpine3.16`

```console
$ docker pull nats@sha256:f8db1a71f146a719842c8d851894fec6e543183c2da4c400f5a2a960ca352102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.4-alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:03761b5d6c59b37faca88bbd8c37d96613f7ee26012573cc86feb34504bd0051
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8006885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd9e2b47f06b7e327bbbfb1f8baba520cad84321648cf3c142908a9551d86e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:19:47 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:19:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:19:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:19:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:19:49 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:19:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d00bd5b211d6d2259e1123fc716bc7778fb4f2ef8140aebc9a600e7691d7251`  
		Last Modified: Fri, 28 Oct 2022 00:20:23 GMT  
		Size: 5.2 MB (5199832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa3b3a919296293971047f3b55bab13f38c874ad3ee595a4ee9de57c4e1e176`  
		Last Modified: Fri, 28 Oct 2022 00:20:22 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9fdb9eee2a7eda4133115ecd218dd98b7afa1de02bda16dfc85a1f544b5a14`  
		Last Modified: Fri, 28 Oct 2022 00:20:22 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.4-alpine3.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:48c4cd343809a6f219ca8643b99ee9540ee1018c6b6108e1056188c0d54b0910
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7574875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c98fab4f18b0ccd35c5999b24a1e85fc4e09ee832ec2941809c47a74708517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:34:22 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:34:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:34:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:34:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:34:25 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:34:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bec236bdb0c174a608728f09fa7bb201e34846e10c96aa0a3cb0da4ce0e064`  
		Last Modified: Fri, 28 Oct 2022 00:35:40 GMT  
		Size: 5.0 MB (4959934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e35b5ff49cea58009b9004b126d99f234f6932652392dd2b286ad2cddc6453`  
		Last Modified: Fri, 28 Oct 2022 00:35:39 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013802adfa3f871235a505bf256abffbaa8ee6af1dd143af6e427e542f1cec3c`  
		Last Modified: Fri, 28 Oct 2022 00:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.4-alpine3.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:fafa9ed028325662750ff07f25939a66aac303a0b50bca635cd6b33f48683f3d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7372975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f22484361778a7e488b1496ff292a52b4bfb779267fee6dc8a99d5171b119b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 01:12:12 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 01:12:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 01:12:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 01:12:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 01:12:14 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 01:12:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01440488995de9af5b51ae28a139872013b93eda267a46f001cd2615ba9ab0f8`  
		Last Modified: Fri, 28 Oct 2022 01:13:32 GMT  
		Size: 5.0 MB (4954939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aac9b75327e61f497ade56035d2515d5a15073ab8c1a4b1345c46f39e394844`  
		Last Modified: Fri, 28 Oct 2022 01:13:31 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebb5d7ec0dd8b480bcba44b32f9ae5b43d529140b1b68be2d5b1bce9cc8c257`  
		Last Modified: Fri, 28 Oct 2022 01:13:31 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.4-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:879ce95c8afa3059b0b8858ce8ad18ada3bb72700c6e6ff296efc6ffebd7e20d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c212d4563965c7102edd4e79355e3907e054df45a0d2df3c1a9c2e73d28c6bc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:40:01 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:40:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:40:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:40:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:40:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:40:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbcbe919967004774a1fa79409186b285f24a7e631c6fb2e6bbf2a95cda9caf`  
		Last Modified: Fri, 28 Oct 2022 00:40:35 GMT  
		Size: 4.8 MB (4782894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659a3f4a00fc9e66e3816eb4310fdbbc3c1e488c97b2b3a780cc4b3fbc9ae486`  
		Last Modified: Fri, 28 Oct 2022 00:40:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a64ad8526321dd00599ac40ef36787222c36b765f37a5a446005c6b31b6862`  
		Last Modified: Fri, 28 Oct 2022 00:40:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.4-linux`

```console
$ docker pull nats@sha256:806d56dd55acbc6497c5cc9ff5916b36ba091212c7308b3a23a1098876e686f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.4-linux` - linux; amd64

```console
$ docker pull nats@sha256:05a4c0bc8897ddeeb9ddb1473028d9e1c9a0a2cb389516b11578c02f9ec8720f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4911098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c9c625dbef5ec34ca7dceca2ce480b3eb978932e2254e6cfe95c15eb9bb28b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:b9e75e481ae9d301a798308347b654037f5ea8bd8ce2eb3b62d56f1d0fb9aa31 in /nats-server 
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:19:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:19:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:19:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de750ae4d2f684dc52058ab61a992122d85ea9cd1a2c7d449a42ea52d637ca18`  
		Last Modified: Fri, 28 Oct 2022 00:20:46 GMT  
		Size: 4.9 MB (4910589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b72f1a5adda7df074f0eb3d095e5b1300624cd78ef32ff0c78927402b93d0e`  
		Last Modified: Fri, 28 Oct 2022 00:20:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.4-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:6a348db5fdde022e586e4fe00252f5207f73386b543dad2b9c791c926472bf98
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4678079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d212b3f530fd382de8872a80b70481fc4db336913a9a59a503f67eac93938faa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:0fb4e969033ab88575e23537c015c04681107529d9128dd4fb94d4f441cf13ea in /nats-server 
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:34:37 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:34:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:34:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ce7e3dd39763e6d0dc795d5534c1a6b6e722fda5cf6cbea372a78489a04f27e`  
		Last Modified: Fri, 28 Oct 2022 00:36:14 GMT  
		Size: 4.7 MB (4677570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c4367ae4414051a0ffbe623600d5fedcab0f7b5110c0a0d95e8bf78c93cfad`  
		Last Modified: Fri, 28 Oct 2022 00:36:13 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.4-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:8cf5bcc23025af97af872f1e5fc8e37f60ef5ce1b99163e840515dbc515c735c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4669750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef35e6a4f18c95e20350eca6fd4dd61d948dce45a42d73088f65d880c4dde5f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 01:12:28 GMT
COPY file:c324c9ced487df787b815eb06f1de7520b3f2f3c23cb313b6b6e692d30dce518 in /nats-server 
# Fri, 28 Oct 2022 01:12:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 01:12:29 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:493666cecebad3f9973ea93e7811c9fb15f833a53618a7c6abc12abc16a828b6`  
		Last Modified: Fri, 28 Oct 2022 01:14:05 GMT  
		Size: 4.7 MB (4669243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b13ae6ba1b3faf170714cacd52b2535f8aaf0f18ea5f16479b9a3a9e2e89159`  
		Last Modified: Fri, 28 Oct 2022 01:14:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.4-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:eebe621bb4c2136c03d0ede2969549480d42c0faa54935450acdaa9b90dcd474
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6feb88b2953948859fb8aeb942da3d4917625a55916e864e7d1995f816a108`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:4a2b1fa0bbd909bf79b017ae360815907a983b7b2c3b158abf0ed8a95668fb78 in /nats-server 
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:40:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:40:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca262f3c33011e42391f6b52c9727d27cd46c6b5a6a5ed69851d60e703606850`  
		Last Modified: Fri, 28 Oct 2022 00:40:59 GMT  
		Size: 4.5 MB (4498479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e4d79c576957d7c047001eb103698d3be1cb4784790f6947b14d39851bf550`  
		Last Modified: Fri, 28 Oct 2022 00:40:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.4-nanoserver`

```console
$ docker pull nats@sha256:fafc6597b93f9cbe091b8309cf8ae5f413fcdac1263da3b9c407becbb4edf56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9.4-nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:2223d534de4b168e93ee5731584939fef6069904b42e09ca39e4ef46358dd54f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111744859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05e32726d6a3eb6cd30c7f3cfd15eac77097a00adac44dc185b61d03b58e62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Oct 2022 00:17:42 GMT
RUN cmd /S /C #(nop) COPY file:5cda9aa918fe992fe978c90843552eede9fe664f92442d3068d77fa07c27682b in C:\nats-server.exe 
# Fri, 28 Oct 2022 00:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce29f4214f0fb0200b149c387d5e94ee47d5705e9bc7b884331390782282065f`  
		Last Modified: Thu, 27 Oct 2022 21:23:38 GMT  
		Size: 106.8 MB (106773776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4388e47ca696927a8eab713d6e9905f0069a119b2029c0ddc2d6c8c0f1094157`  
		Last Modified: Fri, 28 Oct 2022 00:18:37 GMT  
		Size: 5.0 MB (4965105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d567bc025c016fe1b38a5f2463f1deb5986fed52de265a356d96e4f782ea04d`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147121d4056552beb6f6f5c897e57e7a81fe46d490dddeb6c410461807b6bf78`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20911c0814537b45d8c70b48e190f3b0a68c11a97b5b3d2745ce9e4d96f4b42`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b8f3033a8d06c06f6986ee485dc4c2f6ee159f98545da2612b238b6c716fcc`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.4-nanoserver-1809`

```console
$ docker pull nats@sha256:fafc6597b93f9cbe091b8309cf8ae5f413fcdac1263da3b9c407becbb4edf56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9.4-nanoserver-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:2223d534de4b168e93ee5731584939fef6069904b42e09ca39e4ef46358dd54f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111744859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05e32726d6a3eb6cd30c7f3cfd15eac77097a00adac44dc185b61d03b58e62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Oct 2022 00:17:42 GMT
RUN cmd /S /C #(nop) COPY file:5cda9aa918fe992fe978c90843552eede9fe664f92442d3068d77fa07c27682b in C:\nats-server.exe 
# Fri, 28 Oct 2022 00:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce29f4214f0fb0200b149c387d5e94ee47d5705e9bc7b884331390782282065f`  
		Last Modified: Thu, 27 Oct 2022 21:23:38 GMT  
		Size: 106.8 MB (106773776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4388e47ca696927a8eab713d6e9905f0069a119b2029c0ddc2d6c8c0f1094157`  
		Last Modified: Fri, 28 Oct 2022 00:18:37 GMT  
		Size: 5.0 MB (4965105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d567bc025c016fe1b38a5f2463f1deb5986fed52de265a356d96e4f782ea04d`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147121d4056552beb6f6f5c897e57e7a81fe46d490dddeb6c410461807b6bf78`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20911c0814537b45d8c70b48e190f3b0a68c11a97b5b3d2745ce9e4d96f4b42`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b8f3033a8d06c06f6986ee485dc4c2f6ee159f98545da2612b238b6c716fcc`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.4-scratch`

```console
$ docker pull nats@sha256:806d56dd55acbc6497c5cc9ff5916b36ba091212c7308b3a23a1098876e686f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.4-scratch` - linux; amd64

```console
$ docker pull nats@sha256:05a4c0bc8897ddeeb9ddb1473028d9e1c9a0a2cb389516b11578c02f9ec8720f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4911098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c9c625dbef5ec34ca7dceca2ce480b3eb978932e2254e6cfe95c15eb9bb28b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:b9e75e481ae9d301a798308347b654037f5ea8bd8ce2eb3b62d56f1d0fb9aa31 in /nats-server 
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:19:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:19:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:19:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de750ae4d2f684dc52058ab61a992122d85ea9cd1a2c7d449a42ea52d637ca18`  
		Last Modified: Fri, 28 Oct 2022 00:20:46 GMT  
		Size: 4.9 MB (4910589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b72f1a5adda7df074f0eb3d095e5b1300624cd78ef32ff0c78927402b93d0e`  
		Last Modified: Fri, 28 Oct 2022 00:20:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.4-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:6a348db5fdde022e586e4fe00252f5207f73386b543dad2b9c791c926472bf98
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4678079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d212b3f530fd382de8872a80b70481fc4db336913a9a59a503f67eac93938faa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:0fb4e969033ab88575e23537c015c04681107529d9128dd4fb94d4f441cf13ea in /nats-server 
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:34:37 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:34:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:34:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ce7e3dd39763e6d0dc795d5534c1a6b6e722fda5cf6cbea372a78489a04f27e`  
		Last Modified: Fri, 28 Oct 2022 00:36:14 GMT  
		Size: 4.7 MB (4677570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c4367ae4414051a0ffbe623600d5fedcab0f7b5110c0a0d95e8bf78c93cfad`  
		Last Modified: Fri, 28 Oct 2022 00:36:13 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.4-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:8cf5bcc23025af97af872f1e5fc8e37f60ef5ce1b99163e840515dbc515c735c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4669750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef35e6a4f18c95e20350eca6fd4dd61d948dce45a42d73088f65d880c4dde5f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 01:12:28 GMT
COPY file:c324c9ced487df787b815eb06f1de7520b3f2f3c23cb313b6b6e692d30dce518 in /nats-server 
# Fri, 28 Oct 2022 01:12:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 01:12:29 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:493666cecebad3f9973ea93e7811c9fb15f833a53618a7c6abc12abc16a828b6`  
		Last Modified: Fri, 28 Oct 2022 01:14:05 GMT  
		Size: 4.7 MB (4669243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b13ae6ba1b3faf170714cacd52b2535f8aaf0f18ea5f16479b9a3a9e2e89159`  
		Last Modified: Fri, 28 Oct 2022 01:14:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.4-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:eebe621bb4c2136c03d0ede2969549480d42c0faa54935450acdaa9b90dcd474
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6feb88b2953948859fb8aeb942da3d4917625a55916e864e7d1995f816a108`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:4a2b1fa0bbd909bf79b017ae360815907a983b7b2c3b158abf0ed8a95668fb78 in /nats-server 
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:40:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:40:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca262f3c33011e42391f6b52c9727d27cd46c6b5a6a5ed69851d60e703606850`  
		Last Modified: Fri, 28 Oct 2022 00:40:59 GMT  
		Size: 4.5 MB (4498479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e4d79c576957d7c047001eb103698d3be1cb4784790f6947b14d39851bf550`  
		Last Modified: Fri, 28 Oct 2022 00:40:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.4-windowsservercore`

```console
$ docker pull nats@sha256:fdb8994491270872284ca4358bc66e164b2f6fa02e5189163b51cb8df71bc276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9.4-windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:43e84da881b4607236ff0f9158fe2215c782c94b01effb76af5fb9831a594fcb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2779174179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab33aded854a32b758ffbe80d2425e85d79fe5e68257d305b54bf4661ce0ab5f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Fri, 28 Oct 2022 00:14:59 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:14:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.4/nats-server-v2.9.4-windows-amd64.zip
# Fri, 28 Oct 2022 00:15:01 GMT
ENV NATS_SERVER_SHASUM=ba5d135b14bb4f4c106639c6f0b3fe5530b4e9ec4dd2c4e3b83f78c0e808e435
# Fri, 28 Oct 2022 00:15:53 GMT
RUN Set-PSDebug -Trace 2
# Fri, 28 Oct 2022 00:17:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 28 Oct 2022 00:17:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:24 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6193ab94a0498ba6454e2a35e189837b37a2eb01403e8b62654bdc28a4569c`  
		Last Modified: Mon, 17 Oct 2022 21:52:22 GMT  
		Size: 849.2 MB (849228999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777120ea710a4a6c96e29b0896d6ba5301aeabc76ebc7746bdaf630026ceb3dd`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178f4f6f90f6bab4aaf8342187d088536e8a65bce5b71a78c8775ab21d57dc39`  
		Last Modified: Fri, 28 Oct 2022 00:18:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64be820df0d316e845aeaa24d9714941dc6038fb96c3af1ae68ce7de1304a0b`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7711c2ad12dd348b7559e313bb366a27c48900fb880fc0e18562ab742ce5e6`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 357.8 KB (357788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d41267dcad8d27b3da89455553106bf0cafab939c7e8ba37b7aa2a3c7bfb46d`  
		Last Modified: Fri, 28 Oct 2022 00:18:18 GMT  
		Size: 5.3 MB (5305490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7434c9c183776b09625ce99d06e361a904e516542812ffb699420f5a5a150394`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a4aaaadc6896c5cdcd54e586dc2512c4925eff8b4545ab14d6b23f33aaf1ec`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56300ead49ee511a9bd2dd1eb8849af5673a6f85d81158b22a3ab7349dbd4be4`  
		Last Modified: Fri, 28 Oct 2022 00:18:17 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1e5f72226f5d2f9b0094bf2b7fa505f3ebcea3bea5157a66f1fdce6147bb07`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.4-windowsservercore-1809`

```console
$ docker pull nats@sha256:fdb8994491270872284ca4358bc66e164b2f6fa02e5189163b51cb8df71bc276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:2.9.4-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:43e84da881b4607236ff0f9158fe2215c782c94b01effb76af5fb9831a594fcb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2779174179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab33aded854a32b758ffbe80d2425e85d79fe5e68257d305b54bf4661ce0ab5f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Fri, 28 Oct 2022 00:14:59 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:14:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.4/nats-server-v2.9.4-windows-amd64.zip
# Fri, 28 Oct 2022 00:15:01 GMT
ENV NATS_SERVER_SHASUM=ba5d135b14bb4f4c106639c6f0b3fe5530b4e9ec4dd2c4e3b83f78c0e808e435
# Fri, 28 Oct 2022 00:15:53 GMT
RUN Set-PSDebug -Trace 2
# Fri, 28 Oct 2022 00:17:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 28 Oct 2022 00:17:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:24 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6193ab94a0498ba6454e2a35e189837b37a2eb01403e8b62654bdc28a4569c`  
		Last Modified: Mon, 17 Oct 2022 21:52:22 GMT  
		Size: 849.2 MB (849228999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777120ea710a4a6c96e29b0896d6ba5301aeabc76ebc7746bdaf630026ceb3dd`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178f4f6f90f6bab4aaf8342187d088536e8a65bce5b71a78c8775ab21d57dc39`  
		Last Modified: Fri, 28 Oct 2022 00:18:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64be820df0d316e845aeaa24d9714941dc6038fb96c3af1ae68ce7de1304a0b`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7711c2ad12dd348b7559e313bb366a27c48900fb880fc0e18562ab742ce5e6`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 357.8 KB (357788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d41267dcad8d27b3da89455553106bf0cafab939c7e8ba37b7aa2a3c7bfb46d`  
		Last Modified: Fri, 28 Oct 2022 00:18:18 GMT  
		Size: 5.3 MB (5305490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7434c9c183776b09625ce99d06e361a904e516542812ffb699420f5a5a150394`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a4aaaadc6896c5cdcd54e586dc2512c4925eff8b4545ab14d6b23f33aaf1ec`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56300ead49ee511a9bd2dd1eb8849af5673a6f85d81158b22a3ab7349dbd4be4`  
		Last Modified: Fri, 28 Oct 2022 00:18:17 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1e5f72226f5d2f9b0094bf2b7fa505f3ebcea3bea5157a66f1fdce6147bb07`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:f8db1a71f146a719842c8d851894fec6e543183c2da4c400f5a2a960ca352102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:03761b5d6c59b37faca88bbd8c37d96613f7ee26012573cc86feb34504bd0051
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8006885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd9e2b47f06b7e327bbbfb1f8baba520cad84321648cf3c142908a9551d86e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:19:47 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:19:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:19:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:19:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:19:49 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:19:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d00bd5b211d6d2259e1123fc716bc7778fb4f2ef8140aebc9a600e7691d7251`  
		Last Modified: Fri, 28 Oct 2022 00:20:23 GMT  
		Size: 5.2 MB (5199832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa3b3a919296293971047f3b55bab13f38c874ad3ee595a4ee9de57c4e1e176`  
		Last Modified: Fri, 28 Oct 2022 00:20:22 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9fdb9eee2a7eda4133115ecd218dd98b7afa1de02bda16dfc85a1f544b5a14`  
		Last Modified: Fri, 28 Oct 2022 00:20:22 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:48c4cd343809a6f219ca8643b99ee9540ee1018c6b6108e1056188c0d54b0910
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7574875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c98fab4f18b0ccd35c5999b24a1e85fc4e09ee832ec2941809c47a74708517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:34:22 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:34:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:34:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:34:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:34:25 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:34:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bec236bdb0c174a608728f09fa7bb201e34846e10c96aa0a3cb0da4ce0e064`  
		Last Modified: Fri, 28 Oct 2022 00:35:40 GMT  
		Size: 5.0 MB (4959934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e35b5ff49cea58009b9004b126d99f234f6932652392dd2b286ad2cddc6453`  
		Last Modified: Fri, 28 Oct 2022 00:35:39 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013802adfa3f871235a505bf256abffbaa8ee6af1dd143af6e427e542f1cec3c`  
		Last Modified: Fri, 28 Oct 2022 00:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:fafa9ed028325662750ff07f25939a66aac303a0b50bca635cd6b33f48683f3d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7372975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f22484361778a7e488b1496ff292a52b4bfb779267fee6dc8a99d5171b119b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 01:12:12 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 01:12:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 01:12:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 01:12:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 01:12:14 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 01:12:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01440488995de9af5b51ae28a139872013b93eda267a46f001cd2615ba9ab0f8`  
		Last Modified: Fri, 28 Oct 2022 01:13:32 GMT  
		Size: 5.0 MB (4954939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aac9b75327e61f497ade56035d2515d5a15073ab8c1a4b1345c46f39e394844`  
		Last Modified: Fri, 28 Oct 2022 01:13:31 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebb5d7ec0dd8b480bcba44b32f9ae5b43d529140b1b68be2d5b1bce9cc8c257`  
		Last Modified: Fri, 28 Oct 2022 01:13:31 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:879ce95c8afa3059b0b8858ce8ad18ada3bb72700c6e6ff296efc6ffebd7e20d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c212d4563965c7102edd4e79355e3907e054df45a0d2df3c1a9c2e73d28c6bc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:40:01 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:40:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:40:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:40:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:40:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:40:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbcbe919967004774a1fa79409186b285f24a7e631c6fb2e6bbf2a95cda9caf`  
		Last Modified: Fri, 28 Oct 2022 00:40:35 GMT  
		Size: 4.8 MB (4782894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659a3f4a00fc9e66e3816eb4310fdbbc3c1e488c97b2b3a780cc4b3fbc9ae486`  
		Last Modified: Fri, 28 Oct 2022 00:40:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a64ad8526321dd00599ac40ef36787222c36b765f37a5a446005c6b31b6862`  
		Last Modified: Fri, 28 Oct 2022 00:40:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.16`

```console
$ docker pull nats@sha256:f8db1a71f146a719842c8d851894fec6e543183c2da4c400f5a2a960ca352102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.16` - linux; amd64

```console
$ docker pull nats@sha256:03761b5d6c59b37faca88bbd8c37d96613f7ee26012573cc86feb34504bd0051
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8006885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd9e2b47f06b7e327bbbfb1f8baba520cad84321648cf3c142908a9551d86e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:19:47 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:19:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:19:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:19:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:19:49 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:19:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d00bd5b211d6d2259e1123fc716bc7778fb4f2ef8140aebc9a600e7691d7251`  
		Last Modified: Fri, 28 Oct 2022 00:20:23 GMT  
		Size: 5.2 MB (5199832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa3b3a919296293971047f3b55bab13f38c874ad3ee595a4ee9de57c4e1e176`  
		Last Modified: Fri, 28 Oct 2022 00:20:22 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9fdb9eee2a7eda4133115ecd218dd98b7afa1de02bda16dfc85a1f544b5a14`  
		Last Modified: Fri, 28 Oct 2022 00:20:22 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:48c4cd343809a6f219ca8643b99ee9540ee1018c6b6108e1056188c0d54b0910
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7574875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c98fab4f18b0ccd35c5999b24a1e85fc4e09ee832ec2941809c47a74708517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:34:22 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:34:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:34:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:34:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:34:25 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:34:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bec236bdb0c174a608728f09fa7bb201e34846e10c96aa0a3cb0da4ce0e064`  
		Last Modified: Fri, 28 Oct 2022 00:35:40 GMT  
		Size: 5.0 MB (4959934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e35b5ff49cea58009b9004b126d99f234f6932652392dd2b286ad2cddc6453`  
		Last Modified: Fri, 28 Oct 2022 00:35:39 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013802adfa3f871235a505bf256abffbaa8ee6af1dd143af6e427e542f1cec3c`  
		Last Modified: Fri, 28 Oct 2022 00:35:39 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:fafa9ed028325662750ff07f25939a66aac303a0b50bca635cd6b33f48683f3d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7372975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f22484361778a7e488b1496ff292a52b4bfb779267fee6dc8a99d5171b119b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 01:12:12 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 01:12:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 01:12:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 01:12:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 01:12:14 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 01:12:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01440488995de9af5b51ae28a139872013b93eda267a46f001cd2615ba9ab0f8`  
		Last Modified: Fri, 28 Oct 2022 01:13:32 GMT  
		Size: 5.0 MB (4954939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aac9b75327e61f497ade56035d2515d5a15073ab8c1a4b1345c46f39e394844`  
		Last Modified: Fri, 28 Oct 2022 01:13:31 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebb5d7ec0dd8b480bcba44b32f9ae5b43d529140b1b68be2d5b1bce9cc8c257`  
		Last Modified: Fri, 28 Oct 2022 01:13:31 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:879ce95c8afa3059b0b8858ce8ad18ada3bb72700c6e6ff296efc6ffebd7e20d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c212d4563965c7102edd4e79355e3907e054df45a0d2df3c1a9c2e73d28c6bc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:40:01 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:40:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='4f7a05ed80b8c235b8dd706b49c8b3810680b3cb005ca9573e69362927c211bd' ;; 		armhf) natsArch='arm6'; sha256='40d88777c384d035fa2c7a96d885e31240bbce8a907e96821ac12f8c17d3a471' ;; 		armv7) natsArch='arm7'; sha256='eefa52c70486859f963c0d922a0d69929737caf83006c7d642f94ea61bdbe07a' ;; 		x86_64) natsArch='amd64'; sha256='a2fa39fd0f9e4526f08e309bdced1450b9305674772815838f6db6adc5e99a9b' ;; 		x86) natsArch='386'; sha256='f2a1b755ce1bbd346a8b3415bb8d71522fadf6f3a58fcd92a598be2232318cb4' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 28 Oct 2022 00:40:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 28 Oct 2022 00:40:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 28 Oct 2022 00:40:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Oct 2022 00:40:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbcbe919967004774a1fa79409186b285f24a7e631c6fb2e6bbf2a95cda9caf`  
		Last Modified: Fri, 28 Oct 2022 00:40:35 GMT  
		Size: 4.8 MB (4782894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659a3f4a00fc9e66e3816eb4310fdbbc3c1e488c97b2b3a780cc4b3fbc9ae486`  
		Last Modified: Fri, 28 Oct 2022 00:40:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a64ad8526321dd00599ac40ef36787222c36b765f37a5a446005c6b31b6862`  
		Last Modified: Fri, 28 Oct 2022 00:40:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:34942deb3974eeb9aba6ad97a4ab5407ec2e93cf847dcf4a77117261364b0443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3532; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:05a4c0bc8897ddeeb9ddb1473028d9e1c9a0a2cb389516b11578c02f9ec8720f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4911098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c9c625dbef5ec34ca7dceca2ce480b3eb978932e2254e6cfe95c15eb9bb28b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:b9e75e481ae9d301a798308347b654037f5ea8bd8ce2eb3b62d56f1d0fb9aa31 in /nats-server 
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:19:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:19:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:19:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de750ae4d2f684dc52058ab61a992122d85ea9cd1a2c7d449a42ea52d637ca18`  
		Last Modified: Fri, 28 Oct 2022 00:20:46 GMT  
		Size: 4.9 MB (4910589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b72f1a5adda7df074f0eb3d095e5b1300624cd78ef32ff0c78927402b93d0e`  
		Last Modified: Fri, 28 Oct 2022 00:20:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:6a348db5fdde022e586e4fe00252f5207f73386b543dad2b9c791c926472bf98
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4678079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d212b3f530fd382de8872a80b70481fc4db336913a9a59a503f67eac93938faa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:0fb4e969033ab88575e23537c015c04681107529d9128dd4fb94d4f441cf13ea in /nats-server 
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:34:37 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:34:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:34:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ce7e3dd39763e6d0dc795d5534c1a6b6e722fda5cf6cbea372a78489a04f27e`  
		Last Modified: Fri, 28 Oct 2022 00:36:14 GMT  
		Size: 4.7 MB (4677570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c4367ae4414051a0ffbe623600d5fedcab0f7b5110c0a0d95e8bf78c93cfad`  
		Last Modified: Fri, 28 Oct 2022 00:36:13 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:8cf5bcc23025af97af872f1e5fc8e37f60ef5ce1b99163e840515dbc515c735c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4669750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef35e6a4f18c95e20350eca6fd4dd61d948dce45a42d73088f65d880c4dde5f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 01:12:28 GMT
COPY file:c324c9ced487df787b815eb06f1de7520b3f2f3c23cb313b6b6e692d30dce518 in /nats-server 
# Fri, 28 Oct 2022 01:12:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 01:12:29 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:493666cecebad3f9973ea93e7811c9fb15f833a53618a7c6abc12abc16a828b6`  
		Last Modified: Fri, 28 Oct 2022 01:14:05 GMT  
		Size: 4.7 MB (4669243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b13ae6ba1b3faf170714cacd52b2535f8aaf0f18ea5f16479b9a3a9e2e89159`  
		Last Modified: Fri, 28 Oct 2022 01:14:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:eebe621bb4c2136c03d0ede2969549480d42c0faa54935450acdaa9b90dcd474
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6feb88b2953948859fb8aeb942da3d4917625a55916e864e7d1995f816a108`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:4a2b1fa0bbd909bf79b017ae360815907a983b7b2c3b158abf0ed8a95668fb78 in /nats-server 
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:40:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:40:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca262f3c33011e42391f6b52c9727d27cd46c6b5a6a5ed69851d60e703606850`  
		Last Modified: Fri, 28 Oct 2022 00:40:59 GMT  
		Size: 4.5 MB (4498479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e4d79c576957d7c047001eb103698d3be1cb4784790f6947b14d39851bf550`  
		Last Modified: Fri, 28 Oct 2022 00:40:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:2223d534de4b168e93ee5731584939fef6069904b42e09ca39e4ef46358dd54f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111744859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05e32726d6a3eb6cd30c7f3cfd15eac77097a00adac44dc185b61d03b58e62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Oct 2022 00:17:42 GMT
RUN cmd /S /C #(nop) COPY file:5cda9aa918fe992fe978c90843552eede9fe664f92442d3068d77fa07c27682b in C:\nats-server.exe 
# Fri, 28 Oct 2022 00:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce29f4214f0fb0200b149c387d5e94ee47d5705e9bc7b884331390782282065f`  
		Last Modified: Thu, 27 Oct 2022 21:23:38 GMT  
		Size: 106.8 MB (106773776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4388e47ca696927a8eab713d6e9905f0069a119b2029c0ddc2d6c8c0f1094157`  
		Last Modified: Fri, 28 Oct 2022 00:18:37 GMT  
		Size: 5.0 MB (4965105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d567bc025c016fe1b38a5f2463f1deb5986fed52de265a356d96e4f782ea04d`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147121d4056552beb6f6f5c897e57e7a81fe46d490dddeb6c410461807b6bf78`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20911c0814537b45d8c70b48e190f3b0a68c11a97b5b3d2745ce9e4d96f4b42`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b8f3033a8d06c06f6986ee485dc4c2f6ee159f98545da2612b238b6c716fcc`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:806d56dd55acbc6497c5cc9ff5916b36ba091212c7308b3a23a1098876e686f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:05a4c0bc8897ddeeb9ddb1473028d9e1c9a0a2cb389516b11578c02f9ec8720f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4911098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c9c625dbef5ec34ca7dceca2ce480b3eb978932e2254e6cfe95c15eb9bb28b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:b9e75e481ae9d301a798308347b654037f5ea8bd8ce2eb3b62d56f1d0fb9aa31 in /nats-server 
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:19:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:19:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:19:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de750ae4d2f684dc52058ab61a992122d85ea9cd1a2c7d449a42ea52d637ca18`  
		Last Modified: Fri, 28 Oct 2022 00:20:46 GMT  
		Size: 4.9 MB (4910589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b72f1a5adda7df074f0eb3d095e5b1300624cd78ef32ff0c78927402b93d0e`  
		Last Modified: Fri, 28 Oct 2022 00:20:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:6a348db5fdde022e586e4fe00252f5207f73386b543dad2b9c791c926472bf98
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4678079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d212b3f530fd382de8872a80b70481fc4db336913a9a59a503f67eac93938faa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:0fb4e969033ab88575e23537c015c04681107529d9128dd4fb94d4f441cf13ea in /nats-server 
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:34:37 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:34:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:34:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ce7e3dd39763e6d0dc795d5534c1a6b6e722fda5cf6cbea372a78489a04f27e`  
		Last Modified: Fri, 28 Oct 2022 00:36:14 GMT  
		Size: 4.7 MB (4677570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c4367ae4414051a0ffbe623600d5fedcab0f7b5110c0a0d95e8bf78c93cfad`  
		Last Modified: Fri, 28 Oct 2022 00:36:13 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:8cf5bcc23025af97af872f1e5fc8e37f60ef5ce1b99163e840515dbc515c735c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4669750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef35e6a4f18c95e20350eca6fd4dd61d948dce45a42d73088f65d880c4dde5f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 01:12:28 GMT
COPY file:c324c9ced487df787b815eb06f1de7520b3f2f3c23cb313b6b6e692d30dce518 in /nats-server 
# Fri, 28 Oct 2022 01:12:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 01:12:29 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:493666cecebad3f9973ea93e7811c9fb15f833a53618a7c6abc12abc16a828b6`  
		Last Modified: Fri, 28 Oct 2022 01:14:05 GMT  
		Size: 4.7 MB (4669243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b13ae6ba1b3faf170714cacd52b2535f8aaf0f18ea5f16479b9a3a9e2e89159`  
		Last Modified: Fri, 28 Oct 2022 01:14:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:eebe621bb4c2136c03d0ede2969549480d42c0faa54935450acdaa9b90dcd474
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6feb88b2953948859fb8aeb942da3d4917625a55916e864e7d1995f816a108`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:4a2b1fa0bbd909bf79b017ae360815907a983b7b2c3b158abf0ed8a95668fb78 in /nats-server 
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:40:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:40:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca262f3c33011e42391f6b52c9727d27cd46c6b5a6a5ed69851d60e703606850`  
		Last Modified: Fri, 28 Oct 2022 00:40:59 GMT  
		Size: 4.5 MB (4498479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e4d79c576957d7c047001eb103698d3be1cb4784790f6947b14d39851bf550`  
		Last Modified: Fri, 28 Oct 2022 00:40:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:fafc6597b93f9cbe091b8309cf8ae5f413fcdac1263da3b9c407becbb4edf56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:nanoserver` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:2223d534de4b168e93ee5731584939fef6069904b42e09ca39e4ef46358dd54f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111744859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05e32726d6a3eb6cd30c7f3cfd15eac77097a00adac44dc185b61d03b58e62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Oct 2022 00:17:42 GMT
RUN cmd /S /C #(nop) COPY file:5cda9aa918fe992fe978c90843552eede9fe664f92442d3068d77fa07c27682b in C:\nats-server.exe 
# Fri, 28 Oct 2022 00:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce29f4214f0fb0200b149c387d5e94ee47d5705e9bc7b884331390782282065f`  
		Last Modified: Thu, 27 Oct 2022 21:23:38 GMT  
		Size: 106.8 MB (106773776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4388e47ca696927a8eab713d6e9905f0069a119b2029c0ddc2d6c8c0f1094157`  
		Last Modified: Fri, 28 Oct 2022 00:18:37 GMT  
		Size: 5.0 MB (4965105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d567bc025c016fe1b38a5f2463f1deb5986fed52de265a356d96e4f782ea04d`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147121d4056552beb6f6f5c897e57e7a81fe46d490dddeb6c410461807b6bf78`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20911c0814537b45d8c70b48e190f3b0a68c11a97b5b3d2745ce9e4d96f4b42`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b8f3033a8d06c06f6986ee485dc4c2f6ee159f98545da2612b238b6c716fcc`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:fafc6597b93f9cbe091b8309cf8ae5f413fcdac1263da3b9c407becbb4edf56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:2223d534de4b168e93ee5731584939fef6069904b42e09ca39e4ef46358dd54f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111744859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05e32726d6a3eb6cd30c7f3cfd15eac77097a00adac44dc185b61d03b58e62c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Tue, 11 Oct 2022 17:25:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 28 Oct 2022 00:17:42 GMT
RUN cmd /S /C #(nop) COPY file:5cda9aa918fe992fe978c90843552eede9fe664f92442d3068d77fa07c27682b in C:\nats-server.exe 
# Fri, 28 Oct 2022 00:17:43 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:44 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:45 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:46 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce29f4214f0fb0200b149c387d5e94ee47d5705e9bc7b884331390782282065f`  
		Last Modified: Thu, 27 Oct 2022 21:23:38 GMT  
		Size: 106.8 MB (106773776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9663157a1b8c7ebfc835c70cef562479a45950b091ce936a265a510fe6c647d`  
		Last Modified: Tue, 11 Oct 2022 17:26:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4388e47ca696927a8eab713d6e9905f0069a119b2029c0ddc2d6c8c0f1094157`  
		Last Modified: Fri, 28 Oct 2022 00:18:37 GMT  
		Size: 5.0 MB (4965105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d567bc025c016fe1b38a5f2463f1deb5986fed52de265a356d96e4f782ea04d`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147121d4056552beb6f6f5c897e57e7a81fe46d490dddeb6c410461807b6bf78`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20911c0814537b45d8c70b48e190f3b0a68c11a97b5b3d2745ce9e4d96f4b42`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b8f3033a8d06c06f6986ee485dc4c2f6ee159f98545da2612b238b6c716fcc`  
		Last Modified: Fri, 28 Oct 2022 00:18:36 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:806d56dd55acbc6497c5cc9ff5916b36ba091212c7308b3a23a1098876e686f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:05a4c0bc8897ddeeb9ddb1473028d9e1c9a0a2cb389516b11578c02f9ec8720f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4911098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c9c625dbef5ec34ca7dceca2ce480b3eb978932e2254e6cfe95c15eb9bb28b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:b9e75e481ae9d301a798308347b654037f5ea8bd8ce2eb3b62d56f1d0fb9aa31 in /nats-server 
# Fri, 28 Oct 2022 00:19:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:19:58 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:19:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:19:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:19:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:de750ae4d2f684dc52058ab61a992122d85ea9cd1a2c7d449a42ea52d637ca18`  
		Last Modified: Fri, 28 Oct 2022 00:20:46 GMT  
		Size: 4.9 MB (4910589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b72f1a5adda7df074f0eb3d095e5b1300624cd78ef32ff0c78927402b93d0e`  
		Last Modified: Fri, 28 Oct 2022 00:20:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:6a348db5fdde022e586e4fe00252f5207f73386b543dad2b9c791c926472bf98
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4678079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d212b3f530fd382de8872a80b70481fc4db336913a9a59a503f67eac93938faa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:0fb4e969033ab88575e23537c015c04681107529d9128dd4fb94d4f441cf13ea in /nats-server 
# Fri, 28 Oct 2022 00:34:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:34:37 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:34:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:34:37 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:34:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5ce7e3dd39763e6d0dc795d5534c1a6b6e722fda5cf6cbea372a78489a04f27e`  
		Last Modified: Fri, 28 Oct 2022 00:36:14 GMT  
		Size: 4.7 MB (4677570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c4367ae4414051a0ffbe623600d5fedcab0f7b5110c0a0d95e8bf78c93cfad`  
		Last Modified: Fri, 28 Oct 2022 00:36:13 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:8cf5bcc23025af97af872f1e5fc8e37f60ef5ce1b99163e840515dbc515c735c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4669750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef35e6a4f18c95e20350eca6fd4dd61d948dce45a42d73088f65d880c4dde5f5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 01:12:28 GMT
COPY file:c324c9ced487df787b815eb06f1de7520b3f2f3c23cb313b6b6e692d30dce518 in /nats-server 
# Fri, 28 Oct 2022 01:12:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 01:12:29 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:493666cecebad3f9973ea93e7811c9fb15f833a53618a7c6abc12abc16a828b6`  
		Last Modified: Fri, 28 Oct 2022 01:14:05 GMT  
		Size: 4.7 MB (4669243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b13ae6ba1b3faf170714cacd52b2535f8aaf0f18ea5f16479b9a3a9e2e89159`  
		Last Modified: Fri, 28 Oct 2022 01:14:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:eebe621bb4c2136c03d0ede2969549480d42c0faa54935450acdaa9b90dcd474
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6feb88b2953948859fb8aeb942da3d4917625a55916e864e7d1995f816a108`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:4a2b1fa0bbd909bf79b017ae360815907a983b7b2c3b158abf0ed8a95668fb78 in /nats-server 
# Fri, 28 Oct 2022 00:40:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Oct 2022 00:40:10 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:40:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Oct 2022 00:40:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Oct 2022 00:40:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca262f3c33011e42391f6b52c9727d27cd46c6b5a6a5ed69851d60e703606850`  
		Last Modified: Fri, 28 Oct 2022 00:40:59 GMT  
		Size: 4.5 MB (4498479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e4d79c576957d7c047001eb103698d3be1cb4784790f6947b14d39851bf550`  
		Last Modified: Fri, 28 Oct 2022 00:40:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:fdb8994491270872284ca4358bc66e164b2f6fa02e5189163b51cb8df71bc276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:43e84da881b4607236ff0f9158fe2215c782c94b01effb76af5fb9831a594fcb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2779174179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab33aded854a32b758ffbe80d2425e85d79fe5e68257d305b54bf4661ce0ab5f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Fri, 28 Oct 2022 00:14:59 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:14:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.4/nats-server-v2.9.4-windows-amd64.zip
# Fri, 28 Oct 2022 00:15:01 GMT
ENV NATS_SERVER_SHASUM=ba5d135b14bb4f4c106639c6f0b3fe5530b4e9ec4dd2c4e3b83f78c0e808e435
# Fri, 28 Oct 2022 00:15:53 GMT
RUN Set-PSDebug -Trace 2
# Fri, 28 Oct 2022 00:17:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 28 Oct 2022 00:17:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:24 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6193ab94a0498ba6454e2a35e189837b37a2eb01403e8b62654bdc28a4569c`  
		Last Modified: Mon, 17 Oct 2022 21:52:22 GMT  
		Size: 849.2 MB (849228999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777120ea710a4a6c96e29b0896d6ba5301aeabc76ebc7746bdaf630026ceb3dd`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178f4f6f90f6bab4aaf8342187d088536e8a65bce5b71a78c8775ab21d57dc39`  
		Last Modified: Fri, 28 Oct 2022 00:18:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64be820df0d316e845aeaa24d9714941dc6038fb96c3af1ae68ce7de1304a0b`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7711c2ad12dd348b7559e313bb366a27c48900fb880fc0e18562ab742ce5e6`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 357.8 KB (357788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d41267dcad8d27b3da89455553106bf0cafab939c7e8ba37b7aa2a3c7bfb46d`  
		Last Modified: Fri, 28 Oct 2022 00:18:18 GMT  
		Size: 5.3 MB (5305490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7434c9c183776b09625ce99d06e361a904e516542812ffb699420f5a5a150394`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a4aaaadc6896c5cdcd54e586dc2512c4925eff8b4545ab14d6b23f33aaf1ec`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56300ead49ee511a9bd2dd1eb8849af5673a6f85d81158b22a3ab7349dbd4be4`  
		Last Modified: Fri, 28 Oct 2022 00:18:17 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1e5f72226f5d2f9b0094bf2b7fa505f3ebcea3bea5157a66f1fdce6147bb07`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:fdb8994491270872284ca4358bc66e164b2f6fa02e5189163b51cb8df71bc276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull nats@sha256:43e84da881b4607236ff0f9158fe2215c782c94b01effb76af5fb9831a594fcb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2779174179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab33aded854a32b758ffbe80d2425e85d79fe5e68257d305b54bf4661ce0ab5f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Fri, 28 Oct 2022 00:14:59 GMT
ENV NATS_SERVER=2.9.4
# Fri, 28 Oct 2022 00:14:59 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.4/nats-server-v2.9.4-windows-amd64.zip
# Fri, 28 Oct 2022 00:15:01 GMT
ENV NATS_SERVER_SHASUM=ba5d135b14bb4f4c106639c6f0b3fe5530b4e9ec4dd2c4e3b83f78c0e808e435
# Fri, 28 Oct 2022 00:15:53 GMT
RUN Set-PSDebug -Trace 2
# Fri, 28 Oct 2022 00:17:21 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 28 Oct 2022 00:17:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 28 Oct 2022 00:17:24 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Oct 2022 00:17:25 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 28 Oct 2022 00:17:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6193ab94a0498ba6454e2a35e189837b37a2eb01403e8b62654bdc28a4569c`  
		Last Modified: Mon, 17 Oct 2022 21:52:22 GMT  
		Size: 849.2 MB (849228999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c778a0131ae2f1653f1fb703f05998e74365629f70b1a15a0360fb1292182846`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ce79ce85e7eb7d4b12316d81cc8cb3ff2567ee214f4aa0bbf36933fd55891f`  
		Last Modified: Tue, 11 Oct 2022 17:26:37 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777120ea710a4a6c96e29b0896d6ba5301aeabc76ebc7746bdaf630026ceb3dd`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178f4f6f90f6bab4aaf8342187d088536e8a65bce5b71a78c8775ab21d57dc39`  
		Last Modified: Fri, 28 Oct 2022 00:18:18 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64be820df0d316e845aeaa24d9714941dc6038fb96c3af1ae68ce7de1304a0b`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7711c2ad12dd348b7559e313bb366a27c48900fb880fc0e18562ab742ce5e6`  
		Last Modified: Fri, 28 Oct 2022 00:18:19 GMT  
		Size: 357.8 KB (357788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d41267dcad8d27b3da89455553106bf0cafab939c7e8ba37b7aa2a3c7bfb46d`  
		Last Modified: Fri, 28 Oct 2022 00:18:18 GMT  
		Size: 5.3 MB (5305490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7434c9c183776b09625ce99d06e361a904e516542812ffb699420f5a5a150394`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a4aaaadc6896c5cdcd54e586dc2512c4925eff8b4545ab14d6b23f33aaf1ec`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56300ead49ee511a9bd2dd1eb8849af5673a6f85d81158b22a3ab7349dbd4be4`  
		Last Modified: Fri, 28 Oct 2022 00:18:17 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1e5f72226f5d2f9b0094bf2b7fa505f3ebcea3bea5157a66f1fdce6147bb07`  
		Last Modified: Fri, 28 Oct 2022 00:18:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
