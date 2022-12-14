<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.17`](#nats2-alpine317)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.9`](#nats29)
-	[`nats:2.9-alpine`](#nats29-alpine)
-	[`nats:2.9-alpine3.17`](#nats29-alpine317)
-	[`nats:2.9-linux`](#nats29-linux)
-	[`nats:2.9-nanoserver`](#nats29-nanoserver)
-	[`nats:2.9-nanoserver-1809`](#nats29-nanoserver-1809)
-	[`nats:2.9-scratch`](#nats29-scratch)
-	[`nats:2.9-windowsservercore`](#nats29-windowsservercore)
-	[`nats:2.9-windowsservercore-1809`](#nats29-windowsservercore-1809)
-	[`nats:2.9.9`](#nats299)
-	[`nats:2.9.9-alpine`](#nats299-alpine)
-	[`nats:2.9.9-alpine3.17`](#nats299-alpine317)
-	[`nats:2.9.9-linux`](#nats299-linux)
-	[`nats:2.9.9-nanoserver`](#nats299-nanoserver)
-	[`nats:2.9.9-nanoserver-1809`](#nats299-nanoserver-1809)
-	[`nats:2.9.9-scratch`](#nats299-scratch)
-	[`nats:2.9.9-windowsservercore`](#nats299-windowsservercore)
-	[`nats:2.9.9-windowsservercore-1809`](#nats299-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.17`](#natsalpine317)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:e4c75014ae278dcb8192c9718c7c0cebfb55cb76c41b285a1663141794ab96f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3770; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:79830eec98d1dc2f6acd4c63fee41a3434bc47a1b7f31cab9477de1bb3336100
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4922852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce49f767b1c3e8d858ddf7390fb3dad1b4fdebd12784b1fe33719a5a1a7993`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:d13bbefb978757216c59b4e4aba99770a0d4abdac594ab77282fb8cd6b85b588 in /nats-server 
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:35:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:35:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:35:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7692aeb9660d6587db50a4ea4f287699e633f61600a28a2d22092a82846129ce`  
		Last Modified: Thu, 08 Dec 2022 20:36:28 GMT  
		Size: 4.9 MB (4922345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022161875246986f560f72a1c52a359c684e6760487fe8f04a353168edfd2ac7`  
		Last Modified: Thu, 08 Dec 2022 20:36:27 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:24970d929b8d8ecf8887fb00bd92ce687fa3b252218c033614bbc892eec3c380
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4684937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac2c7d543ae2d436c8f9381f98b0bf06c08e5995d33fe8bdebd74699cfc1635`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:00:11 GMT
COPY file:5143a8dee5d00da934937a160852ff57e854ce11c42fdd4828e47d5bb4df42da in /nats-server 
# Thu, 08 Dec 2022 20:00:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:00:12 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:00:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:00:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fedc572ae49bd720399deeb6a36a9250630afd1a477e3c36b0afa73c9106ee50`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 4.7 MB (4684431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8cd5d76c140f074a437a1a67876d7ccd749d332dc6908ccb8fe301cd5dde0a`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:e0e6a65a6d9b16c6fc02bc5eb03804447975e81aab5cb4ef6de5ae0e7b490c54
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2439be95ff20e36b9fc19dd178f16c99ae8deb74465c167849bbff1ae4e66612`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:4c080655f46dbff5713191574af1df195a38d3dc3d3835f7eb875699a8e32d0b in /nats-server 
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:31:19 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:31:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:31:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221d437a3d6581cb4a83aada6c1cd3cb9d173cc07d5d0e9be2c801fb03fa9abe`  
		Last Modified: Thu, 08 Dec 2022 20:32:52 GMT  
		Size: 4.7 MB (4680919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5146fbe1772138448df3c1eb3444c5077d2cdac62bc7b082c112ac5ee4be14b2`  
		Last Modified: Thu, 08 Dec 2022 20:32:51 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:95318d8cd0e5ac24a3070af64056187f97cfb83673bb66a0fd5402f484912bc2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60599b58e21ba05f3bb06c0c373f7f8e213ea6861ad81399a4472fff4a90dbad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:5e130ace514500d49e7ad10785f48a1123d8992953cabcf51a55abf452f854f0 in /nats-server 
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 19:57:18 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:57:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 19:57:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 19:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8935bb735107ae5954afbbd1ce8b5d61ad9a102c82ba176ee5fcc00d437cc63`  
		Last Modified: Thu, 08 Dec 2022 19:58:05 GMT  
		Size: 4.5 MB (4506356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e3d737971cded626be61eca795945c4a04518d6c2dc737dbd7342cac026be`  
		Last Modified: Thu, 08 Dec 2022 19:58:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:e27c1884d9603539962cb28b7a22ad496237beba12bf95e9ed49fe9afa6c86d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111653587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0454f4ce065ac9703834be6c37eabe50eb3607ecae1d7cc7b344972885eb0b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Wed, 14 Dec 2022 02:41:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:41:39 GMT
RUN cmd /S /C #(nop) COPY file:8d03b51c4d2105411f3161f01ef7aad45804539a633733d4a8a5eb9f07e4970a in C:\nats-server.exe 
# Wed, 14 Dec 2022 02:41:40 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e9d361872b14736e9b1544993bd1f54f9284833fe47bff0ed4a51b726c47d8`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75304ecf4347969762a53760eff5f595b7ded2f4bd3ddf5b100cbfe792f5eda7`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 5.0 MB (4976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bacc71a9645bdd06d67819b123d5846ca66131f4d6d357ce3be7a9ba3679ffe`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6d4bc865209ef6542a200df7b975e08fcd6ebb627c4667fb6316854f0a6051`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340559bbbd7873ac427f77173287f004fa4a4fba5395aecaa30ed6923f7823e4`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076d6856ac201aebd4e95cd5f0b55a36849f89f8f43b44db4e80dd4d0b6c1f1`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:c0ffa1bed32d05eebcbc9892ecfa0c37ea9f1139ef480d1bc6c8c031a8d2a78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:4455732015639b8c2fa8e9020f3d17e8a209f9d59543292710768af952148382
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8581793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3b6d7d2a01e46a077c00066353ec8f59dd1f7812c8dd98a987f5250bbd6b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:34:51 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:34:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:34:54 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:34:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:34:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed86478665b1337795c7e912325131cdc2d168214502eed69e3723ff4a234d25`  
		Last Modified: Thu, 08 Dec 2022 20:36:07 GMT  
		Size: 5.2 MB (5210085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69220328c19fd2b50424c54dca1d8a7b058aa5a162eb5ac14521e35c4d62f1a`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79d3be31b99b819fb19f51849bff6e77c2b09db3e5da0d0ef4e094ed967ff8f`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3119056346819803bc76df59c2e831ff5171a8da1f002a4607e7e2abfbe6ecee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8082503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc75fd6f64f71d7f3e687447b6480cd6f9d57bd8a4ba7c2983d8861d4e3b51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:55:46 GMT
ADD file:132c76d7f7dae2f51f589ee460f1870a2cec6e9dc7ff8e38e88fcee2cfbe70da in / 
# Tue, 22 Nov 2022 22:55:46 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:59:56 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:59:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:59:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:00:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:00:00 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:00:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c2eb4db52fbe1266a78d8c185d33544a2916faa7d82fb5f50909fe233e0579da`  
		Last Modified: Tue, 22 Nov 2022 22:56:39 GMT  
		Size: 3.1 MB (3107138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f27e96bda80af22fdcbc14d587a8bd7f1785a53f6186c176c60cb5ee041552`  
		Last Modified: Thu, 08 Dec 2022 20:01:16 GMT  
		Size: 5.0 MB (4974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3bcb78d13a5f28e8655978e2d55ca50e33f3c13cd5c589ed9ff1af70a7316f`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495e1ec935b2a91f7057d7585b3674b8243a942618d53d46882d39f719432979`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:5831f8c5ef78543c5468a18f140d4437b908d992d4d902ede67b681ae1b9d368
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7831737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a580d362e6b152069cf3b30f5e629c7e3b964a990c4a7d15e5e5c33bf6f9610a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:57:20 GMT
ADD file:080010d9005e8e0dae3e98c7f9afff3e3a40ed32579ca01946efc6ede8316bad in / 
# Tue, 22 Nov 2022 22:57:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:30:58 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:31:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:31:02 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:31:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb2ec849933dd31db64abae3fdcb6923c490d9795577bee1ee1be04eab0376ee`  
		Last Modified: Tue, 22 Nov 2022 22:58:12 GMT  
		Size: 2.9 MB (2865346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671c89e40ba9d510918522256afe00ea4e39a695355982e9f361339ed50f7d08`  
		Last Modified: Thu, 08 Dec 2022 20:32:23 GMT  
		Size: 5.0 MB (4965424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de0969a38fcc2a8858b856efe0a63cd2745e3618c370383bea1f20db57e5e0c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6d0563d82f6dafe5dc45f3a674812a38a28ae6df2f7ac30a4d7664811a572c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d6a6c27b86493e468a184154633dfddf07e4fe466ad39c6b7eeaa4609e2ed0d2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8056469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3378f00ddf68731dab0ff2d503395918d1b20713f78c76e5e28bdf22fc29d78f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:56:52 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:56:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 19:56:55 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:56:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 19:56:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986444278dadde0d9a262ed4b893f80ad454eb35ffc857e42b5ad2f073465016`  
		Last Modified: Thu, 08 Dec 2022 19:57:44 GMT  
		Size: 4.8 MB (4796278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f5d8e79ec79a470e91e51e5aa1553566f49b677c12044d8e9b5c796e0ee27e`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4e306fd7736484456b60e0960d6d29025a49f82670bf70fad13a464afa6aec`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.17`

```console
$ docker pull nats@sha256:c0ffa1bed32d05eebcbc9892ecfa0c37ea9f1139ef480d1bc6c8c031a8d2a78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.17` - linux; amd64

```console
$ docker pull nats@sha256:4455732015639b8c2fa8e9020f3d17e8a209f9d59543292710768af952148382
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8581793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3b6d7d2a01e46a077c00066353ec8f59dd1f7812c8dd98a987f5250bbd6b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:34:51 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:34:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:34:54 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:34:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:34:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed86478665b1337795c7e912325131cdc2d168214502eed69e3723ff4a234d25`  
		Last Modified: Thu, 08 Dec 2022 20:36:07 GMT  
		Size: 5.2 MB (5210085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69220328c19fd2b50424c54dca1d8a7b058aa5a162eb5ac14521e35c4d62f1a`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79d3be31b99b819fb19f51849bff6e77c2b09db3e5da0d0ef4e094ed967ff8f`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.17` - linux; arm variant v6

```console
$ docker pull nats@sha256:3119056346819803bc76df59c2e831ff5171a8da1f002a4607e7e2abfbe6ecee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8082503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc75fd6f64f71d7f3e687447b6480cd6f9d57bd8a4ba7c2983d8861d4e3b51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:55:46 GMT
ADD file:132c76d7f7dae2f51f589ee460f1870a2cec6e9dc7ff8e38e88fcee2cfbe70da in / 
# Tue, 22 Nov 2022 22:55:46 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:59:56 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:59:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:59:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:00:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:00:00 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:00:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c2eb4db52fbe1266a78d8c185d33544a2916faa7d82fb5f50909fe233e0579da`  
		Last Modified: Tue, 22 Nov 2022 22:56:39 GMT  
		Size: 3.1 MB (3107138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f27e96bda80af22fdcbc14d587a8bd7f1785a53f6186c176c60cb5ee041552`  
		Last Modified: Thu, 08 Dec 2022 20:01:16 GMT  
		Size: 5.0 MB (4974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3bcb78d13a5f28e8655978e2d55ca50e33f3c13cd5c589ed9ff1af70a7316f`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495e1ec935b2a91f7057d7585b3674b8243a942618d53d46882d39f719432979`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.17` - linux; arm variant v7

```console
$ docker pull nats@sha256:5831f8c5ef78543c5468a18f140d4437b908d992d4d902ede67b681ae1b9d368
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7831737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a580d362e6b152069cf3b30f5e629c7e3b964a990c4a7d15e5e5c33bf6f9610a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:57:20 GMT
ADD file:080010d9005e8e0dae3e98c7f9afff3e3a40ed32579ca01946efc6ede8316bad in / 
# Tue, 22 Nov 2022 22:57:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:30:58 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:31:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:31:02 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:31:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb2ec849933dd31db64abae3fdcb6923c490d9795577bee1ee1be04eab0376ee`  
		Last Modified: Tue, 22 Nov 2022 22:58:12 GMT  
		Size: 2.9 MB (2865346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671c89e40ba9d510918522256afe00ea4e39a695355982e9f361339ed50f7d08`  
		Last Modified: Thu, 08 Dec 2022 20:32:23 GMT  
		Size: 5.0 MB (4965424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de0969a38fcc2a8858b856efe0a63cd2745e3618c370383bea1f20db57e5e0c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6d0563d82f6dafe5dc45f3a674812a38a28ae6df2f7ac30a4d7664811a572c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d6a6c27b86493e468a184154633dfddf07e4fe466ad39c6b7eeaa4609e2ed0d2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8056469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3378f00ddf68731dab0ff2d503395918d1b20713f78c76e5e28bdf22fc29d78f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:56:52 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:56:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 19:56:55 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:56:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 19:56:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986444278dadde0d9a262ed4b893f80ad454eb35ffc857e42b5ad2f073465016`  
		Last Modified: Thu, 08 Dec 2022 19:57:44 GMT  
		Size: 4.8 MB (4796278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f5d8e79ec79a470e91e51e5aa1553566f49b677c12044d8e9b5c796e0ee27e`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4e306fd7736484456b60e0960d6d29025a49f82670bf70fad13a464afa6aec`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:da6a053c9c9f52e84383f68483bc74cb3c7caafdd89ea93fe71d475193d0c530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:79830eec98d1dc2f6acd4c63fee41a3434bc47a1b7f31cab9477de1bb3336100
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4922852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce49f767b1c3e8d858ddf7390fb3dad1b4fdebd12784b1fe33719a5a1a7993`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:d13bbefb978757216c59b4e4aba99770a0d4abdac594ab77282fb8cd6b85b588 in /nats-server 
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:35:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:35:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:35:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7692aeb9660d6587db50a4ea4f287699e633f61600a28a2d22092a82846129ce`  
		Last Modified: Thu, 08 Dec 2022 20:36:28 GMT  
		Size: 4.9 MB (4922345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022161875246986f560f72a1c52a359c684e6760487fe8f04a353168edfd2ac7`  
		Last Modified: Thu, 08 Dec 2022 20:36:27 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:24970d929b8d8ecf8887fb00bd92ce687fa3b252218c033614bbc892eec3c380
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4684937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac2c7d543ae2d436c8f9381f98b0bf06c08e5995d33fe8bdebd74699cfc1635`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:00:11 GMT
COPY file:5143a8dee5d00da934937a160852ff57e854ce11c42fdd4828e47d5bb4df42da in /nats-server 
# Thu, 08 Dec 2022 20:00:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:00:12 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:00:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:00:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fedc572ae49bd720399deeb6a36a9250630afd1a477e3c36b0afa73c9106ee50`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 4.7 MB (4684431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8cd5d76c140f074a437a1a67876d7ccd749d332dc6908ccb8fe301cd5dde0a`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:e0e6a65a6d9b16c6fc02bc5eb03804447975e81aab5cb4ef6de5ae0e7b490c54
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2439be95ff20e36b9fc19dd178f16c99ae8deb74465c167849bbff1ae4e66612`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:4c080655f46dbff5713191574af1df195a38d3dc3d3835f7eb875699a8e32d0b in /nats-server 
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:31:19 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:31:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:31:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221d437a3d6581cb4a83aada6c1cd3cb9d173cc07d5d0e9be2c801fb03fa9abe`  
		Last Modified: Thu, 08 Dec 2022 20:32:52 GMT  
		Size: 4.7 MB (4680919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5146fbe1772138448df3c1eb3444c5077d2cdac62bc7b082c112ac5ee4be14b2`  
		Last Modified: Thu, 08 Dec 2022 20:32:51 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:95318d8cd0e5ac24a3070af64056187f97cfb83673bb66a0fd5402f484912bc2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60599b58e21ba05f3bb06c0c373f7f8e213ea6861ad81399a4472fff4a90dbad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:5e130ace514500d49e7ad10785f48a1123d8992953cabcf51a55abf452f854f0 in /nats-server 
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 19:57:18 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:57:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 19:57:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 19:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8935bb735107ae5954afbbd1ce8b5d61ad9a102c82ba176ee5fcc00d437cc63`  
		Last Modified: Thu, 08 Dec 2022 19:58:05 GMT  
		Size: 4.5 MB (4506356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e3d737971cded626be61eca795945c4a04518d6c2dc737dbd7342cac026be`  
		Last Modified: Thu, 08 Dec 2022 19:58:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:794c09f7a1b633fc92984035474e997ea88e32a22b4db214410f58a95e348a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:e27c1884d9603539962cb28b7a22ad496237beba12bf95e9ed49fe9afa6c86d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111653587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0454f4ce065ac9703834be6c37eabe50eb3607ecae1d7cc7b344972885eb0b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Wed, 14 Dec 2022 02:41:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:41:39 GMT
RUN cmd /S /C #(nop) COPY file:8d03b51c4d2105411f3161f01ef7aad45804539a633733d4a8a5eb9f07e4970a in C:\nats-server.exe 
# Wed, 14 Dec 2022 02:41:40 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e9d361872b14736e9b1544993bd1f54f9284833fe47bff0ed4a51b726c47d8`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75304ecf4347969762a53760eff5f595b7ded2f4bd3ddf5b100cbfe792f5eda7`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 5.0 MB (4976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bacc71a9645bdd06d67819b123d5846ca66131f4d6d357ce3be7a9ba3679ffe`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6d4bc865209ef6542a200df7b975e08fcd6ebb627c4667fb6316854f0a6051`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340559bbbd7873ac427f77173287f004fa4a4fba5395aecaa30ed6923f7823e4`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076d6856ac201aebd4e95cd5f0b55a36849f89f8f43b44db4e80dd4d0b6c1f1`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:794c09f7a1b633fc92984035474e997ea88e32a22b4db214410f58a95e348a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:e27c1884d9603539962cb28b7a22ad496237beba12bf95e9ed49fe9afa6c86d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111653587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0454f4ce065ac9703834be6c37eabe50eb3607ecae1d7cc7b344972885eb0b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Wed, 14 Dec 2022 02:41:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:41:39 GMT
RUN cmd /S /C #(nop) COPY file:8d03b51c4d2105411f3161f01ef7aad45804539a633733d4a8a5eb9f07e4970a in C:\nats-server.exe 
# Wed, 14 Dec 2022 02:41:40 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e9d361872b14736e9b1544993bd1f54f9284833fe47bff0ed4a51b726c47d8`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75304ecf4347969762a53760eff5f595b7ded2f4bd3ddf5b100cbfe792f5eda7`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 5.0 MB (4976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bacc71a9645bdd06d67819b123d5846ca66131f4d6d357ce3be7a9ba3679ffe`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6d4bc865209ef6542a200df7b975e08fcd6ebb627c4667fb6316854f0a6051`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340559bbbd7873ac427f77173287f004fa4a4fba5395aecaa30ed6923f7823e4`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076d6856ac201aebd4e95cd5f0b55a36849f89f8f43b44db4e80dd4d0b6c1f1`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:da6a053c9c9f52e84383f68483bc74cb3c7caafdd89ea93fe71d475193d0c530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:79830eec98d1dc2f6acd4c63fee41a3434bc47a1b7f31cab9477de1bb3336100
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4922852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce49f767b1c3e8d858ddf7390fb3dad1b4fdebd12784b1fe33719a5a1a7993`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:d13bbefb978757216c59b4e4aba99770a0d4abdac594ab77282fb8cd6b85b588 in /nats-server 
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:35:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:35:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:35:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7692aeb9660d6587db50a4ea4f287699e633f61600a28a2d22092a82846129ce`  
		Last Modified: Thu, 08 Dec 2022 20:36:28 GMT  
		Size: 4.9 MB (4922345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022161875246986f560f72a1c52a359c684e6760487fe8f04a353168edfd2ac7`  
		Last Modified: Thu, 08 Dec 2022 20:36:27 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:24970d929b8d8ecf8887fb00bd92ce687fa3b252218c033614bbc892eec3c380
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4684937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac2c7d543ae2d436c8f9381f98b0bf06c08e5995d33fe8bdebd74699cfc1635`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:00:11 GMT
COPY file:5143a8dee5d00da934937a160852ff57e854ce11c42fdd4828e47d5bb4df42da in /nats-server 
# Thu, 08 Dec 2022 20:00:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:00:12 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:00:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:00:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fedc572ae49bd720399deeb6a36a9250630afd1a477e3c36b0afa73c9106ee50`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 4.7 MB (4684431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8cd5d76c140f074a437a1a67876d7ccd749d332dc6908ccb8fe301cd5dde0a`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:e0e6a65a6d9b16c6fc02bc5eb03804447975e81aab5cb4ef6de5ae0e7b490c54
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2439be95ff20e36b9fc19dd178f16c99ae8deb74465c167849bbff1ae4e66612`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:4c080655f46dbff5713191574af1df195a38d3dc3d3835f7eb875699a8e32d0b in /nats-server 
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:31:19 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:31:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:31:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221d437a3d6581cb4a83aada6c1cd3cb9d173cc07d5d0e9be2c801fb03fa9abe`  
		Last Modified: Thu, 08 Dec 2022 20:32:52 GMT  
		Size: 4.7 MB (4680919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5146fbe1772138448df3c1eb3444c5077d2cdac62bc7b082c112ac5ee4be14b2`  
		Last Modified: Thu, 08 Dec 2022 20:32:51 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:95318d8cd0e5ac24a3070af64056187f97cfb83673bb66a0fd5402f484912bc2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60599b58e21ba05f3bb06c0c373f7f8e213ea6861ad81399a4472fff4a90dbad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:5e130ace514500d49e7ad10785f48a1123d8992953cabcf51a55abf452f854f0 in /nats-server 
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 19:57:18 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:57:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 19:57:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 19:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8935bb735107ae5954afbbd1ce8b5d61ad9a102c82ba176ee5fcc00d437cc63`  
		Last Modified: Thu, 08 Dec 2022 19:58:05 GMT  
		Size: 4.5 MB (4506356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e3d737971cded626be61eca795945c4a04518d6c2dc737dbd7342cac026be`  
		Last Modified: Thu, 08 Dec 2022 19:58:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:bd5262b0964a38e7e28de29632b03d507ba57fc832bb3171567478da841d9f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:11e1ab562299ebbb64ab18c5afd891fa67655420780a109677a922340d8777d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2786352699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6dc041a550a2790319a7bb1f8b2b6bc818495c7300afc3226fc2da4d42219a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sun, 11 Dec 2022 08:04:49 GMT
RUN Install update 10.0.17763.3770
# Wed, 14 Dec 2022 01:29:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Dec 2022 02:37:16 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:37:17 GMT
ENV NATS_SERVER=2.9.9
# Wed, 14 Dec 2022 02:37:18 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.9/nats-server-v2.9.9-windows-amd64.zip
# Wed, 14 Dec 2022 02:37:19 GMT
ENV NATS_SERVER_SHASUM=a3456ed1a8f02d9d8ced35a1adbe1f6451af0c303f87ff74c15879dfc8cabd30
# Wed, 14 Dec 2022 02:38:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Dec 2022 02:41:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Dec 2022 02:41:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:20 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ad73ed772f80ab7923579a55dd12fb9b6e090d1d836408d16ffd9d3dee252`  
		Last Modified: Tue, 13 Dec 2022 23:56:47 GMT  
		Size: 856.4 MB (856427878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1d7d21a6f8359d8228f44b50aa9ad552783452100b6ce203e8f042415b5623`  
		Last Modified: Wed, 14 Dec 2022 02:14:22 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2b4fa0f968fba4be86c61da602c6d1d95bea2a5b257fa97e5cb498f7ddc7fe`  
		Last Modified: Wed, 14 Dec 2022 02:42:16 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1296500fbd02b72d68a4f8d4c78bb6c35ddaaa2c332cfe9254604281a913a00`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50931b0d887f06faade1d2051e8cceac2255778e1b4b9653fc75474db54b489d`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d625cf2ad988d5ac80b24112ef78da7fe7bddd4b5d188962fcb3ab90f04b57e`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f665d13d7cbc9a4ce6c8e5bc9120d5e3343377d7211f1e4d12480ddda591f522`  
		Last Modified: Wed, 14 Dec 2022 02:42:15 GMT  
		Size: 342.0 KB (342028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75307c50ea67f0603708dfc03956f1d610f261a5fa0f54d064b1690b0f866274`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 5.3 MB (5300085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1799e7de223a25ae30a351e317b449f128c31f00e818c0df0b02a4be360e4cf3`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 2.0 KB (1962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfeddb4c41b8d5fdc840c446ef490340728041b9202f2db80dce668c9d8d8ca5`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb917ab1b2406dc49a3fcc8fe92a27023ef822724a7c3056fa6f14ea3eca9d09`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2920025a2b586dcc5fa9b1580994f3bedbdbc128a7ab0a5c9bba8ca690025e0e`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:bd5262b0964a38e7e28de29632b03d507ba57fc832bb3171567478da841d9f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:11e1ab562299ebbb64ab18c5afd891fa67655420780a109677a922340d8777d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2786352699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6dc041a550a2790319a7bb1f8b2b6bc818495c7300afc3226fc2da4d42219a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sun, 11 Dec 2022 08:04:49 GMT
RUN Install update 10.0.17763.3770
# Wed, 14 Dec 2022 01:29:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Dec 2022 02:37:16 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:37:17 GMT
ENV NATS_SERVER=2.9.9
# Wed, 14 Dec 2022 02:37:18 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.9/nats-server-v2.9.9-windows-amd64.zip
# Wed, 14 Dec 2022 02:37:19 GMT
ENV NATS_SERVER_SHASUM=a3456ed1a8f02d9d8ced35a1adbe1f6451af0c303f87ff74c15879dfc8cabd30
# Wed, 14 Dec 2022 02:38:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Dec 2022 02:41:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Dec 2022 02:41:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:20 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ad73ed772f80ab7923579a55dd12fb9b6e090d1d836408d16ffd9d3dee252`  
		Last Modified: Tue, 13 Dec 2022 23:56:47 GMT  
		Size: 856.4 MB (856427878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1d7d21a6f8359d8228f44b50aa9ad552783452100b6ce203e8f042415b5623`  
		Last Modified: Wed, 14 Dec 2022 02:14:22 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2b4fa0f968fba4be86c61da602c6d1d95bea2a5b257fa97e5cb498f7ddc7fe`  
		Last Modified: Wed, 14 Dec 2022 02:42:16 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1296500fbd02b72d68a4f8d4c78bb6c35ddaaa2c332cfe9254604281a913a00`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50931b0d887f06faade1d2051e8cceac2255778e1b4b9653fc75474db54b489d`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d625cf2ad988d5ac80b24112ef78da7fe7bddd4b5d188962fcb3ab90f04b57e`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f665d13d7cbc9a4ce6c8e5bc9120d5e3343377d7211f1e4d12480ddda591f522`  
		Last Modified: Wed, 14 Dec 2022 02:42:15 GMT  
		Size: 342.0 KB (342028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75307c50ea67f0603708dfc03956f1d610f261a5fa0f54d064b1690b0f866274`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 5.3 MB (5300085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1799e7de223a25ae30a351e317b449f128c31f00e818c0df0b02a4be360e4cf3`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 2.0 KB (1962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfeddb4c41b8d5fdc840c446ef490340728041b9202f2db80dce668c9d8d8ca5`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb917ab1b2406dc49a3fcc8fe92a27023ef822724a7c3056fa6f14ea3eca9d09`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2920025a2b586dcc5fa9b1580994f3bedbdbc128a7ab0a5c9bba8ca690025e0e`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9`

```console
$ docker pull nats@sha256:e4c75014ae278dcb8192c9718c7c0cebfb55cb76c41b285a1663141794ab96f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3770; amd64

### `nats:2.9` - linux; amd64

```console
$ docker pull nats@sha256:79830eec98d1dc2f6acd4c63fee41a3434bc47a1b7f31cab9477de1bb3336100
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4922852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce49f767b1c3e8d858ddf7390fb3dad1b4fdebd12784b1fe33719a5a1a7993`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:d13bbefb978757216c59b4e4aba99770a0d4abdac594ab77282fb8cd6b85b588 in /nats-server 
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:35:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:35:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:35:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7692aeb9660d6587db50a4ea4f287699e633f61600a28a2d22092a82846129ce`  
		Last Modified: Thu, 08 Dec 2022 20:36:28 GMT  
		Size: 4.9 MB (4922345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022161875246986f560f72a1c52a359c684e6760487fe8f04a353168edfd2ac7`  
		Last Modified: Thu, 08 Dec 2022 20:36:27 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:24970d929b8d8ecf8887fb00bd92ce687fa3b252218c033614bbc892eec3c380
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4684937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac2c7d543ae2d436c8f9381f98b0bf06c08e5995d33fe8bdebd74699cfc1635`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:00:11 GMT
COPY file:5143a8dee5d00da934937a160852ff57e854ce11c42fdd4828e47d5bb4df42da in /nats-server 
# Thu, 08 Dec 2022 20:00:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:00:12 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:00:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:00:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fedc572ae49bd720399deeb6a36a9250630afd1a477e3c36b0afa73c9106ee50`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 4.7 MB (4684431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8cd5d76c140f074a437a1a67876d7ccd749d332dc6908ccb8fe301cd5dde0a`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:e0e6a65a6d9b16c6fc02bc5eb03804447975e81aab5cb4ef6de5ae0e7b490c54
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2439be95ff20e36b9fc19dd178f16c99ae8deb74465c167849bbff1ae4e66612`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:4c080655f46dbff5713191574af1df195a38d3dc3d3835f7eb875699a8e32d0b in /nats-server 
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:31:19 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:31:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:31:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221d437a3d6581cb4a83aada6c1cd3cb9d173cc07d5d0e9be2c801fb03fa9abe`  
		Last Modified: Thu, 08 Dec 2022 20:32:52 GMT  
		Size: 4.7 MB (4680919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5146fbe1772138448df3c1eb3444c5077d2cdac62bc7b082c112ac5ee4be14b2`  
		Last Modified: Thu, 08 Dec 2022 20:32:51 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:95318d8cd0e5ac24a3070af64056187f97cfb83673bb66a0fd5402f484912bc2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60599b58e21ba05f3bb06c0c373f7f8e213ea6861ad81399a4472fff4a90dbad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:5e130ace514500d49e7ad10785f48a1123d8992953cabcf51a55abf452f854f0 in /nats-server 
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 19:57:18 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:57:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 19:57:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 19:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8935bb735107ae5954afbbd1ce8b5d61ad9a102c82ba176ee5fcc00d437cc63`  
		Last Modified: Thu, 08 Dec 2022 19:58:05 GMT  
		Size: 4.5 MB (4506356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e3d737971cded626be61eca795945c4a04518d6c2dc737dbd7342cac026be`  
		Last Modified: Thu, 08 Dec 2022 19:58:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:e27c1884d9603539962cb28b7a22ad496237beba12bf95e9ed49fe9afa6c86d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111653587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0454f4ce065ac9703834be6c37eabe50eb3607ecae1d7cc7b344972885eb0b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Wed, 14 Dec 2022 02:41:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:41:39 GMT
RUN cmd /S /C #(nop) COPY file:8d03b51c4d2105411f3161f01ef7aad45804539a633733d4a8a5eb9f07e4970a in C:\nats-server.exe 
# Wed, 14 Dec 2022 02:41:40 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e9d361872b14736e9b1544993bd1f54f9284833fe47bff0ed4a51b726c47d8`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75304ecf4347969762a53760eff5f595b7ded2f4bd3ddf5b100cbfe792f5eda7`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 5.0 MB (4976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bacc71a9645bdd06d67819b123d5846ca66131f4d6d357ce3be7a9ba3679ffe`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6d4bc865209ef6542a200df7b975e08fcd6ebb627c4667fb6316854f0a6051`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340559bbbd7873ac427f77173287f004fa4a4fba5395aecaa30ed6923f7823e4`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076d6856ac201aebd4e95cd5f0b55a36849f89f8f43b44db4e80dd4d0b6c1f1`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine`

```console
$ docker pull nats@sha256:c0ffa1bed32d05eebcbc9892ecfa0c37ea9f1139ef480d1bc6c8c031a8d2a78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:4455732015639b8c2fa8e9020f3d17e8a209f9d59543292710768af952148382
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8581793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3b6d7d2a01e46a077c00066353ec8f59dd1f7812c8dd98a987f5250bbd6b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:34:51 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:34:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:34:54 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:34:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:34:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed86478665b1337795c7e912325131cdc2d168214502eed69e3723ff4a234d25`  
		Last Modified: Thu, 08 Dec 2022 20:36:07 GMT  
		Size: 5.2 MB (5210085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69220328c19fd2b50424c54dca1d8a7b058aa5a162eb5ac14521e35c4d62f1a`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79d3be31b99b819fb19f51849bff6e77c2b09db3e5da0d0ef4e094ed967ff8f`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3119056346819803bc76df59c2e831ff5171a8da1f002a4607e7e2abfbe6ecee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8082503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc75fd6f64f71d7f3e687447b6480cd6f9d57bd8a4ba7c2983d8861d4e3b51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:55:46 GMT
ADD file:132c76d7f7dae2f51f589ee460f1870a2cec6e9dc7ff8e38e88fcee2cfbe70da in / 
# Tue, 22 Nov 2022 22:55:46 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:59:56 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:59:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:59:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:00:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:00:00 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:00:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c2eb4db52fbe1266a78d8c185d33544a2916faa7d82fb5f50909fe233e0579da`  
		Last Modified: Tue, 22 Nov 2022 22:56:39 GMT  
		Size: 3.1 MB (3107138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f27e96bda80af22fdcbc14d587a8bd7f1785a53f6186c176c60cb5ee041552`  
		Last Modified: Thu, 08 Dec 2022 20:01:16 GMT  
		Size: 5.0 MB (4974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3bcb78d13a5f28e8655978e2d55ca50e33f3c13cd5c589ed9ff1af70a7316f`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495e1ec935b2a91f7057d7585b3674b8243a942618d53d46882d39f719432979`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:5831f8c5ef78543c5468a18f140d4437b908d992d4d902ede67b681ae1b9d368
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7831737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a580d362e6b152069cf3b30f5e629c7e3b964a990c4a7d15e5e5c33bf6f9610a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:57:20 GMT
ADD file:080010d9005e8e0dae3e98c7f9afff3e3a40ed32579ca01946efc6ede8316bad in / 
# Tue, 22 Nov 2022 22:57:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:30:58 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:31:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:31:02 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:31:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb2ec849933dd31db64abae3fdcb6923c490d9795577bee1ee1be04eab0376ee`  
		Last Modified: Tue, 22 Nov 2022 22:58:12 GMT  
		Size: 2.9 MB (2865346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671c89e40ba9d510918522256afe00ea4e39a695355982e9f361339ed50f7d08`  
		Last Modified: Thu, 08 Dec 2022 20:32:23 GMT  
		Size: 5.0 MB (4965424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de0969a38fcc2a8858b856efe0a63cd2745e3618c370383bea1f20db57e5e0c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6d0563d82f6dafe5dc45f3a674812a38a28ae6df2f7ac30a4d7664811a572c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d6a6c27b86493e468a184154633dfddf07e4fe466ad39c6b7eeaa4609e2ed0d2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8056469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3378f00ddf68731dab0ff2d503395918d1b20713f78c76e5e28bdf22fc29d78f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:56:52 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:56:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 19:56:55 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:56:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 19:56:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986444278dadde0d9a262ed4b893f80ad454eb35ffc857e42b5ad2f073465016`  
		Last Modified: Thu, 08 Dec 2022 19:57:44 GMT  
		Size: 4.8 MB (4796278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f5d8e79ec79a470e91e51e5aa1553566f49b677c12044d8e9b5c796e0ee27e`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4e306fd7736484456b60e0960d6d29025a49f82670bf70fad13a464afa6aec`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-alpine3.17`

```console
$ docker pull nats@sha256:c0ffa1bed32d05eebcbc9892ecfa0c37ea9f1139ef480d1bc6c8c031a8d2a78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-alpine3.17` - linux; amd64

```console
$ docker pull nats@sha256:4455732015639b8c2fa8e9020f3d17e8a209f9d59543292710768af952148382
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8581793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3b6d7d2a01e46a077c00066353ec8f59dd1f7812c8dd98a987f5250bbd6b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:34:51 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:34:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:34:54 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:34:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:34:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed86478665b1337795c7e912325131cdc2d168214502eed69e3723ff4a234d25`  
		Last Modified: Thu, 08 Dec 2022 20:36:07 GMT  
		Size: 5.2 MB (5210085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69220328c19fd2b50424c54dca1d8a7b058aa5a162eb5ac14521e35c4d62f1a`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79d3be31b99b819fb19f51849bff6e77c2b09db3e5da0d0ef4e094ed967ff8f`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.17` - linux; arm variant v6

```console
$ docker pull nats@sha256:3119056346819803bc76df59c2e831ff5171a8da1f002a4607e7e2abfbe6ecee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8082503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc75fd6f64f71d7f3e687447b6480cd6f9d57bd8a4ba7c2983d8861d4e3b51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:55:46 GMT
ADD file:132c76d7f7dae2f51f589ee460f1870a2cec6e9dc7ff8e38e88fcee2cfbe70da in / 
# Tue, 22 Nov 2022 22:55:46 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:59:56 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:59:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:59:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:00:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:00:00 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:00:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c2eb4db52fbe1266a78d8c185d33544a2916faa7d82fb5f50909fe233e0579da`  
		Last Modified: Tue, 22 Nov 2022 22:56:39 GMT  
		Size: 3.1 MB (3107138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f27e96bda80af22fdcbc14d587a8bd7f1785a53f6186c176c60cb5ee041552`  
		Last Modified: Thu, 08 Dec 2022 20:01:16 GMT  
		Size: 5.0 MB (4974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3bcb78d13a5f28e8655978e2d55ca50e33f3c13cd5c589ed9ff1af70a7316f`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495e1ec935b2a91f7057d7585b3674b8243a942618d53d46882d39f719432979`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.17` - linux; arm variant v7

```console
$ docker pull nats@sha256:5831f8c5ef78543c5468a18f140d4437b908d992d4d902ede67b681ae1b9d368
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7831737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a580d362e6b152069cf3b30f5e629c7e3b964a990c4a7d15e5e5c33bf6f9610a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:57:20 GMT
ADD file:080010d9005e8e0dae3e98c7f9afff3e3a40ed32579ca01946efc6ede8316bad in / 
# Tue, 22 Nov 2022 22:57:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:30:58 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:31:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:31:02 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:31:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb2ec849933dd31db64abae3fdcb6923c490d9795577bee1ee1be04eab0376ee`  
		Last Modified: Tue, 22 Nov 2022 22:58:12 GMT  
		Size: 2.9 MB (2865346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671c89e40ba9d510918522256afe00ea4e39a695355982e9f361339ed50f7d08`  
		Last Modified: Thu, 08 Dec 2022 20:32:23 GMT  
		Size: 5.0 MB (4965424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de0969a38fcc2a8858b856efe0a63cd2745e3618c370383bea1f20db57e5e0c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6d0563d82f6dafe5dc45f3a674812a38a28ae6df2f7ac30a4d7664811a572c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d6a6c27b86493e468a184154633dfddf07e4fe466ad39c6b7eeaa4609e2ed0d2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8056469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3378f00ddf68731dab0ff2d503395918d1b20713f78c76e5e28bdf22fc29d78f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:56:52 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:56:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 19:56:55 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:56:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 19:56:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986444278dadde0d9a262ed4b893f80ad454eb35ffc857e42b5ad2f073465016`  
		Last Modified: Thu, 08 Dec 2022 19:57:44 GMT  
		Size: 4.8 MB (4796278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f5d8e79ec79a470e91e51e5aa1553566f49b677c12044d8e9b5c796e0ee27e`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4e306fd7736484456b60e0960d6d29025a49f82670bf70fad13a464afa6aec`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-linux`

```console
$ docker pull nats@sha256:da6a053c9c9f52e84383f68483bc74cb3c7caafdd89ea93fe71d475193d0c530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:79830eec98d1dc2f6acd4c63fee41a3434bc47a1b7f31cab9477de1bb3336100
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4922852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce49f767b1c3e8d858ddf7390fb3dad1b4fdebd12784b1fe33719a5a1a7993`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:d13bbefb978757216c59b4e4aba99770a0d4abdac594ab77282fb8cd6b85b588 in /nats-server 
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:35:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:35:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:35:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7692aeb9660d6587db50a4ea4f287699e633f61600a28a2d22092a82846129ce`  
		Last Modified: Thu, 08 Dec 2022 20:36:28 GMT  
		Size: 4.9 MB (4922345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022161875246986f560f72a1c52a359c684e6760487fe8f04a353168edfd2ac7`  
		Last Modified: Thu, 08 Dec 2022 20:36:27 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:24970d929b8d8ecf8887fb00bd92ce687fa3b252218c033614bbc892eec3c380
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4684937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac2c7d543ae2d436c8f9381f98b0bf06c08e5995d33fe8bdebd74699cfc1635`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:00:11 GMT
COPY file:5143a8dee5d00da934937a160852ff57e854ce11c42fdd4828e47d5bb4df42da in /nats-server 
# Thu, 08 Dec 2022 20:00:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:00:12 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:00:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:00:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fedc572ae49bd720399deeb6a36a9250630afd1a477e3c36b0afa73c9106ee50`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 4.7 MB (4684431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8cd5d76c140f074a437a1a67876d7ccd749d332dc6908ccb8fe301cd5dde0a`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:e0e6a65a6d9b16c6fc02bc5eb03804447975e81aab5cb4ef6de5ae0e7b490c54
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2439be95ff20e36b9fc19dd178f16c99ae8deb74465c167849bbff1ae4e66612`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:4c080655f46dbff5713191574af1df195a38d3dc3d3835f7eb875699a8e32d0b in /nats-server 
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:31:19 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:31:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:31:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221d437a3d6581cb4a83aada6c1cd3cb9d173cc07d5d0e9be2c801fb03fa9abe`  
		Last Modified: Thu, 08 Dec 2022 20:32:52 GMT  
		Size: 4.7 MB (4680919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5146fbe1772138448df3c1eb3444c5077d2cdac62bc7b082c112ac5ee4be14b2`  
		Last Modified: Thu, 08 Dec 2022 20:32:51 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:95318d8cd0e5ac24a3070af64056187f97cfb83673bb66a0fd5402f484912bc2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60599b58e21ba05f3bb06c0c373f7f8e213ea6861ad81399a4472fff4a90dbad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:5e130ace514500d49e7ad10785f48a1123d8992953cabcf51a55abf452f854f0 in /nats-server 
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 19:57:18 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:57:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 19:57:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 19:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8935bb735107ae5954afbbd1ce8b5d61ad9a102c82ba176ee5fcc00d437cc63`  
		Last Modified: Thu, 08 Dec 2022 19:58:05 GMT  
		Size: 4.5 MB (4506356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e3d737971cded626be61eca795945c4a04518d6c2dc737dbd7342cac026be`  
		Last Modified: Thu, 08 Dec 2022 19:58:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver`

```console
$ docker pull nats@sha256:794c09f7a1b633fc92984035474e997ea88e32a22b4db214410f58a95e348a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:2.9-nanoserver` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:e27c1884d9603539962cb28b7a22ad496237beba12bf95e9ed49fe9afa6c86d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111653587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0454f4ce065ac9703834be6c37eabe50eb3607ecae1d7cc7b344972885eb0b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Wed, 14 Dec 2022 02:41:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:41:39 GMT
RUN cmd /S /C #(nop) COPY file:8d03b51c4d2105411f3161f01ef7aad45804539a633733d4a8a5eb9f07e4970a in C:\nats-server.exe 
# Wed, 14 Dec 2022 02:41:40 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e9d361872b14736e9b1544993bd1f54f9284833fe47bff0ed4a51b726c47d8`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75304ecf4347969762a53760eff5f595b7ded2f4bd3ddf5b100cbfe792f5eda7`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 5.0 MB (4976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bacc71a9645bdd06d67819b123d5846ca66131f4d6d357ce3be7a9ba3679ffe`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6d4bc865209ef6542a200df7b975e08fcd6ebb627c4667fb6316854f0a6051`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340559bbbd7873ac427f77173287f004fa4a4fba5395aecaa30ed6923f7823e4`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076d6856ac201aebd4e95cd5f0b55a36849f89f8f43b44db4e80dd4d0b6c1f1`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-nanoserver-1809`

```console
$ docker pull nats@sha256:794c09f7a1b633fc92984035474e997ea88e32a22b4db214410f58a95e348a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:2.9-nanoserver-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:e27c1884d9603539962cb28b7a22ad496237beba12bf95e9ed49fe9afa6c86d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111653587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0454f4ce065ac9703834be6c37eabe50eb3607ecae1d7cc7b344972885eb0b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Wed, 14 Dec 2022 02:41:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:41:39 GMT
RUN cmd /S /C #(nop) COPY file:8d03b51c4d2105411f3161f01ef7aad45804539a633733d4a8a5eb9f07e4970a in C:\nats-server.exe 
# Wed, 14 Dec 2022 02:41:40 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e9d361872b14736e9b1544993bd1f54f9284833fe47bff0ed4a51b726c47d8`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75304ecf4347969762a53760eff5f595b7ded2f4bd3ddf5b100cbfe792f5eda7`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 5.0 MB (4976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bacc71a9645bdd06d67819b123d5846ca66131f4d6d357ce3be7a9ba3679ffe`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6d4bc865209ef6542a200df7b975e08fcd6ebb627c4667fb6316854f0a6051`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340559bbbd7873ac427f77173287f004fa4a4fba5395aecaa30ed6923f7823e4`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076d6856ac201aebd4e95cd5f0b55a36849f89f8f43b44db4e80dd4d0b6c1f1`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-scratch`

```console
$ docker pull nats@sha256:da6a053c9c9f52e84383f68483bc74cb3c7caafdd89ea93fe71d475193d0c530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:79830eec98d1dc2f6acd4c63fee41a3434bc47a1b7f31cab9477de1bb3336100
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4922852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce49f767b1c3e8d858ddf7390fb3dad1b4fdebd12784b1fe33719a5a1a7993`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:d13bbefb978757216c59b4e4aba99770a0d4abdac594ab77282fb8cd6b85b588 in /nats-server 
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:35:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:35:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:35:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7692aeb9660d6587db50a4ea4f287699e633f61600a28a2d22092a82846129ce`  
		Last Modified: Thu, 08 Dec 2022 20:36:28 GMT  
		Size: 4.9 MB (4922345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022161875246986f560f72a1c52a359c684e6760487fe8f04a353168edfd2ac7`  
		Last Modified: Thu, 08 Dec 2022 20:36:27 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:24970d929b8d8ecf8887fb00bd92ce687fa3b252218c033614bbc892eec3c380
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4684937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac2c7d543ae2d436c8f9381f98b0bf06c08e5995d33fe8bdebd74699cfc1635`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:00:11 GMT
COPY file:5143a8dee5d00da934937a160852ff57e854ce11c42fdd4828e47d5bb4df42da in /nats-server 
# Thu, 08 Dec 2022 20:00:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:00:12 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:00:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:00:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fedc572ae49bd720399deeb6a36a9250630afd1a477e3c36b0afa73c9106ee50`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 4.7 MB (4684431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8cd5d76c140f074a437a1a67876d7ccd749d332dc6908ccb8fe301cd5dde0a`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:e0e6a65a6d9b16c6fc02bc5eb03804447975e81aab5cb4ef6de5ae0e7b490c54
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2439be95ff20e36b9fc19dd178f16c99ae8deb74465c167849bbff1ae4e66612`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:4c080655f46dbff5713191574af1df195a38d3dc3d3835f7eb875699a8e32d0b in /nats-server 
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:31:19 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:31:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:31:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221d437a3d6581cb4a83aada6c1cd3cb9d173cc07d5d0e9be2c801fb03fa9abe`  
		Last Modified: Thu, 08 Dec 2022 20:32:52 GMT  
		Size: 4.7 MB (4680919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5146fbe1772138448df3c1eb3444c5077d2cdac62bc7b082c112ac5ee4be14b2`  
		Last Modified: Thu, 08 Dec 2022 20:32:51 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:95318d8cd0e5ac24a3070af64056187f97cfb83673bb66a0fd5402f484912bc2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60599b58e21ba05f3bb06c0c373f7f8e213ea6861ad81399a4472fff4a90dbad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:5e130ace514500d49e7ad10785f48a1123d8992953cabcf51a55abf452f854f0 in /nats-server 
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 19:57:18 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:57:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 19:57:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 19:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8935bb735107ae5954afbbd1ce8b5d61ad9a102c82ba176ee5fcc00d437cc63`  
		Last Modified: Thu, 08 Dec 2022 19:58:05 GMT  
		Size: 4.5 MB (4506356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e3d737971cded626be61eca795945c4a04518d6c2dc737dbd7342cac026be`  
		Last Modified: Thu, 08 Dec 2022 19:58:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore`

```console
$ docker pull nats@sha256:bd5262b0964a38e7e28de29632b03d507ba57fc832bb3171567478da841d9f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:2.9-windowsservercore` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:11e1ab562299ebbb64ab18c5afd891fa67655420780a109677a922340d8777d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2786352699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6dc041a550a2790319a7bb1f8b2b6bc818495c7300afc3226fc2da4d42219a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sun, 11 Dec 2022 08:04:49 GMT
RUN Install update 10.0.17763.3770
# Wed, 14 Dec 2022 01:29:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Dec 2022 02:37:16 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:37:17 GMT
ENV NATS_SERVER=2.9.9
# Wed, 14 Dec 2022 02:37:18 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.9/nats-server-v2.9.9-windows-amd64.zip
# Wed, 14 Dec 2022 02:37:19 GMT
ENV NATS_SERVER_SHASUM=a3456ed1a8f02d9d8ced35a1adbe1f6451af0c303f87ff74c15879dfc8cabd30
# Wed, 14 Dec 2022 02:38:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Dec 2022 02:41:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Dec 2022 02:41:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:20 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ad73ed772f80ab7923579a55dd12fb9b6e090d1d836408d16ffd9d3dee252`  
		Last Modified: Tue, 13 Dec 2022 23:56:47 GMT  
		Size: 856.4 MB (856427878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1d7d21a6f8359d8228f44b50aa9ad552783452100b6ce203e8f042415b5623`  
		Last Modified: Wed, 14 Dec 2022 02:14:22 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2b4fa0f968fba4be86c61da602c6d1d95bea2a5b257fa97e5cb498f7ddc7fe`  
		Last Modified: Wed, 14 Dec 2022 02:42:16 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1296500fbd02b72d68a4f8d4c78bb6c35ddaaa2c332cfe9254604281a913a00`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50931b0d887f06faade1d2051e8cceac2255778e1b4b9653fc75474db54b489d`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d625cf2ad988d5ac80b24112ef78da7fe7bddd4b5d188962fcb3ab90f04b57e`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f665d13d7cbc9a4ce6c8e5bc9120d5e3343377d7211f1e4d12480ddda591f522`  
		Last Modified: Wed, 14 Dec 2022 02:42:15 GMT  
		Size: 342.0 KB (342028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75307c50ea67f0603708dfc03956f1d610f261a5fa0f54d064b1690b0f866274`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 5.3 MB (5300085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1799e7de223a25ae30a351e317b449f128c31f00e818c0df0b02a4be360e4cf3`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 2.0 KB (1962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfeddb4c41b8d5fdc840c446ef490340728041b9202f2db80dce668c9d8d8ca5`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb917ab1b2406dc49a3fcc8fe92a27023ef822724a7c3056fa6f14ea3eca9d09`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2920025a2b586dcc5fa9b1580994f3bedbdbc128a7ab0a5c9bba8ca690025e0e`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:bd5262b0964a38e7e28de29632b03d507ba57fc832bb3171567478da841d9f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:2.9-windowsservercore-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:11e1ab562299ebbb64ab18c5afd891fa67655420780a109677a922340d8777d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2786352699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6dc041a550a2790319a7bb1f8b2b6bc818495c7300afc3226fc2da4d42219a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sun, 11 Dec 2022 08:04:49 GMT
RUN Install update 10.0.17763.3770
# Wed, 14 Dec 2022 01:29:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Dec 2022 02:37:16 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:37:17 GMT
ENV NATS_SERVER=2.9.9
# Wed, 14 Dec 2022 02:37:18 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.9/nats-server-v2.9.9-windows-amd64.zip
# Wed, 14 Dec 2022 02:37:19 GMT
ENV NATS_SERVER_SHASUM=a3456ed1a8f02d9d8ced35a1adbe1f6451af0c303f87ff74c15879dfc8cabd30
# Wed, 14 Dec 2022 02:38:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Dec 2022 02:41:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Dec 2022 02:41:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:20 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ad73ed772f80ab7923579a55dd12fb9b6e090d1d836408d16ffd9d3dee252`  
		Last Modified: Tue, 13 Dec 2022 23:56:47 GMT  
		Size: 856.4 MB (856427878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1d7d21a6f8359d8228f44b50aa9ad552783452100b6ce203e8f042415b5623`  
		Last Modified: Wed, 14 Dec 2022 02:14:22 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2b4fa0f968fba4be86c61da602c6d1d95bea2a5b257fa97e5cb498f7ddc7fe`  
		Last Modified: Wed, 14 Dec 2022 02:42:16 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1296500fbd02b72d68a4f8d4c78bb6c35ddaaa2c332cfe9254604281a913a00`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50931b0d887f06faade1d2051e8cceac2255778e1b4b9653fc75474db54b489d`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d625cf2ad988d5ac80b24112ef78da7fe7bddd4b5d188962fcb3ab90f04b57e`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f665d13d7cbc9a4ce6c8e5bc9120d5e3343377d7211f1e4d12480ddda591f522`  
		Last Modified: Wed, 14 Dec 2022 02:42:15 GMT  
		Size: 342.0 KB (342028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75307c50ea67f0603708dfc03956f1d610f261a5fa0f54d064b1690b0f866274`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 5.3 MB (5300085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1799e7de223a25ae30a351e317b449f128c31f00e818c0df0b02a4be360e4cf3`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 2.0 KB (1962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfeddb4c41b8d5fdc840c446ef490340728041b9202f2db80dce668c9d8d8ca5`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb917ab1b2406dc49a3fcc8fe92a27023ef822724a7c3056fa6f14ea3eca9d09`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2920025a2b586dcc5fa9b1580994f3bedbdbc128a7ab0a5c9bba8ca690025e0e`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.9`

```console
$ docker pull nats@sha256:e4c75014ae278dcb8192c9718c7c0cebfb55cb76c41b285a1663141794ab96f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3770; amd64

### `nats:2.9.9` - linux; amd64

```console
$ docker pull nats@sha256:79830eec98d1dc2f6acd4c63fee41a3434bc47a1b7f31cab9477de1bb3336100
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4922852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce49f767b1c3e8d858ddf7390fb3dad1b4fdebd12784b1fe33719a5a1a7993`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:d13bbefb978757216c59b4e4aba99770a0d4abdac594ab77282fb8cd6b85b588 in /nats-server 
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:35:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:35:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:35:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7692aeb9660d6587db50a4ea4f287699e633f61600a28a2d22092a82846129ce`  
		Last Modified: Thu, 08 Dec 2022 20:36:28 GMT  
		Size: 4.9 MB (4922345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022161875246986f560f72a1c52a359c684e6760487fe8f04a353168edfd2ac7`  
		Last Modified: Thu, 08 Dec 2022 20:36:27 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:24970d929b8d8ecf8887fb00bd92ce687fa3b252218c033614bbc892eec3c380
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4684937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac2c7d543ae2d436c8f9381f98b0bf06c08e5995d33fe8bdebd74699cfc1635`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:00:11 GMT
COPY file:5143a8dee5d00da934937a160852ff57e854ce11c42fdd4828e47d5bb4df42da in /nats-server 
# Thu, 08 Dec 2022 20:00:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:00:12 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:00:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:00:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fedc572ae49bd720399deeb6a36a9250630afd1a477e3c36b0afa73c9106ee50`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 4.7 MB (4684431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8cd5d76c140f074a437a1a67876d7ccd749d332dc6908ccb8fe301cd5dde0a`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:e0e6a65a6d9b16c6fc02bc5eb03804447975e81aab5cb4ef6de5ae0e7b490c54
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2439be95ff20e36b9fc19dd178f16c99ae8deb74465c167849bbff1ae4e66612`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:4c080655f46dbff5713191574af1df195a38d3dc3d3835f7eb875699a8e32d0b in /nats-server 
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:31:19 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:31:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:31:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221d437a3d6581cb4a83aada6c1cd3cb9d173cc07d5d0e9be2c801fb03fa9abe`  
		Last Modified: Thu, 08 Dec 2022 20:32:52 GMT  
		Size: 4.7 MB (4680919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5146fbe1772138448df3c1eb3444c5077d2cdac62bc7b082c112ac5ee4be14b2`  
		Last Modified: Thu, 08 Dec 2022 20:32:51 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:95318d8cd0e5ac24a3070af64056187f97cfb83673bb66a0fd5402f484912bc2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60599b58e21ba05f3bb06c0c373f7f8e213ea6861ad81399a4472fff4a90dbad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:5e130ace514500d49e7ad10785f48a1123d8992953cabcf51a55abf452f854f0 in /nats-server 
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 19:57:18 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:57:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 19:57:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 19:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8935bb735107ae5954afbbd1ce8b5d61ad9a102c82ba176ee5fcc00d437cc63`  
		Last Modified: Thu, 08 Dec 2022 19:58:05 GMT  
		Size: 4.5 MB (4506356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e3d737971cded626be61eca795945c4a04518d6c2dc737dbd7342cac026be`  
		Last Modified: Thu, 08 Dec 2022 19:58:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.9` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:e27c1884d9603539962cb28b7a22ad496237beba12bf95e9ed49fe9afa6c86d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111653587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0454f4ce065ac9703834be6c37eabe50eb3607ecae1d7cc7b344972885eb0b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Wed, 14 Dec 2022 02:41:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:41:39 GMT
RUN cmd /S /C #(nop) COPY file:8d03b51c4d2105411f3161f01ef7aad45804539a633733d4a8a5eb9f07e4970a in C:\nats-server.exe 
# Wed, 14 Dec 2022 02:41:40 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e9d361872b14736e9b1544993bd1f54f9284833fe47bff0ed4a51b726c47d8`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75304ecf4347969762a53760eff5f595b7ded2f4bd3ddf5b100cbfe792f5eda7`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 5.0 MB (4976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bacc71a9645bdd06d67819b123d5846ca66131f4d6d357ce3be7a9ba3679ffe`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6d4bc865209ef6542a200df7b975e08fcd6ebb627c4667fb6316854f0a6051`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340559bbbd7873ac427f77173287f004fa4a4fba5395aecaa30ed6923f7823e4`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076d6856ac201aebd4e95cd5f0b55a36849f89f8f43b44db4e80dd4d0b6c1f1`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.9-alpine`

```console
$ docker pull nats@sha256:c0ffa1bed32d05eebcbc9892ecfa0c37ea9f1139ef480d1bc6c8c031a8d2a78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:4455732015639b8c2fa8e9020f3d17e8a209f9d59543292710768af952148382
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8581793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3b6d7d2a01e46a077c00066353ec8f59dd1f7812c8dd98a987f5250bbd6b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:34:51 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:34:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:34:54 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:34:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:34:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed86478665b1337795c7e912325131cdc2d168214502eed69e3723ff4a234d25`  
		Last Modified: Thu, 08 Dec 2022 20:36:07 GMT  
		Size: 5.2 MB (5210085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69220328c19fd2b50424c54dca1d8a7b058aa5a162eb5ac14521e35c4d62f1a`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79d3be31b99b819fb19f51849bff6e77c2b09db3e5da0d0ef4e094ed967ff8f`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3119056346819803bc76df59c2e831ff5171a8da1f002a4607e7e2abfbe6ecee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8082503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc75fd6f64f71d7f3e687447b6480cd6f9d57bd8a4ba7c2983d8861d4e3b51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:55:46 GMT
ADD file:132c76d7f7dae2f51f589ee460f1870a2cec6e9dc7ff8e38e88fcee2cfbe70da in / 
# Tue, 22 Nov 2022 22:55:46 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:59:56 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:59:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:59:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:00:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:00:00 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:00:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c2eb4db52fbe1266a78d8c185d33544a2916faa7d82fb5f50909fe233e0579da`  
		Last Modified: Tue, 22 Nov 2022 22:56:39 GMT  
		Size: 3.1 MB (3107138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f27e96bda80af22fdcbc14d587a8bd7f1785a53f6186c176c60cb5ee041552`  
		Last Modified: Thu, 08 Dec 2022 20:01:16 GMT  
		Size: 5.0 MB (4974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3bcb78d13a5f28e8655978e2d55ca50e33f3c13cd5c589ed9ff1af70a7316f`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495e1ec935b2a91f7057d7585b3674b8243a942618d53d46882d39f719432979`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:5831f8c5ef78543c5468a18f140d4437b908d992d4d902ede67b681ae1b9d368
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7831737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a580d362e6b152069cf3b30f5e629c7e3b964a990c4a7d15e5e5c33bf6f9610a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:57:20 GMT
ADD file:080010d9005e8e0dae3e98c7f9afff3e3a40ed32579ca01946efc6ede8316bad in / 
# Tue, 22 Nov 2022 22:57:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:30:58 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:31:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:31:02 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:31:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb2ec849933dd31db64abae3fdcb6923c490d9795577bee1ee1be04eab0376ee`  
		Last Modified: Tue, 22 Nov 2022 22:58:12 GMT  
		Size: 2.9 MB (2865346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671c89e40ba9d510918522256afe00ea4e39a695355982e9f361339ed50f7d08`  
		Last Modified: Thu, 08 Dec 2022 20:32:23 GMT  
		Size: 5.0 MB (4965424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de0969a38fcc2a8858b856efe0a63cd2745e3618c370383bea1f20db57e5e0c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6d0563d82f6dafe5dc45f3a674812a38a28ae6df2f7ac30a4d7664811a572c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d6a6c27b86493e468a184154633dfddf07e4fe466ad39c6b7eeaa4609e2ed0d2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8056469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3378f00ddf68731dab0ff2d503395918d1b20713f78c76e5e28bdf22fc29d78f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:56:52 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:56:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 19:56:55 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:56:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 19:56:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986444278dadde0d9a262ed4b893f80ad454eb35ffc857e42b5ad2f073465016`  
		Last Modified: Thu, 08 Dec 2022 19:57:44 GMT  
		Size: 4.8 MB (4796278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f5d8e79ec79a470e91e51e5aa1553566f49b677c12044d8e9b5c796e0ee27e`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4e306fd7736484456b60e0960d6d29025a49f82670bf70fad13a464afa6aec`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.9-alpine3.17`

```console
$ docker pull nats@sha256:c0ffa1bed32d05eebcbc9892ecfa0c37ea9f1139ef480d1bc6c8c031a8d2a78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.9-alpine3.17` - linux; amd64

```console
$ docker pull nats@sha256:4455732015639b8c2fa8e9020f3d17e8a209f9d59543292710768af952148382
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8581793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3b6d7d2a01e46a077c00066353ec8f59dd1f7812c8dd98a987f5250bbd6b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:34:51 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:34:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:34:54 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:34:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:34:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed86478665b1337795c7e912325131cdc2d168214502eed69e3723ff4a234d25`  
		Last Modified: Thu, 08 Dec 2022 20:36:07 GMT  
		Size: 5.2 MB (5210085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69220328c19fd2b50424c54dca1d8a7b058aa5a162eb5ac14521e35c4d62f1a`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79d3be31b99b819fb19f51849bff6e77c2b09db3e5da0d0ef4e094ed967ff8f`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.9-alpine3.17` - linux; arm variant v6

```console
$ docker pull nats@sha256:3119056346819803bc76df59c2e831ff5171a8da1f002a4607e7e2abfbe6ecee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8082503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc75fd6f64f71d7f3e687447b6480cd6f9d57bd8a4ba7c2983d8861d4e3b51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:55:46 GMT
ADD file:132c76d7f7dae2f51f589ee460f1870a2cec6e9dc7ff8e38e88fcee2cfbe70da in / 
# Tue, 22 Nov 2022 22:55:46 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:59:56 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:59:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:59:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:00:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:00:00 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:00:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c2eb4db52fbe1266a78d8c185d33544a2916faa7d82fb5f50909fe233e0579da`  
		Last Modified: Tue, 22 Nov 2022 22:56:39 GMT  
		Size: 3.1 MB (3107138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f27e96bda80af22fdcbc14d587a8bd7f1785a53f6186c176c60cb5ee041552`  
		Last Modified: Thu, 08 Dec 2022 20:01:16 GMT  
		Size: 5.0 MB (4974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3bcb78d13a5f28e8655978e2d55ca50e33f3c13cd5c589ed9ff1af70a7316f`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495e1ec935b2a91f7057d7585b3674b8243a942618d53d46882d39f719432979`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.9-alpine3.17` - linux; arm variant v7

```console
$ docker pull nats@sha256:5831f8c5ef78543c5468a18f140d4437b908d992d4d902ede67b681ae1b9d368
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7831737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a580d362e6b152069cf3b30f5e629c7e3b964a990c4a7d15e5e5c33bf6f9610a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:57:20 GMT
ADD file:080010d9005e8e0dae3e98c7f9afff3e3a40ed32579ca01946efc6ede8316bad in / 
# Tue, 22 Nov 2022 22:57:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:30:58 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:31:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:31:02 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:31:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb2ec849933dd31db64abae3fdcb6923c490d9795577bee1ee1be04eab0376ee`  
		Last Modified: Tue, 22 Nov 2022 22:58:12 GMT  
		Size: 2.9 MB (2865346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671c89e40ba9d510918522256afe00ea4e39a695355982e9f361339ed50f7d08`  
		Last Modified: Thu, 08 Dec 2022 20:32:23 GMT  
		Size: 5.0 MB (4965424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de0969a38fcc2a8858b856efe0a63cd2745e3618c370383bea1f20db57e5e0c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6d0563d82f6dafe5dc45f3a674812a38a28ae6df2f7ac30a4d7664811a572c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.9-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d6a6c27b86493e468a184154633dfddf07e4fe466ad39c6b7eeaa4609e2ed0d2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8056469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3378f00ddf68731dab0ff2d503395918d1b20713f78c76e5e28bdf22fc29d78f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:56:52 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:56:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 19:56:55 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:56:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 19:56:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986444278dadde0d9a262ed4b893f80ad454eb35ffc857e42b5ad2f073465016`  
		Last Modified: Thu, 08 Dec 2022 19:57:44 GMT  
		Size: 4.8 MB (4796278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f5d8e79ec79a470e91e51e5aa1553566f49b677c12044d8e9b5c796e0ee27e`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4e306fd7736484456b60e0960d6d29025a49f82670bf70fad13a464afa6aec`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.9-linux`

```console
$ docker pull nats@sha256:da6a053c9c9f52e84383f68483bc74cb3c7caafdd89ea93fe71d475193d0c530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:79830eec98d1dc2f6acd4c63fee41a3434bc47a1b7f31cab9477de1bb3336100
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4922852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce49f767b1c3e8d858ddf7390fb3dad1b4fdebd12784b1fe33719a5a1a7993`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:d13bbefb978757216c59b4e4aba99770a0d4abdac594ab77282fb8cd6b85b588 in /nats-server 
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:35:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:35:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:35:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7692aeb9660d6587db50a4ea4f287699e633f61600a28a2d22092a82846129ce`  
		Last Modified: Thu, 08 Dec 2022 20:36:28 GMT  
		Size: 4.9 MB (4922345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022161875246986f560f72a1c52a359c684e6760487fe8f04a353168edfd2ac7`  
		Last Modified: Thu, 08 Dec 2022 20:36:27 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:24970d929b8d8ecf8887fb00bd92ce687fa3b252218c033614bbc892eec3c380
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4684937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac2c7d543ae2d436c8f9381f98b0bf06c08e5995d33fe8bdebd74699cfc1635`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:00:11 GMT
COPY file:5143a8dee5d00da934937a160852ff57e854ce11c42fdd4828e47d5bb4df42da in /nats-server 
# Thu, 08 Dec 2022 20:00:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:00:12 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:00:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:00:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fedc572ae49bd720399deeb6a36a9250630afd1a477e3c36b0afa73c9106ee50`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 4.7 MB (4684431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8cd5d76c140f074a437a1a67876d7ccd749d332dc6908ccb8fe301cd5dde0a`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:e0e6a65a6d9b16c6fc02bc5eb03804447975e81aab5cb4ef6de5ae0e7b490c54
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2439be95ff20e36b9fc19dd178f16c99ae8deb74465c167849bbff1ae4e66612`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:4c080655f46dbff5713191574af1df195a38d3dc3d3835f7eb875699a8e32d0b in /nats-server 
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:31:19 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:31:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:31:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221d437a3d6581cb4a83aada6c1cd3cb9d173cc07d5d0e9be2c801fb03fa9abe`  
		Last Modified: Thu, 08 Dec 2022 20:32:52 GMT  
		Size: 4.7 MB (4680919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5146fbe1772138448df3c1eb3444c5077d2cdac62bc7b082c112ac5ee4be14b2`  
		Last Modified: Thu, 08 Dec 2022 20:32:51 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:95318d8cd0e5ac24a3070af64056187f97cfb83673bb66a0fd5402f484912bc2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60599b58e21ba05f3bb06c0c373f7f8e213ea6861ad81399a4472fff4a90dbad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:5e130ace514500d49e7ad10785f48a1123d8992953cabcf51a55abf452f854f0 in /nats-server 
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 19:57:18 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:57:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 19:57:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 19:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8935bb735107ae5954afbbd1ce8b5d61ad9a102c82ba176ee5fcc00d437cc63`  
		Last Modified: Thu, 08 Dec 2022 19:58:05 GMT  
		Size: 4.5 MB (4506356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e3d737971cded626be61eca795945c4a04518d6c2dc737dbd7342cac026be`  
		Last Modified: Thu, 08 Dec 2022 19:58:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.9-nanoserver`

```console
$ docker pull nats@sha256:794c09f7a1b633fc92984035474e997ea88e32a22b4db214410f58a95e348a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:2.9.9-nanoserver` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:e27c1884d9603539962cb28b7a22ad496237beba12bf95e9ed49fe9afa6c86d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111653587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0454f4ce065ac9703834be6c37eabe50eb3607ecae1d7cc7b344972885eb0b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Wed, 14 Dec 2022 02:41:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:41:39 GMT
RUN cmd /S /C #(nop) COPY file:8d03b51c4d2105411f3161f01ef7aad45804539a633733d4a8a5eb9f07e4970a in C:\nats-server.exe 
# Wed, 14 Dec 2022 02:41:40 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e9d361872b14736e9b1544993bd1f54f9284833fe47bff0ed4a51b726c47d8`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75304ecf4347969762a53760eff5f595b7ded2f4bd3ddf5b100cbfe792f5eda7`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 5.0 MB (4976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bacc71a9645bdd06d67819b123d5846ca66131f4d6d357ce3be7a9ba3679ffe`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6d4bc865209ef6542a200df7b975e08fcd6ebb627c4667fb6316854f0a6051`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340559bbbd7873ac427f77173287f004fa4a4fba5395aecaa30ed6923f7823e4`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076d6856ac201aebd4e95cd5f0b55a36849f89f8f43b44db4e80dd4d0b6c1f1`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.9-nanoserver-1809`

```console
$ docker pull nats@sha256:794c09f7a1b633fc92984035474e997ea88e32a22b4db214410f58a95e348a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:2.9.9-nanoserver-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:e27c1884d9603539962cb28b7a22ad496237beba12bf95e9ed49fe9afa6c86d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111653587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0454f4ce065ac9703834be6c37eabe50eb3607ecae1d7cc7b344972885eb0b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Wed, 14 Dec 2022 02:41:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:41:39 GMT
RUN cmd /S /C #(nop) COPY file:8d03b51c4d2105411f3161f01ef7aad45804539a633733d4a8a5eb9f07e4970a in C:\nats-server.exe 
# Wed, 14 Dec 2022 02:41:40 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e9d361872b14736e9b1544993bd1f54f9284833fe47bff0ed4a51b726c47d8`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75304ecf4347969762a53760eff5f595b7ded2f4bd3ddf5b100cbfe792f5eda7`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 5.0 MB (4976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bacc71a9645bdd06d67819b123d5846ca66131f4d6d357ce3be7a9ba3679ffe`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6d4bc865209ef6542a200df7b975e08fcd6ebb627c4667fb6316854f0a6051`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340559bbbd7873ac427f77173287f004fa4a4fba5395aecaa30ed6923f7823e4`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076d6856ac201aebd4e95cd5f0b55a36849f89f8f43b44db4e80dd4d0b6c1f1`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.9-scratch`

```console
$ docker pull nats@sha256:da6a053c9c9f52e84383f68483bc74cb3c7caafdd89ea93fe71d475193d0c530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.9.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:79830eec98d1dc2f6acd4c63fee41a3434bc47a1b7f31cab9477de1bb3336100
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4922852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce49f767b1c3e8d858ddf7390fb3dad1b4fdebd12784b1fe33719a5a1a7993`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:d13bbefb978757216c59b4e4aba99770a0d4abdac594ab77282fb8cd6b85b588 in /nats-server 
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:35:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:35:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:35:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7692aeb9660d6587db50a4ea4f287699e633f61600a28a2d22092a82846129ce`  
		Last Modified: Thu, 08 Dec 2022 20:36:28 GMT  
		Size: 4.9 MB (4922345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022161875246986f560f72a1c52a359c684e6760487fe8f04a353168edfd2ac7`  
		Last Modified: Thu, 08 Dec 2022 20:36:27 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:24970d929b8d8ecf8887fb00bd92ce687fa3b252218c033614bbc892eec3c380
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4684937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac2c7d543ae2d436c8f9381f98b0bf06c08e5995d33fe8bdebd74699cfc1635`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:00:11 GMT
COPY file:5143a8dee5d00da934937a160852ff57e854ce11c42fdd4828e47d5bb4df42da in /nats-server 
# Thu, 08 Dec 2022 20:00:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:00:12 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:00:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:00:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fedc572ae49bd720399deeb6a36a9250630afd1a477e3c36b0afa73c9106ee50`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 4.7 MB (4684431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8cd5d76c140f074a437a1a67876d7ccd749d332dc6908ccb8fe301cd5dde0a`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:e0e6a65a6d9b16c6fc02bc5eb03804447975e81aab5cb4ef6de5ae0e7b490c54
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2439be95ff20e36b9fc19dd178f16c99ae8deb74465c167849bbff1ae4e66612`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:4c080655f46dbff5713191574af1df195a38d3dc3d3835f7eb875699a8e32d0b in /nats-server 
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:31:19 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:31:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:31:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221d437a3d6581cb4a83aada6c1cd3cb9d173cc07d5d0e9be2c801fb03fa9abe`  
		Last Modified: Thu, 08 Dec 2022 20:32:52 GMT  
		Size: 4.7 MB (4680919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5146fbe1772138448df3c1eb3444c5077d2cdac62bc7b082c112ac5ee4be14b2`  
		Last Modified: Thu, 08 Dec 2022 20:32:51 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.9.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:95318d8cd0e5ac24a3070af64056187f97cfb83673bb66a0fd5402f484912bc2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60599b58e21ba05f3bb06c0c373f7f8e213ea6861ad81399a4472fff4a90dbad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:5e130ace514500d49e7ad10785f48a1123d8992953cabcf51a55abf452f854f0 in /nats-server 
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 19:57:18 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:57:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 19:57:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 19:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8935bb735107ae5954afbbd1ce8b5d61ad9a102c82ba176ee5fcc00d437cc63`  
		Last Modified: Thu, 08 Dec 2022 19:58:05 GMT  
		Size: 4.5 MB (4506356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e3d737971cded626be61eca795945c4a04518d6c2dc737dbd7342cac026be`  
		Last Modified: Thu, 08 Dec 2022 19:58:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.9-windowsservercore`

```console
$ docker pull nats@sha256:bd5262b0964a38e7e28de29632b03d507ba57fc832bb3171567478da841d9f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:2.9.9-windowsservercore` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:11e1ab562299ebbb64ab18c5afd891fa67655420780a109677a922340d8777d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2786352699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6dc041a550a2790319a7bb1f8b2b6bc818495c7300afc3226fc2da4d42219a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sun, 11 Dec 2022 08:04:49 GMT
RUN Install update 10.0.17763.3770
# Wed, 14 Dec 2022 01:29:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Dec 2022 02:37:16 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:37:17 GMT
ENV NATS_SERVER=2.9.9
# Wed, 14 Dec 2022 02:37:18 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.9/nats-server-v2.9.9-windows-amd64.zip
# Wed, 14 Dec 2022 02:37:19 GMT
ENV NATS_SERVER_SHASUM=a3456ed1a8f02d9d8ced35a1adbe1f6451af0c303f87ff74c15879dfc8cabd30
# Wed, 14 Dec 2022 02:38:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Dec 2022 02:41:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Dec 2022 02:41:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:20 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ad73ed772f80ab7923579a55dd12fb9b6e090d1d836408d16ffd9d3dee252`  
		Last Modified: Tue, 13 Dec 2022 23:56:47 GMT  
		Size: 856.4 MB (856427878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1d7d21a6f8359d8228f44b50aa9ad552783452100b6ce203e8f042415b5623`  
		Last Modified: Wed, 14 Dec 2022 02:14:22 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2b4fa0f968fba4be86c61da602c6d1d95bea2a5b257fa97e5cb498f7ddc7fe`  
		Last Modified: Wed, 14 Dec 2022 02:42:16 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1296500fbd02b72d68a4f8d4c78bb6c35ddaaa2c332cfe9254604281a913a00`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50931b0d887f06faade1d2051e8cceac2255778e1b4b9653fc75474db54b489d`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d625cf2ad988d5ac80b24112ef78da7fe7bddd4b5d188962fcb3ab90f04b57e`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f665d13d7cbc9a4ce6c8e5bc9120d5e3343377d7211f1e4d12480ddda591f522`  
		Last Modified: Wed, 14 Dec 2022 02:42:15 GMT  
		Size: 342.0 KB (342028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75307c50ea67f0603708dfc03956f1d610f261a5fa0f54d064b1690b0f866274`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 5.3 MB (5300085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1799e7de223a25ae30a351e317b449f128c31f00e818c0df0b02a4be360e4cf3`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 2.0 KB (1962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfeddb4c41b8d5fdc840c446ef490340728041b9202f2db80dce668c9d8d8ca5`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb917ab1b2406dc49a3fcc8fe92a27023ef822724a7c3056fa6f14ea3eca9d09`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2920025a2b586dcc5fa9b1580994f3bedbdbc128a7ab0a5c9bba8ca690025e0e`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.9.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:bd5262b0964a38e7e28de29632b03d507ba57fc832bb3171567478da841d9f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:2.9.9-windowsservercore-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:11e1ab562299ebbb64ab18c5afd891fa67655420780a109677a922340d8777d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2786352699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6dc041a550a2790319a7bb1f8b2b6bc818495c7300afc3226fc2da4d42219a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sun, 11 Dec 2022 08:04:49 GMT
RUN Install update 10.0.17763.3770
# Wed, 14 Dec 2022 01:29:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Dec 2022 02:37:16 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:37:17 GMT
ENV NATS_SERVER=2.9.9
# Wed, 14 Dec 2022 02:37:18 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.9/nats-server-v2.9.9-windows-amd64.zip
# Wed, 14 Dec 2022 02:37:19 GMT
ENV NATS_SERVER_SHASUM=a3456ed1a8f02d9d8ced35a1adbe1f6451af0c303f87ff74c15879dfc8cabd30
# Wed, 14 Dec 2022 02:38:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Dec 2022 02:41:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Dec 2022 02:41:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:20 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ad73ed772f80ab7923579a55dd12fb9b6e090d1d836408d16ffd9d3dee252`  
		Last Modified: Tue, 13 Dec 2022 23:56:47 GMT  
		Size: 856.4 MB (856427878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1d7d21a6f8359d8228f44b50aa9ad552783452100b6ce203e8f042415b5623`  
		Last Modified: Wed, 14 Dec 2022 02:14:22 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2b4fa0f968fba4be86c61da602c6d1d95bea2a5b257fa97e5cb498f7ddc7fe`  
		Last Modified: Wed, 14 Dec 2022 02:42:16 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1296500fbd02b72d68a4f8d4c78bb6c35ddaaa2c332cfe9254604281a913a00`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50931b0d887f06faade1d2051e8cceac2255778e1b4b9653fc75474db54b489d`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d625cf2ad988d5ac80b24112ef78da7fe7bddd4b5d188962fcb3ab90f04b57e`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f665d13d7cbc9a4ce6c8e5bc9120d5e3343377d7211f1e4d12480ddda591f522`  
		Last Modified: Wed, 14 Dec 2022 02:42:15 GMT  
		Size: 342.0 KB (342028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75307c50ea67f0603708dfc03956f1d610f261a5fa0f54d064b1690b0f866274`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 5.3 MB (5300085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1799e7de223a25ae30a351e317b449f128c31f00e818c0df0b02a4be360e4cf3`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 2.0 KB (1962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfeddb4c41b8d5fdc840c446ef490340728041b9202f2db80dce668c9d8d8ca5`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb917ab1b2406dc49a3fcc8fe92a27023ef822724a7c3056fa6f14ea3eca9d09`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2920025a2b586dcc5fa9b1580994f3bedbdbc128a7ab0a5c9bba8ca690025e0e`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:c0ffa1bed32d05eebcbc9892ecfa0c37ea9f1139ef480d1bc6c8c031a8d2a78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:4455732015639b8c2fa8e9020f3d17e8a209f9d59543292710768af952148382
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8581793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3b6d7d2a01e46a077c00066353ec8f59dd1f7812c8dd98a987f5250bbd6b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:34:51 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:34:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:34:54 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:34:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:34:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed86478665b1337795c7e912325131cdc2d168214502eed69e3723ff4a234d25`  
		Last Modified: Thu, 08 Dec 2022 20:36:07 GMT  
		Size: 5.2 MB (5210085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69220328c19fd2b50424c54dca1d8a7b058aa5a162eb5ac14521e35c4d62f1a`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79d3be31b99b819fb19f51849bff6e77c2b09db3e5da0d0ef4e094ed967ff8f`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3119056346819803bc76df59c2e831ff5171a8da1f002a4607e7e2abfbe6ecee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8082503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc75fd6f64f71d7f3e687447b6480cd6f9d57bd8a4ba7c2983d8861d4e3b51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:55:46 GMT
ADD file:132c76d7f7dae2f51f589ee460f1870a2cec6e9dc7ff8e38e88fcee2cfbe70da in / 
# Tue, 22 Nov 2022 22:55:46 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:59:56 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:59:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:59:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:00:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:00:00 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:00:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c2eb4db52fbe1266a78d8c185d33544a2916faa7d82fb5f50909fe233e0579da`  
		Last Modified: Tue, 22 Nov 2022 22:56:39 GMT  
		Size: 3.1 MB (3107138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f27e96bda80af22fdcbc14d587a8bd7f1785a53f6186c176c60cb5ee041552`  
		Last Modified: Thu, 08 Dec 2022 20:01:16 GMT  
		Size: 5.0 MB (4974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3bcb78d13a5f28e8655978e2d55ca50e33f3c13cd5c589ed9ff1af70a7316f`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495e1ec935b2a91f7057d7585b3674b8243a942618d53d46882d39f719432979`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:5831f8c5ef78543c5468a18f140d4437b908d992d4d902ede67b681ae1b9d368
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7831737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a580d362e6b152069cf3b30f5e629c7e3b964a990c4a7d15e5e5c33bf6f9610a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:57:20 GMT
ADD file:080010d9005e8e0dae3e98c7f9afff3e3a40ed32579ca01946efc6ede8316bad in / 
# Tue, 22 Nov 2022 22:57:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:30:58 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:31:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:31:02 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:31:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb2ec849933dd31db64abae3fdcb6923c490d9795577bee1ee1be04eab0376ee`  
		Last Modified: Tue, 22 Nov 2022 22:58:12 GMT  
		Size: 2.9 MB (2865346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671c89e40ba9d510918522256afe00ea4e39a695355982e9f361339ed50f7d08`  
		Last Modified: Thu, 08 Dec 2022 20:32:23 GMT  
		Size: 5.0 MB (4965424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de0969a38fcc2a8858b856efe0a63cd2745e3618c370383bea1f20db57e5e0c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6d0563d82f6dafe5dc45f3a674812a38a28ae6df2f7ac30a4d7664811a572c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d6a6c27b86493e468a184154633dfddf07e4fe466ad39c6b7eeaa4609e2ed0d2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8056469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3378f00ddf68731dab0ff2d503395918d1b20713f78c76e5e28bdf22fc29d78f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:56:52 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:56:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 19:56:55 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:56:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 19:56:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986444278dadde0d9a262ed4b893f80ad454eb35ffc857e42b5ad2f073465016`  
		Last Modified: Thu, 08 Dec 2022 19:57:44 GMT  
		Size: 4.8 MB (4796278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f5d8e79ec79a470e91e51e5aa1553566f49b677c12044d8e9b5c796e0ee27e`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4e306fd7736484456b60e0960d6d29025a49f82670bf70fad13a464afa6aec`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.17`

```console
$ docker pull nats@sha256:c0ffa1bed32d05eebcbc9892ecfa0c37ea9f1139ef480d1bc6c8c031a8d2a78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.17` - linux; amd64

```console
$ docker pull nats@sha256:4455732015639b8c2fa8e9020f3d17e8a209f9d59543292710768af952148382
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8581793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3b6d7d2a01e46a077c00066353ec8f59dd1f7812c8dd98a987f5250bbd6b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:34:51 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:34:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:34:54 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:34:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:34:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed86478665b1337795c7e912325131cdc2d168214502eed69e3723ff4a234d25`  
		Last Modified: Thu, 08 Dec 2022 20:36:07 GMT  
		Size: 5.2 MB (5210085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69220328c19fd2b50424c54dca1d8a7b058aa5a162eb5ac14521e35c4d62f1a`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79d3be31b99b819fb19f51849bff6e77c2b09db3e5da0d0ef4e094ed967ff8f`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.17` - linux; arm variant v6

```console
$ docker pull nats@sha256:3119056346819803bc76df59c2e831ff5171a8da1f002a4607e7e2abfbe6ecee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8082503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc75fd6f64f71d7f3e687447b6480cd6f9d57bd8a4ba7c2983d8861d4e3b51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:55:46 GMT
ADD file:132c76d7f7dae2f51f589ee460f1870a2cec6e9dc7ff8e38e88fcee2cfbe70da in / 
# Tue, 22 Nov 2022 22:55:46 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:59:56 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:59:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:59:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:00:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:00:00 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:00:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c2eb4db52fbe1266a78d8c185d33544a2916faa7d82fb5f50909fe233e0579da`  
		Last Modified: Tue, 22 Nov 2022 22:56:39 GMT  
		Size: 3.1 MB (3107138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f27e96bda80af22fdcbc14d587a8bd7f1785a53f6186c176c60cb5ee041552`  
		Last Modified: Thu, 08 Dec 2022 20:01:16 GMT  
		Size: 5.0 MB (4974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3bcb78d13a5f28e8655978e2d55ca50e33f3c13cd5c589ed9ff1af70a7316f`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495e1ec935b2a91f7057d7585b3674b8243a942618d53d46882d39f719432979`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.17` - linux; arm variant v7

```console
$ docker pull nats@sha256:5831f8c5ef78543c5468a18f140d4437b908d992d4d902ede67b681ae1b9d368
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7831737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a580d362e6b152069cf3b30f5e629c7e3b964a990c4a7d15e5e5c33bf6f9610a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:57:20 GMT
ADD file:080010d9005e8e0dae3e98c7f9afff3e3a40ed32579ca01946efc6ede8316bad in / 
# Tue, 22 Nov 2022 22:57:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:30:58 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:31:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:31:02 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:31:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb2ec849933dd31db64abae3fdcb6923c490d9795577bee1ee1be04eab0376ee`  
		Last Modified: Tue, 22 Nov 2022 22:58:12 GMT  
		Size: 2.9 MB (2865346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671c89e40ba9d510918522256afe00ea4e39a695355982e9f361339ed50f7d08`  
		Last Modified: Thu, 08 Dec 2022 20:32:23 GMT  
		Size: 5.0 MB (4965424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de0969a38fcc2a8858b856efe0a63cd2745e3618c370383bea1f20db57e5e0c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6d0563d82f6dafe5dc45f3a674812a38a28ae6df2f7ac30a4d7664811a572c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.17` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d6a6c27b86493e468a184154633dfddf07e4fe466ad39c6b7eeaa4609e2ed0d2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8056469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3378f00ddf68731dab0ff2d503395918d1b20713f78c76e5e28bdf22fc29d78f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:56:52 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:56:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 19:56:55 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:56:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 19:56:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986444278dadde0d9a262ed4b893f80ad454eb35ffc857e42b5ad2f073465016`  
		Last Modified: Thu, 08 Dec 2022 19:57:44 GMT  
		Size: 4.8 MB (4796278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f5d8e79ec79a470e91e51e5aa1553566f49b677c12044d8e9b5c796e0ee27e`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4e306fd7736484456b60e0960d6d29025a49f82670bf70fad13a464afa6aec`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:e4c75014ae278dcb8192c9718c7c0cebfb55cb76c41b285a1663141794ab96f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3770; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:79830eec98d1dc2f6acd4c63fee41a3434bc47a1b7f31cab9477de1bb3336100
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4922852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce49f767b1c3e8d858ddf7390fb3dad1b4fdebd12784b1fe33719a5a1a7993`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:d13bbefb978757216c59b4e4aba99770a0d4abdac594ab77282fb8cd6b85b588 in /nats-server 
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:35:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:35:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:35:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7692aeb9660d6587db50a4ea4f287699e633f61600a28a2d22092a82846129ce`  
		Last Modified: Thu, 08 Dec 2022 20:36:28 GMT  
		Size: 4.9 MB (4922345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022161875246986f560f72a1c52a359c684e6760487fe8f04a353168edfd2ac7`  
		Last Modified: Thu, 08 Dec 2022 20:36:27 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:24970d929b8d8ecf8887fb00bd92ce687fa3b252218c033614bbc892eec3c380
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4684937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac2c7d543ae2d436c8f9381f98b0bf06c08e5995d33fe8bdebd74699cfc1635`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:00:11 GMT
COPY file:5143a8dee5d00da934937a160852ff57e854ce11c42fdd4828e47d5bb4df42da in /nats-server 
# Thu, 08 Dec 2022 20:00:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:00:12 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:00:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:00:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fedc572ae49bd720399deeb6a36a9250630afd1a477e3c36b0afa73c9106ee50`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 4.7 MB (4684431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8cd5d76c140f074a437a1a67876d7ccd749d332dc6908ccb8fe301cd5dde0a`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:e0e6a65a6d9b16c6fc02bc5eb03804447975e81aab5cb4ef6de5ae0e7b490c54
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2439be95ff20e36b9fc19dd178f16c99ae8deb74465c167849bbff1ae4e66612`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:4c080655f46dbff5713191574af1df195a38d3dc3d3835f7eb875699a8e32d0b in /nats-server 
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:31:19 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:31:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:31:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221d437a3d6581cb4a83aada6c1cd3cb9d173cc07d5d0e9be2c801fb03fa9abe`  
		Last Modified: Thu, 08 Dec 2022 20:32:52 GMT  
		Size: 4.7 MB (4680919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5146fbe1772138448df3c1eb3444c5077d2cdac62bc7b082c112ac5ee4be14b2`  
		Last Modified: Thu, 08 Dec 2022 20:32:51 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:95318d8cd0e5ac24a3070af64056187f97cfb83673bb66a0fd5402f484912bc2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60599b58e21ba05f3bb06c0c373f7f8e213ea6861ad81399a4472fff4a90dbad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:5e130ace514500d49e7ad10785f48a1123d8992953cabcf51a55abf452f854f0 in /nats-server 
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 19:57:18 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:57:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 19:57:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 19:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8935bb735107ae5954afbbd1ce8b5d61ad9a102c82ba176ee5fcc00d437cc63`  
		Last Modified: Thu, 08 Dec 2022 19:58:05 GMT  
		Size: 4.5 MB (4506356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e3d737971cded626be61eca795945c4a04518d6c2dc737dbd7342cac026be`  
		Last Modified: Thu, 08 Dec 2022 19:58:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:e27c1884d9603539962cb28b7a22ad496237beba12bf95e9ed49fe9afa6c86d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111653587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0454f4ce065ac9703834be6c37eabe50eb3607ecae1d7cc7b344972885eb0b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Wed, 14 Dec 2022 02:41:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:41:39 GMT
RUN cmd /S /C #(nop) COPY file:8d03b51c4d2105411f3161f01ef7aad45804539a633733d4a8a5eb9f07e4970a in C:\nats-server.exe 
# Wed, 14 Dec 2022 02:41:40 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e9d361872b14736e9b1544993bd1f54f9284833fe47bff0ed4a51b726c47d8`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75304ecf4347969762a53760eff5f595b7ded2f4bd3ddf5b100cbfe792f5eda7`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 5.0 MB (4976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bacc71a9645bdd06d67819b123d5846ca66131f4d6d357ce3be7a9ba3679ffe`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6d4bc865209ef6542a200df7b975e08fcd6ebb627c4667fb6316854f0a6051`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340559bbbd7873ac427f77173287f004fa4a4fba5395aecaa30ed6923f7823e4`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076d6856ac201aebd4e95cd5f0b55a36849f89f8f43b44db4e80dd4d0b6c1f1`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:da6a053c9c9f52e84383f68483bc74cb3c7caafdd89ea93fe71d475193d0c530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:79830eec98d1dc2f6acd4c63fee41a3434bc47a1b7f31cab9477de1bb3336100
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4922852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce49f767b1c3e8d858ddf7390fb3dad1b4fdebd12784b1fe33719a5a1a7993`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:d13bbefb978757216c59b4e4aba99770a0d4abdac594ab77282fb8cd6b85b588 in /nats-server 
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:35:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:35:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:35:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7692aeb9660d6587db50a4ea4f287699e633f61600a28a2d22092a82846129ce`  
		Last Modified: Thu, 08 Dec 2022 20:36:28 GMT  
		Size: 4.9 MB (4922345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022161875246986f560f72a1c52a359c684e6760487fe8f04a353168edfd2ac7`  
		Last Modified: Thu, 08 Dec 2022 20:36:27 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:24970d929b8d8ecf8887fb00bd92ce687fa3b252218c033614bbc892eec3c380
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4684937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac2c7d543ae2d436c8f9381f98b0bf06c08e5995d33fe8bdebd74699cfc1635`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:00:11 GMT
COPY file:5143a8dee5d00da934937a160852ff57e854ce11c42fdd4828e47d5bb4df42da in /nats-server 
# Thu, 08 Dec 2022 20:00:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:00:12 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:00:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:00:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fedc572ae49bd720399deeb6a36a9250630afd1a477e3c36b0afa73c9106ee50`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 4.7 MB (4684431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8cd5d76c140f074a437a1a67876d7ccd749d332dc6908ccb8fe301cd5dde0a`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:e0e6a65a6d9b16c6fc02bc5eb03804447975e81aab5cb4ef6de5ae0e7b490c54
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2439be95ff20e36b9fc19dd178f16c99ae8deb74465c167849bbff1ae4e66612`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:4c080655f46dbff5713191574af1df195a38d3dc3d3835f7eb875699a8e32d0b in /nats-server 
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:31:19 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:31:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:31:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221d437a3d6581cb4a83aada6c1cd3cb9d173cc07d5d0e9be2c801fb03fa9abe`  
		Last Modified: Thu, 08 Dec 2022 20:32:52 GMT  
		Size: 4.7 MB (4680919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5146fbe1772138448df3c1eb3444c5077d2cdac62bc7b082c112ac5ee4be14b2`  
		Last Modified: Thu, 08 Dec 2022 20:32:51 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:95318d8cd0e5ac24a3070af64056187f97cfb83673bb66a0fd5402f484912bc2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60599b58e21ba05f3bb06c0c373f7f8e213ea6861ad81399a4472fff4a90dbad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:5e130ace514500d49e7ad10785f48a1123d8992953cabcf51a55abf452f854f0 in /nats-server 
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 19:57:18 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:57:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 19:57:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 19:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8935bb735107ae5954afbbd1ce8b5d61ad9a102c82ba176ee5fcc00d437cc63`  
		Last Modified: Thu, 08 Dec 2022 19:58:05 GMT  
		Size: 4.5 MB (4506356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e3d737971cded626be61eca795945c4a04518d6c2dc737dbd7342cac026be`  
		Last Modified: Thu, 08 Dec 2022 19:58:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:794c09f7a1b633fc92984035474e997ea88e32a22b4db214410f58a95e348a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:nanoserver` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:e27c1884d9603539962cb28b7a22ad496237beba12bf95e9ed49fe9afa6c86d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111653587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0454f4ce065ac9703834be6c37eabe50eb3607ecae1d7cc7b344972885eb0b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Wed, 14 Dec 2022 02:41:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:41:39 GMT
RUN cmd /S /C #(nop) COPY file:8d03b51c4d2105411f3161f01ef7aad45804539a633733d4a8a5eb9f07e4970a in C:\nats-server.exe 
# Wed, 14 Dec 2022 02:41:40 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e9d361872b14736e9b1544993bd1f54f9284833fe47bff0ed4a51b726c47d8`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75304ecf4347969762a53760eff5f595b7ded2f4bd3ddf5b100cbfe792f5eda7`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 5.0 MB (4976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bacc71a9645bdd06d67819b123d5846ca66131f4d6d357ce3be7a9ba3679ffe`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6d4bc865209ef6542a200df7b975e08fcd6ebb627c4667fb6316854f0a6051`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340559bbbd7873ac427f77173287f004fa4a4fba5395aecaa30ed6923f7823e4`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076d6856ac201aebd4e95cd5f0b55a36849f89f8f43b44db4e80dd4d0b6c1f1`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:794c09f7a1b633fc92984035474e997ea88e32a22b4db214410f58a95e348a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:e27c1884d9603539962cb28b7a22ad496237beba12bf95e9ed49fe9afa6c86d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111653587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0454f4ce065ac9703834be6c37eabe50eb3607ecae1d7cc7b344972885eb0b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Wed, 14 Dec 2022 02:41:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:41:39 GMT
RUN cmd /S /C #(nop) COPY file:8d03b51c4d2105411f3161f01ef7aad45804539a633733d4a8a5eb9f07e4970a in C:\nats-server.exe 
# Wed, 14 Dec 2022 02:41:40 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:42 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:43 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e9d361872b14736e9b1544993bd1f54f9284833fe47bff0ed4a51b726c47d8`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75304ecf4347969762a53760eff5f595b7ded2f4bd3ddf5b100cbfe792f5eda7`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 5.0 MB (4976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bacc71a9645bdd06d67819b123d5846ca66131f4d6d357ce3be7a9ba3679ffe`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6d4bc865209ef6542a200df7b975e08fcd6ebb627c4667fb6316854f0a6051`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340559bbbd7873ac427f77173287f004fa4a4fba5395aecaa30ed6923f7823e4`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076d6856ac201aebd4e95cd5f0b55a36849f89f8f43b44db4e80dd4d0b6c1f1`  
		Last Modified: Wed, 14 Dec 2022 02:42:29 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:da6a053c9c9f52e84383f68483bc74cb3c7caafdd89ea93fe71d475193d0c530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:79830eec98d1dc2f6acd4c63fee41a3434bc47a1b7f31cab9477de1bb3336100
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4922852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce49f767b1c3e8d858ddf7390fb3dad1b4fdebd12784b1fe33719a5a1a7993`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:d13bbefb978757216c59b4e4aba99770a0d4abdac594ab77282fb8cd6b85b588 in /nats-server 
# Thu, 08 Dec 2022 20:35:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:35:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:35:38 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:35:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7692aeb9660d6587db50a4ea4f287699e633f61600a28a2d22092a82846129ce`  
		Last Modified: Thu, 08 Dec 2022 20:36:28 GMT  
		Size: 4.9 MB (4922345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022161875246986f560f72a1c52a359c684e6760487fe8f04a353168edfd2ac7`  
		Last Modified: Thu, 08 Dec 2022 20:36:27 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:24970d929b8d8ecf8887fb00bd92ce687fa3b252218c033614bbc892eec3c380
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4684937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac2c7d543ae2d436c8f9381f98b0bf06c08e5995d33fe8bdebd74699cfc1635`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:00:11 GMT
COPY file:5143a8dee5d00da934937a160852ff57e854ce11c42fdd4828e47d5bb4df42da in /nats-server 
# Thu, 08 Dec 2022 20:00:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:00:12 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:00:12 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:00:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fedc572ae49bd720399deeb6a36a9250630afd1a477e3c36b0afa73c9106ee50`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 4.7 MB (4684431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8cd5d76c140f074a437a1a67876d7ccd749d332dc6908ccb8fe301cd5dde0a`  
		Last Modified: Thu, 08 Dec 2022 20:01:44 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:e0e6a65a6d9b16c6fc02bc5eb03804447975e81aab5cb4ef6de5ae0e7b490c54
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4681424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2439be95ff20e36b9fc19dd178f16c99ae8deb74465c167849bbff1ae4e66612`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:4c080655f46dbff5713191574af1df195a38d3dc3d3835f7eb875699a8e32d0b in /nats-server 
# Thu, 08 Dec 2022 20:31:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 20:31:19 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 20:31:19 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 20:31:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221d437a3d6581cb4a83aada6c1cd3cb9d173cc07d5d0e9be2c801fb03fa9abe`  
		Last Modified: Thu, 08 Dec 2022 20:32:52 GMT  
		Size: 4.7 MB (4680919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5146fbe1772138448df3c1eb3444c5077d2cdac62bc7b082c112ac5ee4be14b2`  
		Last Modified: Thu, 08 Dec 2022 20:32:51 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:95318d8cd0e5ac24a3070af64056187f97cfb83673bb66a0fd5402f484912bc2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60599b58e21ba05f3bb06c0c373f7f8e213ea6861ad81399a4472fff4a90dbad`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:5e130ace514500d49e7ad10785f48a1123d8992953cabcf51a55abf452f854f0 in /nats-server 
# Thu, 08 Dec 2022 19:57:18 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 08 Dec 2022 19:57:18 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:57:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 08 Dec 2022 19:57:18 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 08 Dec 2022 19:57:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8935bb735107ae5954afbbd1ce8b5d61ad9a102c82ba176ee5fcc00d437cc63`  
		Last Modified: Thu, 08 Dec 2022 19:58:05 GMT  
		Size: 4.5 MB (4506356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e3d737971cded626be61eca795945c4a04518d6c2dc737dbd7342cac026be`  
		Last Modified: Thu, 08 Dec 2022 19:58:04 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:bd5262b0964a38e7e28de29632b03d507ba57fc832bb3171567478da841d9f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:windowsservercore` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:11e1ab562299ebbb64ab18c5afd891fa67655420780a109677a922340d8777d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2786352699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6dc041a550a2790319a7bb1f8b2b6bc818495c7300afc3226fc2da4d42219a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sun, 11 Dec 2022 08:04:49 GMT
RUN Install update 10.0.17763.3770
# Wed, 14 Dec 2022 01:29:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Dec 2022 02:37:16 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:37:17 GMT
ENV NATS_SERVER=2.9.9
# Wed, 14 Dec 2022 02:37:18 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.9/nats-server-v2.9.9-windows-amd64.zip
# Wed, 14 Dec 2022 02:37:19 GMT
ENV NATS_SERVER_SHASUM=a3456ed1a8f02d9d8ced35a1adbe1f6451af0c303f87ff74c15879dfc8cabd30
# Wed, 14 Dec 2022 02:38:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Dec 2022 02:41:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Dec 2022 02:41:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:20 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ad73ed772f80ab7923579a55dd12fb9b6e090d1d836408d16ffd9d3dee252`  
		Last Modified: Tue, 13 Dec 2022 23:56:47 GMT  
		Size: 856.4 MB (856427878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1d7d21a6f8359d8228f44b50aa9ad552783452100b6ce203e8f042415b5623`  
		Last Modified: Wed, 14 Dec 2022 02:14:22 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2b4fa0f968fba4be86c61da602c6d1d95bea2a5b257fa97e5cb498f7ddc7fe`  
		Last Modified: Wed, 14 Dec 2022 02:42:16 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1296500fbd02b72d68a4f8d4c78bb6c35ddaaa2c332cfe9254604281a913a00`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50931b0d887f06faade1d2051e8cceac2255778e1b4b9653fc75474db54b489d`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d625cf2ad988d5ac80b24112ef78da7fe7bddd4b5d188962fcb3ab90f04b57e`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f665d13d7cbc9a4ce6c8e5bc9120d5e3343377d7211f1e4d12480ddda591f522`  
		Last Modified: Wed, 14 Dec 2022 02:42:15 GMT  
		Size: 342.0 KB (342028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75307c50ea67f0603708dfc03956f1d610f261a5fa0f54d064b1690b0f866274`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 5.3 MB (5300085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1799e7de223a25ae30a351e317b449f128c31f00e818c0df0b02a4be360e4cf3`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 2.0 KB (1962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfeddb4c41b8d5fdc840c446ef490340728041b9202f2db80dce668c9d8d8ca5`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb917ab1b2406dc49a3fcc8fe92a27023ef822724a7c3056fa6f14ea3eca9d09`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2920025a2b586dcc5fa9b1580994f3bedbdbc128a7ab0a5c9bba8ca690025e0e`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:bd5262b0964a38e7e28de29632b03d507ba57fc832bb3171567478da841d9f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:11e1ab562299ebbb64ab18c5afd891fa67655420780a109677a922340d8777d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2786352699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6dc041a550a2790319a7bb1f8b2b6bc818495c7300afc3226fc2da4d42219a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sun, 11 Dec 2022 08:04:49 GMT
RUN Install update 10.0.17763.3770
# Wed, 14 Dec 2022 01:29:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Dec 2022 02:37:16 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:37:17 GMT
ENV NATS_SERVER=2.9.9
# Wed, 14 Dec 2022 02:37:18 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.9/nats-server-v2.9.9-windows-amd64.zip
# Wed, 14 Dec 2022 02:37:19 GMT
ENV NATS_SERVER_SHASUM=a3456ed1a8f02d9d8ced35a1adbe1f6451af0c303f87ff74c15879dfc8cabd30
# Wed, 14 Dec 2022 02:38:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Dec 2022 02:41:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Dec 2022 02:41:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:20 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ad73ed772f80ab7923579a55dd12fb9b6e090d1d836408d16ffd9d3dee252`  
		Last Modified: Tue, 13 Dec 2022 23:56:47 GMT  
		Size: 856.4 MB (856427878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1d7d21a6f8359d8228f44b50aa9ad552783452100b6ce203e8f042415b5623`  
		Last Modified: Wed, 14 Dec 2022 02:14:22 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2b4fa0f968fba4be86c61da602c6d1d95bea2a5b257fa97e5cb498f7ddc7fe`  
		Last Modified: Wed, 14 Dec 2022 02:42:16 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1296500fbd02b72d68a4f8d4c78bb6c35ddaaa2c332cfe9254604281a913a00`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50931b0d887f06faade1d2051e8cceac2255778e1b4b9653fc75474db54b489d`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d625cf2ad988d5ac80b24112ef78da7fe7bddd4b5d188962fcb3ab90f04b57e`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f665d13d7cbc9a4ce6c8e5bc9120d5e3343377d7211f1e4d12480ddda591f522`  
		Last Modified: Wed, 14 Dec 2022 02:42:15 GMT  
		Size: 342.0 KB (342028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75307c50ea67f0603708dfc03956f1d610f261a5fa0f54d064b1690b0f866274`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 5.3 MB (5300085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1799e7de223a25ae30a351e317b449f128c31f00e818c0df0b02a4be360e4cf3`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 2.0 KB (1962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfeddb4c41b8d5fdc840c446ef490340728041b9202f2db80dce668c9d8d8ca5`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb917ab1b2406dc49a3fcc8fe92a27023ef822724a7c3056fa6f14ea3eca9d09`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2920025a2b586dcc5fa9b1580994f3bedbdbc128a7ab0a5c9bba8ca690025e0e`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
