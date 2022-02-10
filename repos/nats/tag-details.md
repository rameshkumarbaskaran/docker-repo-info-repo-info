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
-	[`nats:2.7.2`](#nats272)
-	[`nats:2.7.2-alpine`](#nats272-alpine)
-	[`nats:2.7.2-alpine3.15`](#nats272-alpine315)
-	[`nats:2.7.2-linux`](#nats272-linux)
-	[`nats:2.7.2-nanoserver`](#nats272-nanoserver)
-	[`nats:2.7.2-nanoserver-1809`](#nats272-nanoserver-1809)
-	[`nats:2.7.2-scratch`](#nats272-scratch)
-	[`nats:2.7.2-windowsservercore`](#nats272-windowsservercore)
-	[`nats:2.7.2-windowsservercore-1809`](#nats272-windowsservercore-1809)
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
$ docker pull nats@sha256:178f84bff4dab5a40bf69ba0a004b2a93b54aef07e24236bccd933fea56ed5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2565; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:7a1ab2e6e8274fa48286f74bdc4049613f4a195b106ad60b1c20d639a7d9e6eb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107616018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65a67e57e8400b4d29c0ad5699f7a280a95dfa3f515fcf965c4bacd3f16c3a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:51:18 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Wed, 09 Feb 2022 20:51:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580b72f9873a54f539c487aadc8937ae832cd2cffdd1af06f368629e058518ef`  
		Last Modified: Wed, 09 Feb 2022 20:52:11 GMT  
		Size: 4.5 MB (4522598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a10b192969d99c1eceb2713eeff85e1048113487b44dafa3d2012754fbdba`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e12c5402b38a673c9ae6c7de6d41c4f00a6c575f7e94336c5d9235c733efe2`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b17a4d20c99029a251a506f8c1b304cb89fbd352d8e4f0729834fae9e52cf3d`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adde8dc40298e7b0637e0543056d95dd5bb5ad4c8db8a6017be7b49527cfd58f`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:8b3fb2423a8cce4607ef30a990b35545afe0a3c613cd05b8eec7b483df268b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:89eb697c14f6556d6fb2703240e48d9600b40b408dda60ae36e262425a4431e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cd50aa7198f5c12f156d09daa0ddc1112236fff6860f120a2251d96ff9eb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 05:59:05 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 05:59:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 05:59:08 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 05:59:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802d7c7e4ac6a66227b2370fdcdf5a6a23823257ca471179abfd0902b956fd7`  
		Last Modified: Sat, 05 Feb 2022 06:00:25 GMT  
		Size: 4.8 MB (4753836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426dd83cc6600f256ef35338c32eaf3d0399bab79c1246ec09184bdd1ea5b1f`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93f969dc9e9707d1fb2f5eaf6e9636680ca5b3cdfe45b8466a97b0105f036ba`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:26c9fd5ce79bfefe188314878ab0f821a0fbca95fcfbe50f92e81d7f4484ec10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7052346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b52e6eb1b52cca05de6f415e6236b2bd399ce0fb9f1d1ce06066a1558de8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 00:57:59 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 00:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 00:58:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 00:58:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e778c855e77141dc3829b1882837f8ec9f4bc5a650dd40a2917a225e1c15d0d`  
		Last Modified: Sat, 05 Feb 2022 01:00:11 GMT  
		Size: 4.4 MB (4419922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8accecf8efa4c43a09a141647ccf09dc6a56558b970610993d7fdbee2275956f`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7dff5d8e4ec08b7521acbd3a01a86b9f803f821c99252b840a0491493b43b`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9f1dff6dca496cefa436b4db1fa8fa857eb557bd0a6e6760c9b296f096bde9e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6847919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc4a088149c39457ad06caa0dedec762d0dcf09f2ae4743592c4d418f8e890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 06:12:22 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 06:12:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 06:12:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 06:12:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 06:12:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 06:12:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603aa49db7f9a89152dcd7cdf78b402ef16aff3bb40294f6c66a933f07378ee0`  
		Last Modified: Sat, 05 Feb 2022 06:14:40 GMT  
		Size: 4.4 MB (4412155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ab40c3eba476ac4d53154b86201d8626e858e7ed7651fc1045021e03587fee`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ec7b9832ec0d741d78be9c59991717e8a0a7b188c6ac0252cee24c879dcfcf`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b23b110a6166fdd559bbdf992cff078caa3eeb7e37fa86d2cf2765bdddd7898
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c3ca4ead676b4547ea7e17b1a67ffc43fc9e9a70f9fbbc6dfbe03a6615799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 04:08:44 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 04:08:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 04:08:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 04:08:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 04:08:50 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 04:08:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e8b74114ddf2278e01658eb7e01be08056565bae8a2955645300b982fb0f2`  
		Last Modified: Sat, 05 Feb 2022 04:09:53 GMT  
		Size: 4.4 MB (4398315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76361110853d49e5895bb2123f92f8e3f8f1a08ce01c8ccda76acb70a73d7e22`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a80240856cec2d4b5bcd8aaff898e547e4b7572d85156a941620aaf5d1b432`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.15`

```console
$ docker pull nats@sha256:8b3fb2423a8cce4607ef30a990b35545afe0a3c613cd05b8eec7b483df268b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:89eb697c14f6556d6fb2703240e48d9600b40b408dda60ae36e262425a4431e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cd50aa7198f5c12f156d09daa0ddc1112236fff6860f120a2251d96ff9eb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 05:59:05 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 05:59:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 05:59:08 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 05:59:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802d7c7e4ac6a66227b2370fdcdf5a6a23823257ca471179abfd0902b956fd7`  
		Last Modified: Sat, 05 Feb 2022 06:00:25 GMT  
		Size: 4.8 MB (4753836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426dd83cc6600f256ef35338c32eaf3d0399bab79c1246ec09184bdd1ea5b1f`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93f969dc9e9707d1fb2f5eaf6e9636680ca5b3cdfe45b8466a97b0105f036ba`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:26c9fd5ce79bfefe188314878ab0f821a0fbca95fcfbe50f92e81d7f4484ec10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7052346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b52e6eb1b52cca05de6f415e6236b2bd399ce0fb9f1d1ce06066a1558de8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 00:57:59 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 00:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 00:58:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 00:58:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e778c855e77141dc3829b1882837f8ec9f4bc5a650dd40a2917a225e1c15d0d`  
		Last Modified: Sat, 05 Feb 2022 01:00:11 GMT  
		Size: 4.4 MB (4419922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8accecf8efa4c43a09a141647ccf09dc6a56558b970610993d7fdbee2275956f`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7dff5d8e4ec08b7521acbd3a01a86b9f803f821c99252b840a0491493b43b`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:9f1dff6dca496cefa436b4db1fa8fa857eb557bd0a6e6760c9b296f096bde9e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6847919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc4a088149c39457ad06caa0dedec762d0dcf09f2ae4743592c4d418f8e890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 06:12:22 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 06:12:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 06:12:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 06:12:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 06:12:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 06:12:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603aa49db7f9a89152dcd7cdf78b402ef16aff3bb40294f6c66a933f07378ee0`  
		Last Modified: Sat, 05 Feb 2022 06:14:40 GMT  
		Size: 4.4 MB (4412155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ab40c3eba476ac4d53154b86201d8626e858e7ed7651fc1045021e03587fee`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ec7b9832ec0d741d78be9c59991717e8a0a7b188c6ac0252cee24c879dcfcf`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b23b110a6166fdd559bbdf992cff078caa3eeb7e37fa86d2cf2765bdddd7898
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c3ca4ead676b4547ea7e17b1a67ffc43fc9e9a70f9fbbc6dfbe03a6615799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 04:08:44 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 04:08:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 04:08:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 04:08:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 04:08:50 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 04:08:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e8b74114ddf2278e01658eb7e01be08056565bae8a2955645300b982fb0f2`  
		Last Modified: Sat, 05 Feb 2022 04:09:53 GMT  
		Size: 4.4 MB (4398315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76361110853d49e5895bb2123f92f8e3f8f1a08ce01c8ccda76acb70a73d7e22`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a80240856cec2d4b5bcd8aaff898e547e4b7572d85156a941620aaf5d1b432`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:7d5e0768fec0607c8aca58d0f15fa00ca535c5abffaef46aaf4196657521a605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:586fed106de60d6bebea6665796e0c0f4b44125970b5fd123f558dac8c964dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:7a1ab2e6e8274fa48286f74bdc4049613f4a195b106ad60b1c20d639a7d9e6eb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107616018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65a67e57e8400b4d29c0ad5699f7a280a95dfa3f515fcf965c4bacd3f16c3a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:51:18 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Wed, 09 Feb 2022 20:51:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580b72f9873a54f539c487aadc8937ae832cd2cffdd1af06f368629e058518ef`  
		Last Modified: Wed, 09 Feb 2022 20:52:11 GMT  
		Size: 4.5 MB (4522598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a10b192969d99c1eceb2713eeff85e1048113487b44dafa3d2012754fbdba`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e12c5402b38a673c9ae6c7de6d41c4f00a6c575f7e94336c5d9235c733efe2`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b17a4d20c99029a251a506f8c1b304cb89fbd352d8e4f0729834fae9e52cf3d`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adde8dc40298e7b0637e0543056d95dd5bb5ad4c8db8a6017be7b49527cfd58f`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:586fed106de60d6bebea6665796e0c0f4b44125970b5fd123f558dac8c964dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:7a1ab2e6e8274fa48286f74bdc4049613f4a195b106ad60b1c20d639a7d9e6eb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107616018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65a67e57e8400b4d29c0ad5699f7a280a95dfa3f515fcf965c4bacd3f16c3a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:51:18 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Wed, 09 Feb 2022 20:51:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580b72f9873a54f539c487aadc8937ae832cd2cffdd1af06f368629e058518ef`  
		Last Modified: Wed, 09 Feb 2022 20:52:11 GMT  
		Size: 4.5 MB (4522598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a10b192969d99c1eceb2713eeff85e1048113487b44dafa3d2012754fbdba`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e12c5402b38a673c9ae6c7de6d41c4f00a6c575f7e94336c5d9235c733efe2`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b17a4d20c99029a251a506f8c1b304cb89fbd352d8e4f0729834fae9e52cf3d`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adde8dc40298e7b0637e0543056d95dd5bb5ad4c8db8a6017be7b49527cfd58f`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:7d5e0768fec0607c8aca58d0f15fa00ca535c5abffaef46aaf4196657521a605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:33946d4adb965632134b6c514f7e588e27df9e4f7d4e3b555d31c28496fd2181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:2f206c7404528b4d1b631e8747726f7f32fa0519169bc201b32fc2b826d89a1f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718958093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8800eccde299346c51025ba23593daa22a824125479a0501431412ee4934a6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 15:04:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Feb 2022 18:10:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:48:50 GMT
ENV NATS_SERVER=2.7.2
# Wed, 09 Feb 2022 20:48:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Wed, 09 Feb 2022 20:48:52 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Wed, 09 Feb 2022 20:49:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Feb 2022 20:51:00 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Feb 2022 20:51:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:02 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f49d3791198cf2ea875fd54ce3bb715670742d4a58c00252395ad1b74036662a`  
		Last Modified: Wed, 09 Feb 2022 16:39:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4235aeeb4e8b577cc7aa26c7994ec94c94dd53a38764fc510b330b77cef4abad`  
		Last Modified: Wed, 09 Feb 2022 18:14:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5624de3564dcef1325bc61eea92cfcb7dbc1c7b35b0023cd17b2f17c38e6df9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3f050ab2ed35215f1fa3bd806046f502f70d7e85d3f070bdd6fd744864cf9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58550f980b41b606662c4c2d767cca700cbd91b7ec3445c99c5044ca946d586b`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5343d460a59e635dddf02a131dadf49fd2316ad0fef64a08af5e30a3cba30cb5`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 364.5 KB (364524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd6e130904f62e22c3a23ea8b080883ee9bbb534b2db618e0a38cab2766151e`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 4.9 MB (4865553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac13c2b0fa7ddd6703c6c46640b9752b4b5be3aac511ccf5af6c20188a55152`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff779110ef51e3be2fae7dc9e966b4392f3dc10973c23dc689c8c5e78e35494`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9efdff7b3152cb65b604c10ab9822a72e900481f5815179012a1c7a945f9567`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb94adbb9b65f8ab12036ec18b5b9903bb67aa43ed6e10f680078e35eb76c4fe`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:33946d4adb965632134b6c514f7e588e27df9e4f7d4e3b555d31c28496fd2181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:2f206c7404528b4d1b631e8747726f7f32fa0519169bc201b32fc2b826d89a1f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718958093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8800eccde299346c51025ba23593daa22a824125479a0501431412ee4934a6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 15:04:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Feb 2022 18:10:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:48:50 GMT
ENV NATS_SERVER=2.7.2
# Wed, 09 Feb 2022 20:48:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Wed, 09 Feb 2022 20:48:52 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Wed, 09 Feb 2022 20:49:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Feb 2022 20:51:00 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Feb 2022 20:51:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:02 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f49d3791198cf2ea875fd54ce3bb715670742d4a58c00252395ad1b74036662a`  
		Last Modified: Wed, 09 Feb 2022 16:39:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4235aeeb4e8b577cc7aa26c7994ec94c94dd53a38764fc510b330b77cef4abad`  
		Last Modified: Wed, 09 Feb 2022 18:14:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5624de3564dcef1325bc61eea92cfcb7dbc1c7b35b0023cd17b2f17c38e6df9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3f050ab2ed35215f1fa3bd806046f502f70d7e85d3f070bdd6fd744864cf9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58550f980b41b606662c4c2d767cca700cbd91b7ec3445c99c5044ca946d586b`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5343d460a59e635dddf02a131dadf49fd2316ad0fef64a08af5e30a3cba30cb5`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 364.5 KB (364524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd6e130904f62e22c3a23ea8b080883ee9bbb534b2db618e0a38cab2766151e`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 4.9 MB (4865553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac13c2b0fa7ddd6703c6c46640b9752b4b5be3aac511ccf5af6c20188a55152`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff779110ef51e3be2fae7dc9e966b4392f3dc10973c23dc689c8c5e78e35494`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9efdff7b3152cb65b604c10ab9822a72e900481f5815179012a1c7a945f9567`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb94adbb9b65f8ab12036ec18b5b9903bb67aa43ed6e10f680078e35eb76c4fe`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7`

```console
$ docker pull nats@sha256:178f84bff4dab5a40bf69ba0a004b2a93b54aef07e24236bccd933fea56ed5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2565; amd64

### `nats:2.7` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:7a1ab2e6e8274fa48286f74bdc4049613f4a195b106ad60b1c20d639a7d9e6eb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107616018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65a67e57e8400b4d29c0ad5699f7a280a95dfa3f515fcf965c4bacd3f16c3a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:51:18 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Wed, 09 Feb 2022 20:51:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580b72f9873a54f539c487aadc8937ae832cd2cffdd1af06f368629e058518ef`  
		Last Modified: Wed, 09 Feb 2022 20:52:11 GMT  
		Size: 4.5 MB (4522598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a10b192969d99c1eceb2713eeff85e1048113487b44dafa3d2012754fbdba`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e12c5402b38a673c9ae6c7de6d41c4f00a6c575f7e94336c5d9235c733efe2`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b17a4d20c99029a251a506f8c1b304cb89fbd352d8e4f0729834fae9e52cf3d`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adde8dc40298e7b0637e0543056d95dd5bb5ad4c8db8a6017be7b49527cfd58f`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-alpine`

```console
$ docker pull nats@sha256:8b3fb2423a8cce4607ef30a990b35545afe0a3c613cd05b8eec7b483df268b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-alpine` - linux; amd64

```console
$ docker pull nats@sha256:89eb697c14f6556d6fb2703240e48d9600b40b408dda60ae36e262425a4431e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cd50aa7198f5c12f156d09daa0ddc1112236fff6860f120a2251d96ff9eb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 05:59:05 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 05:59:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 05:59:08 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 05:59:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802d7c7e4ac6a66227b2370fdcdf5a6a23823257ca471179abfd0902b956fd7`  
		Last Modified: Sat, 05 Feb 2022 06:00:25 GMT  
		Size: 4.8 MB (4753836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426dd83cc6600f256ef35338c32eaf3d0399bab79c1246ec09184bdd1ea5b1f`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93f969dc9e9707d1fb2f5eaf6e9636680ca5b3cdfe45b8466a97b0105f036ba`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:26c9fd5ce79bfefe188314878ab0f821a0fbca95fcfbe50f92e81d7f4484ec10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7052346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b52e6eb1b52cca05de6f415e6236b2bd399ce0fb9f1d1ce06066a1558de8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 00:57:59 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 00:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 00:58:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 00:58:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e778c855e77141dc3829b1882837f8ec9f4bc5a650dd40a2917a225e1c15d0d`  
		Last Modified: Sat, 05 Feb 2022 01:00:11 GMT  
		Size: 4.4 MB (4419922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8accecf8efa4c43a09a141647ccf09dc6a56558b970610993d7fdbee2275956f`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7dff5d8e4ec08b7521acbd3a01a86b9f803f821c99252b840a0491493b43b`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9f1dff6dca496cefa436b4db1fa8fa857eb557bd0a6e6760c9b296f096bde9e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6847919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc4a088149c39457ad06caa0dedec762d0dcf09f2ae4743592c4d418f8e890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 06:12:22 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 06:12:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 06:12:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 06:12:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 06:12:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 06:12:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603aa49db7f9a89152dcd7cdf78b402ef16aff3bb40294f6c66a933f07378ee0`  
		Last Modified: Sat, 05 Feb 2022 06:14:40 GMT  
		Size: 4.4 MB (4412155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ab40c3eba476ac4d53154b86201d8626e858e7ed7651fc1045021e03587fee`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ec7b9832ec0d741d78be9c59991717e8a0a7b188c6ac0252cee24c879dcfcf`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b23b110a6166fdd559bbdf992cff078caa3eeb7e37fa86d2cf2765bdddd7898
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c3ca4ead676b4547ea7e17b1a67ffc43fc9e9a70f9fbbc6dfbe03a6615799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 04:08:44 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 04:08:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 04:08:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 04:08:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 04:08:50 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 04:08:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e8b74114ddf2278e01658eb7e01be08056565bae8a2955645300b982fb0f2`  
		Last Modified: Sat, 05 Feb 2022 04:09:53 GMT  
		Size: 4.4 MB (4398315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76361110853d49e5895bb2123f92f8e3f8f1a08ce01c8ccda76acb70a73d7e22`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a80240856cec2d4b5bcd8aaff898e547e4b7572d85156a941620aaf5d1b432`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-alpine3.15`

```console
$ docker pull nats@sha256:8b3fb2423a8cce4607ef30a990b35545afe0a3c613cd05b8eec7b483df268b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:89eb697c14f6556d6fb2703240e48d9600b40b408dda60ae36e262425a4431e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cd50aa7198f5c12f156d09daa0ddc1112236fff6860f120a2251d96ff9eb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 05:59:05 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 05:59:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 05:59:08 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 05:59:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802d7c7e4ac6a66227b2370fdcdf5a6a23823257ca471179abfd0902b956fd7`  
		Last Modified: Sat, 05 Feb 2022 06:00:25 GMT  
		Size: 4.8 MB (4753836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426dd83cc6600f256ef35338c32eaf3d0399bab79c1246ec09184bdd1ea5b1f`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93f969dc9e9707d1fb2f5eaf6e9636680ca5b3cdfe45b8466a97b0105f036ba`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:26c9fd5ce79bfefe188314878ab0f821a0fbca95fcfbe50f92e81d7f4484ec10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7052346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b52e6eb1b52cca05de6f415e6236b2bd399ce0fb9f1d1ce06066a1558de8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 00:57:59 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 00:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 00:58:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 00:58:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e778c855e77141dc3829b1882837f8ec9f4bc5a650dd40a2917a225e1c15d0d`  
		Last Modified: Sat, 05 Feb 2022 01:00:11 GMT  
		Size: 4.4 MB (4419922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8accecf8efa4c43a09a141647ccf09dc6a56558b970610993d7fdbee2275956f`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7dff5d8e4ec08b7521acbd3a01a86b9f803f821c99252b840a0491493b43b`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:9f1dff6dca496cefa436b4db1fa8fa857eb557bd0a6e6760c9b296f096bde9e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6847919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc4a088149c39457ad06caa0dedec762d0dcf09f2ae4743592c4d418f8e890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 06:12:22 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 06:12:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 06:12:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 06:12:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 06:12:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 06:12:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603aa49db7f9a89152dcd7cdf78b402ef16aff3bb40294f6c66a933f07378ee0`  
		Last Modified: Sat, 05 Feb 2022 06:14:40 GMT  
		Size: 4.4 MB (4412155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ab40c3eba476ac4d53154b86201d8626e858e7ed7651fc1045021e03587fee`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ec7b9832ec0d741d78be9c59991717e8a0a7b188c6ac0252cee24c879dcfcf`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b23b110a6166fdd559bbdf992cff078caa3eeb7e37fa86d2cf2765bdddd7898
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c3ca4ead676b4547ea7e17b1a67ffc43fc9e9a70f9fbbc6dfbe03a6615799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 04:08:44 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 04:08:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 04:08:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 04:08:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 04:08:50 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 04:08:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e8b74114ddf2278e01658eb7e01be08056565bae8a2955645300b982fb0f2`  
		Last Modified: Sat, 05 Feb 2022 04:09:53 GMT  
		Size: 4.4 MB (4398315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76361110853d49e5895bb2123f92f8e3f8f1a08ce01c8ccda76acb70a73d7e22`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a80240856cec2d4b5bcd8aaff898e547e4b7572d85156a941620aaf5d1b432`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-linux`

```console
$ docker pull nats@sha256:7d5e0768fec0607c8aca58d0f15fa00ca535c5abffaef46aaf4196657521a605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-linux` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-nanoserver`

```console
$ docker pull nats@sha256:586fed106de60d6bebea6665796e0c0f4b44125970b5fd123f558dac8c964dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats:2.7-nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:7a1ab2e6e8274fa48286f74bdc4049613f4a195b106ad60b1c20d639a7d9e6eb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107616018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65a67e57e8400b4d29c0ad5699f7a280a95dfa3f515fcf965c4bacd3f16c3a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:51:18 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Wed, 09 Feb 2022 20:51:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580b72f9873a54f539c487aadc8937ae832cd2cffdd1af06f368629e058518ef`  
		Last Modified: Wed, 09 Feb 2022 20:52:11 GMT  
		Size: 4.5 MB (4522598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a10b192969d99c1eceb2713eeff85e1048113487b44dafa3d2012754fbdba`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e12c5402b38a673c9ae6c7de6d41c4f00a6c575f7e94336c5d9235c733efe2`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b17a4d20c99029a251a506f8c1b304cb89fbd352d8e4f0729834fae9e52cf3d`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adde8dc40298e7b0637e0543056d95dd5bb5ad4c8db8a6017be7b49527cfd58f`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-nanoserver-1809`

```console
$ docker pull nats@sha256:586fed106de60d6bebea6665796e0c0f4b44125970b5fd123f558dac8c964dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats:2.7-nanoserver-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:7a1ab2e6e8274fa48286f74bdc4049613f4a195b106ad60b1c20d639a7d9e6eb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107616018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65a67e57e8400b4d29c0ad5699f7a280a95dfa3f515fcf965c4bacd3f16c3a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:51:18 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Wed, 09 Feb 2022 20:51:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580b72f9873a54f539c487aadc8937ae832cd2cffdd1af06f368629e058518ef`  
		Last Modified: Wed, 09 Feb 2022 20:52:11 GMT  
		Size: 4.5 MB (4522598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a10b192969d99c1eceb2713eeff85e1048113487b44dafa3d2012754fbdba`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e12c5402b38a673c9ae6c7de6d41c4f00a6c575f7e94336c5d9235c733efe2`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b17a4d20c99029a251a506f8c1b304cb89fbd352d8e4f0729834fae9e52cf3d`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adde8dc40298e7b0637e0543056d95dd5bb5ad4c8db8a6017be7b49527cfd58f`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-scratch`

```console
$ docker pull nats@sha256:7d5e0768fec0607c8aca58d0f15fa00ca535c5abffaef46aaf4196657521a605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7-scratch` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-windowsservercore`

```console
$ docker pull nats@sha256:33946d4adb965632134b6c514f7e588e27df9e4f7d4e3b555d31c28496fd2181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats:2.7-windowsservercore` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:2f206c7404528b4d1b631e8747726f7f32fa0519169bc201b32fc2b826d89a1f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718958093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8800eccde299346c51025ba23593daa22a824125479a0501431412ee4934a6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 15:04:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Feb 2022 18:10:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:48:50 GMT
ENV NATS_SERVER=2.7.2
# Wed, 09 Feb 2022 20:48:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Wed, 09 Feb 2022 20:48:52 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Wed, 09 Feb 2022 20:49:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Feb 2022 20:51:00 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Feb 2022 20:51:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:02 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f49d3791198cf2ea875fd54ce3bb715670742d4a58c00252395ad1b74036662a`  
		Last Modified: Wed, 09 Feb 2022 16:39:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4235aeeb4e8b577cc7aa26c7994ec94c94dd53a38764fc510b330b77cef4abad`  
		Last Modified: Wed, 09 Feb 2022 18:14:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5624de3564dcef1325bc61eea92cfcb7dbc1c7b35b0023cd17b2f17c38e6df9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3f050ab2ed35215f1fa3bd806046f502f70d7e85d3f070bdd6fd744864cf9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58550f980b41b606662c4c2d767cca700cbd91b7ec3445c99c5044ca946d586b`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5343d460a59e635dddf02a131dadf49fd2316ad0fef64a08af5e30a3cba30cb5`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 364.5 KB (364524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd6e130904f62e22c3a23ea8b080883ee9bbb534b2db618e0a38cab2766151e`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 4.9 MB (4865553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac13c2b0fa7ddd6703c6c46640b9752b4b5be3aac511ccf5af6c20188a55152`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff779110ef51e3be2fae7dc9e966b4392f3dc10973c23dc689c8c5e78e35494`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9efdff7b3152cb65b604c10ab9822a72e900481f5815179012a1c7a945f9567`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb94adbb9b65f8ab12036ec18b5b9903bb67aa43ed6e10f680078e35eb76c4fe`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7-windowsservercore-1809`

```console
$ docker pull nats@sha256:33946d4adb965632134b6c514f7e588e27df9e4f7d4e3b555d31c28496fd2181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats:2.7-windowsservercore-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:2f206c7404528b4d1b631e8747726f7f32fa0519169bc201b32fc2b826d89a1f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718958093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8800eccde299346c51025ba23593daa22a824125479a0501431412ee4934a6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 15:04:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Feb 2022 18:10:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:48:50 GMT
ENV NATS_SERVER=2.7.2
# Wed, 09 Feb 2022 20:48:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Wed, 09 Feb 2022 20:48:52 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Wed, 09 Feb 2022 20:49:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Feb 2022 20:51:00 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Feb 2022 20:51:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:02 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f49d3791198cf2ea875fd54ce3bb715670742d4a58c00252395ad1b74036662a`  
		Last Modified: Wed, 09 Feb 2022 16:39:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4235aeeb4e8b577cc7aa26c7994ec94c94dd53a38764fc510b330b77cef4abad`  
		Last Modified: Wed, 09 Feb 2022 18:14:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5624de3564dcef1325bc61eea92cfcb7dbc1c7b35b0023cd17b2f17c38e6df9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3f050ab2ed35215f1fa3bd806046f502f70d7e85d3f070bdd6fd744864cf9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58550f980b41b606662c4c2d767cca700cbd91b7ec3445c99c5044ca946d586b`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5343d460a59e635dddf02a131dadf49fd2316ad0fef64a08af5e30a3cba30cb5`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 364.5 KB (364524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd6e130904f62e22c3a23ea8b080883ee9bbb534b2db618e0a38cab2766151e`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 4.9 MB (4865553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac13c2b0fa7ddd6703c6c46640b9752b4b5be3aac511ccf5af6c20188a55152`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff779110ef51e3be2fae7dc9e966b4392f3dc10973c23dc689c8c5e78e35494`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9efdff7b3152cb65b604c10ab9822a72e900481f5815179012a1c7a945f9567`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb94adbb9b65f8ab12036ec18b5b9903bb67aa43ed6e10f680078e35eb76c4fe`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2`

```console
$ docker pull nats@sha256:178f84bff4dab5a40bf69ba0a004b2a93b54aef07e24236bccd933fea56ed5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2565; amd64

### `nats:2.7.2` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:7a1ab2e6e8274fa48286f74bdc4049613f4a195b106ad60b1c20d639a7d9e6eb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107616018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65a67e57e8400b4d29c0ad5699f7a280a95dfa3f515fcf965c4bacd3f16c3a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:51:18 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Wed, 09 Feb 2022 20:51:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580b72f9873a54f539c487aadc8937ae832cd2cffdd1af06f368629e058518ef`  
		Last Modified: Wed, 09 Feb 2022 20:52:11 GMT  
		Size: 4.5 MB (4522598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a10b192969d99c1eceb2713eeff85e1048113487b44dafa3d2012754fbdba`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e12c5402b38a673c9ae6c7de6d41c4f00a6c575f7e94336c5d9235c733efe2`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b17a4d20c99029a251a506f8c1b304cb89fbd352d8e4f0729834fae9e52cf3d`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adde8dc40298e7b0637e0543056d95dd5bb5ad4c8db8a6017be7b49527cfd58f`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2-alpine`

```console
$ docker pull nats@sha256:8b3fb2423a8cce4607ef30a990b35545afe0a3c613cd05b8eec7b483df268b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:89eb697c14f6556d6fb2703240e48d9600b40b408dda60ae36e262425a4431e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cd50aa7198f5c12f156d09daa0ddc1112236fff6860f120a2251d96ff9eb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 05:59:05 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 05:59:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 05:59:08 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 05:59:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802d7c7e4ac6a66227b2370fdcdf5a6a23823257ca471179abfd0902b956fd7`  
		Last Modified: Sat, 05 Feb 2022 06:00:25 GMT  
		Size: 4.8 MB (4753836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426dd83cc6600f256ef35338c32eaf3d0399bab79c1246ec09184bdd1ea5b1f`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93f969dc9e9707d1fb2f5eaf6e9636680ca5b3cdfe45b8466a97b0105f036ba`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:26c9fd5ce79bfefe188314878ab0f821a0fbca95fcfbe50f92e81d7f4484ec10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7052346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b52e6eb1b52cca05de6f415e6236b2bd399ce0fb9f1d1ce06066a1558de8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 00:57:59 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 00:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 00:58:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 00:58:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e778c855e77141dc3829b1882837f8ec9f4bc5a650dd40a2917a225e1c15d0d`  
		Last Modified: Sat, 05 Feb 2022 01:00:11 GMT  
		Size: 4.4 MB (4419922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8accecf8efa4c43a09a141647ccf09dc6a56558b970610993d7fdbee2275956f`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7dff5d8e4ec08b7521acbd3a01a86b9f803f821c99252b840a0491493b43b`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9f1dff6dca496cefa436b4db1fa8fa857eb557bd0a6e6760c9b296f096bde9e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6847919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc4a088149c39457ad06caa0dedec762d0dcf09f2ae4743592c4d418f8e890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 06:12:22 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 06:12:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 06:12:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 06:12:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 06:12:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 06:12:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603aa49db7f9a89152dcd7cdf78b402ef16aff3bb40294f6c66a933f07378ee0`  
		Last Modified: Sat, 05 Feb 2022 06:14:40 GMT  
		Size: 4.4 MB (4412155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ab40c3eba476ac4d53154b86201d8626e858e7ed7651fc1045021e03587fee`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ec7b9832ec0d741d78be9c59991717e8a0a7b188c6ac0252cee24c879dcfcf`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b23b110a6166fdd559bbdf992cff078caa3eeb7e37fa86d2cf2765bdddd7898
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c3ca4ead676b4547ea7e17b1a67ffc43fc9e9a70f9fbbc6dfbe03a6615799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 04:08:44 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 04:08:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 04:08:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 04:08:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 04:08:50 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 04:08:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e8b74114ddf2278e01658eb7e01be08056565bae8a2955645300b982fb0f2`  
		Last Modified: Sat, 05 Feb 2022 04:09:53 GMT  
		Size: 4.4 MB (4398315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76361110853d49e5895bb2123f92f8e3f8f1a08ce01c8ccda76acb70a73d7e22`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a80240856cec2d4b5bcd8aaff898e547e4b7572d85156a941620aaf5d1b432`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2-alpine3.15`

```console
$ docker pull nats@sha256:8b3fb2423a8cce4607ef30a990b35545afe0a3c613cd05b8eec7b483df268b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.2-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:89eb697c14f6556d6fb2703240e48d9600b40b408dda60ae36e262425a4431e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cd50aa7198f5c12f156d09daa0ddc1112236fff6860f120a2251d96ff9eb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 05:59:05 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 05:59:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 05:59:08 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 05:59:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802d7c7e4ac6a66227b2370fdcdf5a6a23823257ca471179abfd0902b956fd7`  
		Last Modified: Sat, 05 Feb 2022 06:00:25 GMT  
		Size: 4.8 MB (4753836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426dd83cc6600f256ef35338c32eaf3d0399bab79c1246ec09184bdd1ea5b1f`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93f969dc9e9707d1fb2f5eaf6e9636680ca5b3cdfe45b8466a97b0105f036ba`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:26c9fd5ce79bfefe188314878ab0f821a0fbca95fcfbe50f92e81d7f4484ec10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7052346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b52e6eb1b52cca05de6f415e6236b2bd399ce0fb9f1d1ce06066a1558de8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 00:57:59 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 00:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 00:58:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 00:58:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e778c855e77141dc3829b1882837f8ec9f4bc5a650dd40a2917a225e1c15d0d`  
		Last Modified: Sat, 05 Feb 2022 01:00:11 GMT  
		Size: 4.4 MB (4419922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8accecf8efa4c43a09a141647ccf09dc6a56558b970610993d7fdbee2275956f`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7dff5d8e4ec08b7521acbd3a01a86b9f803f821c99252b840a0491493b43b`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:9f1dff6dca496cefa436b4db1fa8fa857eb557bd0a6e6760c9b296f096bde9e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6847919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc4a088149c39457ad06caa0dedec762d0dcf09f2ae4743592c4d418f8e890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 06:12:22 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 06:12:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 06:12:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 06:12:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 06:12:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 06:12:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603aa49db7f9a89152dcd7cdf78b402ef16aff3bb40294f6c66a933f07378ee0`  
		Last Modified: Sat, 05 Feb 2022 06:14:40 GMT  
		Size: 4.4 MB (4412155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ab40c3eba476ac4d53154b86201d8626e858e7ed7651fc1045021e03587fee`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ec7b9832ec0d741d78be9c59991717e8a0a7b188c6ac0252cee24c879dcfcf`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b23b110a6166fdd559bbdf992cff078caa3eeb7e37fa86d2cf2765bdddd7898
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c3ca4ead676b4547ea7e17b1a67ffc43fc9e9a70f9fbbc6dfbe03a6615799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 04:08:44 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 04:08:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 04:08:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 04:08:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 04:08:50 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 04:08:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e8b74114ddf2278e01658eb7e01be08056565bae8a2955645300b982fb0f2`  
		Last Modified: Sat, 05 Feb 2022 04:09:53 GMT  
		Size: 4.4 MB (4398315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76361110853d49e5895bb2123f92f8e3f8f1a08ce01c8ccda76acb70a73d7e22`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a80240856cec2d4b5bcd8aaff898e547e4b7572d85156a941620aaf5d1b432`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2-linux`

```console
$ docker pull nats@sha256:7d5e0768fec0607c8aca58d0f15fa00ca535c5abffaef46aaf4196657521a605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.2-linux` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2-nanoserver`

```console
$ docker pull nats@sha256:586fed106de60d6bebea6665796e0c0f4b44125970b5fd123f558dac8c964dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats:2.7.2-nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:7a1ab2e6e8274fa48286f74bdc4049613f4a195b106ad60b1c20d639a7d9e6eb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107616018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65a67e57e8400b4d29c0ad5699f7a280a95dfa3f515fcf965c4bacd3f16c3a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:51:18 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Wed, 09 Feb 2022 20:51:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580b72f9873a54f539c487aadc8937ae832cd2cffdd1af06f368629e058518ef`  
		Last Modified: Wed, 09 Feb 2022 20:52:11 GMT  
		Size: 4.5 MB (4522598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a10b192969d99c1eceb2713eeff85e1048113487b44dafa3d2012754fbdba`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e12c5402b38a673c9ae6c7de6d41c4f00a6c575f7e94336c5d9235c733efe2`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b17a4d20c99029a251a506f8c1b304cb89fbd352d8e4f0729834fae9e52cf3d`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adde8dc40298e7b0637e0543056d95dd5bb5ad4c8db8a6017be7b49527cfd58f`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2-nanoserver-1809`

```console
$ docker pull nats@sha256:586fed106de60d6bebea6665796e0c0f4b44125970b5fd123f558dac8c964dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats:2.7.2-nanoserver-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:7a1ab2e6e8274fa48286f74bdc4049613f4a195b106ad60b1c20d639a7d9e6eb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107616018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65a67e57e8400b4d29c0ad5699f7a280a95dfa3f515fcf965c4bacd3f16c3a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:51:18 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Wed, 09 Feb 2022 20:51:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580b72f9873a54f539c487aadc8937ae832cd2cffdd1af06f368629e058518ef`  
		Last Modified: Wed, 09 Feb 2022 20:52:11 GMT  
		Size: 4.5 MB (4522598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a10b192969d99c1eceb2713eeff85e1048113487b44dafa3d2012754fbdba`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e12c5402b38a673c9ae6c7de6d41c4f00a6c575f7e94336c5d9235c733efe2`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b17a4d20c99029a251a506f8c1b304cb89fbd352d8e4f0729834fae9e52cf3d`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adde8dc40298e7b0637e0543056d95dd5bb5ad4c8db8a6017be7b49527cfd58f`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2-scratch`

```console
$ docker pull nats@sha256:7d5e0768fec0607c8aca58d0f15fa00ca535c5abffaef46aaf4196657521a605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.7.2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.7.2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2-windowsservercore`

```console
$ docker pull nats@sha256:33946d4adb965632134b6c514f7e588e27df9e4f7d4e3b555d31c28496fd2181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats:2.7.2-windowsservercore` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:2f206c7404528b4d1b631e8747726f7f32fa0519169bc201b32fc2b826d89a1f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718958093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8800eccde299346c51025ba23593daa22a824125479a0501431412ee4934a6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 15:04:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Feb 2022 18:10:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:48:50 GMT
ENV NATS_SERVER=2.7.2
# Wed, 09 Feb 2022 20:48:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Wed, 09 Feb 2022 20:48:52 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Wed, 09 Feb 2022 20:49:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Feb 2022 20:51:00 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Feb 2022 20:51:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:02 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f49d3791198cf2ea875fd54ce3bb715670742d4a58c00252395ad1b74036662a`  
		Last Modified: Wed, 09 Feb 2022 16:39:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4235aeeb4e8b577cc7aa26c7994ec94c94dd53a38764fc510b330b77cef4abad`  
		Last Modified: Wed, 09 Feb 2022 18:14:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5624de3564dcef1325bc61eea92cfcb7dbc1c7b35b0023cd17b2f17c38e6df9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3f050ab2ed35215f1fa3bd806046f502f70d7e85d3f070bdd6fd744864cf9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58550f980b41b606662c4c2d767cca700cbd91b7ec3445c99c5044ca946d586b`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5343d460a59e635dddf02a131dadf49fd2316ad0fef64a08af5e30a3cba30cb5`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 364.5 KB (364524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd6e130904f62e22c3a23ea8b080883ee9bbb534b2db618e0a38cab2766151e`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 4.9 MB (4865553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac13c2b0fa7ddd6703c6c46640b9752b4b5be3aac511ccf5af6c20188a55152`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff779110ef51e3be2fae7dc9e966b4392f3dc10973c23dc689c8c5e78e35494`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9efdff7b3152cb65b604c10ab9822a72e900481f5815179012a1c7a945f9567`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb94adbb9b65f8ab12036ec18b5b9903bb67aa43ed6e10f680078e35eb76c4fe`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.7.2-windowsservercore-1809`

```console
$ docker pull nats@sha256:33946d4adb965632134b6c514f7e588e27df9e4f7d4e3b555d31c28496fd2181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats:2.7.2-windowsservercore-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:2f206c7404528b4d1b631e8747726f7f32fa0519169bc201b32fc2b826d89a1f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718958093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8800eccde299346c51025ba23593daa22a824125479a0501431412ee4934a6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 15:04:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Feb 2022 18:10:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:48:50 GMT
ENV NATS_SERVER=2.7.2
# Wed, 09 Feb 2022 20:48:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Wed, 09 Feb 2022 20:48:52 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Wed, 09 Feb 2022 20:49:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Feb 2022 20:51:00 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Feb 2022 20:51:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:02 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f49d3791198cf2ea875fd54ce3bb715670742d4a58c00252395ad1b74036662a`  
		Last Modified: Wed, 09 Feb 2022 16:39:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4235aeeb4e8b577cc7aa26c7994ec94c94dd53a38764fc510b330b77cef4abad`  
		Last Modified: Wed, 09 Feb 2022 18:14:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5624de3564dcef1325bc61eea92cfcb7dbc1c7b35b0023cd17b2f17c38e6df9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3f050ab2ed35215f1fa3bd806046f502f70d7e85d3f070bdd6fd744864cf9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58550f980b41b606662c4c2d767cca700cbd91b7ec3445c99c5044ca946d586b`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5343d460a59e635dddf02a131dadf49fd2316ad0fef64a08af5e30a3cba30cb5`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 364.5 KB (364524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd6e130904f62e22c3a23ea8b080883ee9bbb534b2db618e0a38cab2766151e`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 4.9 MB (4865553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac13c2b0fa7ddd6703c6c46640b9752b4b5be3aac511ccf5af6c20188a55152`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff779110ef51e3be2fae7dc9e966b4392f3dc10973c23dc689c8c5e78e35494`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9efdff7b3152cb65b604c10ab9822a72e900481f5815179012a1c7a945f9567`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb94adbb9b65f8ab12036ec18b5b9903bb67aa43ed6e10f680078e35eb76c4fe`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:8b3fb2423a8cce4607ef30a990b35545afe0a3c613cd05b8eec7b483df268b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:89eb697c14f6556d6fb2703240e48d9600b40b408dda60ae36e262425a4431e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cd50aa7198f5c12f156d09daa0ddc1112236fff6860f120a2251d96ff9eb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 05:59:05 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 05:59:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 05:59:08 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 05:59:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802d7c7e4ac6a66227b2370fdcdf5a6a23823257ca471179abfd0902b956fd7`  
		Last Modified: Sat, 05 Feb 2022 06:00:25 GMT  
		Size: 4.8 MB (4753836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426dd83cc6600f256ef35338c32eaf3d0399bab79c1246ec09184bdd1ea5b1f`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93f969dc9e9707d1fb2f5eaf6e9636680ca5b3cdfe45b8466a97b0105f036ba`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:26c9fd5ce79bfefe188314878ab0f821a0fbca95fcfbe50f92e81d7f4484ec10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7052346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b52e6eb1b52cca05de6f415e6236b2bd399ce0fb9f1d1ce06066a1558de8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 00:57:59 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 00:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 00:58:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 00:58:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e778c855e77141dc3829b1882837f8ec9f4bc5a650dd40a2917a225e1c15d0d`  
		Last Modified: Sat, 05 Feb 2022 01:00:11 GMT  
		Size: 4.4 MB (4419922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8accecf8efa4c43a09a141647ccf09dc6a56558b970610993d7fdbee2275956f`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7dff5d8e4ec08b7521acbd3a01a86b9f803f821c99252b840a0491493b43b`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9f1dff6dca496cefa436b4db1fa8fa857eb557bd0a6e6760c9b296f096bde9e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6847919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc4a088149c39457ad06caa0dedec762d0dcf09f2ae4743592c4d418f8e890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 06:12:22 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 06:12:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 06:12:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 06:12:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 06:12:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 06:12:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603aa49db7f9a89152dcd7cdf78b402ef16aff3bb40294f6c66a933f07378ee0`  
		Last Modified: Sat, 05 Feb 2022 06:14:40 GMT  
		Size: 4.4 MB (4412155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ab40c3eba476ac4d53154b86201d8626e858e7ed7651fc1045021e03587fee`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ec7b9832ec0d741d78be9c59991717e8a0a7b188c6ac0252cee24c879dcfcf`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b23b110a6166fdd559bbdf992cff078caa3eeb7e37fa86d2cf2765bdddd7898
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c3ca4ead676b4547ea7e17b1a67ffc43fc9e9a70f9fbbc6dfbe03a6615799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 04:08:44 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 04:08:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 04:08:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 04:08:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 04:08:50 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 04:08:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e8b74114ddf2278e01658eb7e01be08056565bae8a2955645300b982fb0f2`  
		Last Modified: Sat, 05 Feb 2022 04:09:53 GMT  
		Size: 4.4 MB (4398315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76361110853d49e5895bb2123f92f8e3f8f1a08ce01c8ccda76acb70a73d7e22`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a80240856cec2d4b5bcd8aaff898e547e4b7572d85156a941620aaf5d1b432`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.15`

```console
$ docker pull nats@sha256:8b3fb2423a8cce4607ef30a990b35545afe0a3c613cd05b8eec7b483df268b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:89eb697c14f6556d6fb2703240e48d9600b40b408dda60ae36e262425a4431e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cd50aa7198f5c12f156d09daa0ddc1112236fff6860f120a2251d96ff9eb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 05:59:05 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 05:59:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 05:59:08 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 05:59:08 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 05:59:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6802d7c7e4ac6a66227b2370fdcdf5a6a23823257ca471179abfd0902b956fd7`  
		Last Modified: Sat, 05 Feb 2022 06:00:25 GMT  
		Size: 4.8 MB (4753836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426dd83cc6600f256ef35338c32eaf3d0399bab79c1246ec09184bdd1ea5b1f`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93f969dc9e9707d1fb2f5eaf6e9636680ca5b3cdfe45b8466a97b0105f036ba`  
		Last Modified: Sat, 05 Feb 2022 06:00:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:26c9fd5ce79bfefe188314878ab0f821a0fbca95fcfbe50f92e81d7f4484ec10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7052346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b52e6eb1b52cca05de6f415e6236b2bd399ce0fb9f1d1ce06066a1558de8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 00:57:59 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 00:58:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 00:58:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 00:58:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 00:58:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e778c855e77141dc3829b1882837f8ec9f4bc5a650dd40a2917a225e1c15d0d`  
		Last Modified: Sat, 05 Feb 2022 01:00:11 GMT  
		Size: 4.4 MB (4419922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8accecf8efa4c43a09a141647ccf09dc6a56558b970610993d7fdbee2275956f`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc7dff5d8e4ec08b7521acbd3a01a86b9f803f821c99252b840a0491493b43b`  
		Last Modified: Sat, 05 Feb 2022 01:00:09 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:9f1dff6dca496cefa436b4db1fa8fa857eb557bd0a6e6760c9b296f096bde9e9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6847919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcc4a088149c39457ad06caa0dedec762d0dcf09f2ae4743592c4d418f8e890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 06:12:22 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 06:12:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 06:12:26 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 06:12:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 06:12:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 06:12:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603aa49db7f9a89152dcd7cdf78b402ef16aff3bb40294f6c66a933f07378ee0`  
		Last Modified: Sat, 05 Feb 2022 06:14:40 GMT  
		Size: 4.4 MB (4412155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ab40c3eba476ac4d53154b86201d8626e858e7ed7651fc1045021e03587fee`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ec7b9832ec0d741d78be9c59991717e8a0a7b188c6ac0252cee24c879dcfcf`  
		Last Modified: Sat, 05 Feb 2022 06:14:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8b23b110a6166fdd559bbdf992cff078caa3eeb7e37fa86d2cf2765bdddd7898
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7114722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c3ca4ead676b4547ea7e17b1a67ffc43fc9e9a70f9fbbc6dfbe03a6615799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Sat, 05 Feb 2022 04:08:44 GMT
ENV NATS_SERVER=2.7.2
# Sat, 05 Feb 2022 04:08:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7160b8fce84427cb9da6862e365ccaf1c5bcc1ab37c5a74a50bbf1c18dd0cef3' ;; 		armhf) natsArch='arm6'; sha256='8e74741ad48b680a9fad05af30d352fb316754feb37ef7a84d5d660a69d5ba1e' ;; 		armv7) natsArch='arm7'; sha256='b1bb6a5e9159e37efc8c823a217c343d0580564c2e836d07c93b43633bb46245' ;; 		x86_64) natsArch='amd64'; sha256='6f58d9df9d9ab47d93ecb06d1041c86a784fc61c3475ab994e144e8ae15584d9' ;; 		x86) natsArch='386'; sha256='5276a5af79f6e9b8a07c6c63886386f8d154f38ab743a8f929b64dad38056b9a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 05 Feb 2022 04:08:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 05 Feb 2022 04:08:50 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 05 Feb 2022 04:08:50 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Feb 2022 04:08:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e8b74114ddf2278e01658eb7e01be08056565bae8a2955645300b982fb0f2`  
		Last Modified: Sat, 05 Feb 2022 04:09:53 GMT  
		Size: 4.4 MB (4398315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76361110853d49e5895bb2123f92f8e3f8f1a08ce01c8ccda76acb70a73d7e22`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a80240856cec2d4b5bcd8aaff898e547e4b7572d85156a941620aaf5d1b432`  
		Last Modified: Sat, 05 Feb 2022 04:09:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:178f84bff4dab5a40bf69ba0a004b2a93b54aef07e24236bccd933fea56ed5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2565; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:7a1ab2e6e8274fa48286f74bdc4049613f4a195b106ad60b1c20d639a7d9e6eb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107616018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65a67e57e8400b4d29c0ad5699f7a280a95dfa3f515fcf965c4bacd3f16c3a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:51:18 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Wed, 09 Feb 2022 20:51:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580b72f9873a54f539c487aadc8937ae832cd2cffdd1af06f368629e058518ef`  
		Last Modified: Wed, 09 Feb 2022 20:52:11 GMT  
		Size: 4.5 MB (4522598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a10b192969d99c1eceb2713eeff85e1048113487b44dafa3d2012754fbdba`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e12c5402b38a673c9ae6c7de6d41c4f00a6c575f7e94336c5d9235c733efe2`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b17a4d20c99029a251a506f8c1b304cb89fbd352d8e4f0729834fae9e52cf3d`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adde8dc40298e7b0637e0543056d95dd5bb5ad4c8db8a6017be7b49527cfd58f`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:7d5e0768fec0607c8aca58d0f15fa00ca535c5abffaef46aaf4196657521a605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:586fed106de60d6bebea6665796e0c0f4b44125970b5fd123f558dac8c964dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats:nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:7a1ab2e6e8274fa48286f74bdc4049613f4a195b106ad60b1c20d639a7d9e6eb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107616018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65a67e57e8400b4d29c0ad5699f7a280a95dfa3f515fcf965c4bacd3f16c3a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:51:18 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Wed, 09 Feb 2022 20:51:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580b72f9873a54f539c487aadc8937ae832cd2cffdd1af06f368629e058518ef`  
		Last Modified: Wed, 09 Feb 2022 20:52:11 GMT  
		Size: 4.5 MB (4522598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a10b192969d99c1eceb2713eeff85e1048113487b44dafa3d2012754fbdba`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e12c5402b38a673c9ae6c7de6d41c4f00a6c575f7e94336c5d9235c733efe2`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b17a4d20c99029a251a506f8c1b304cb89fbd352d8e4f0729834fae9e52cf3d`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adde8dc40298e7b0637e0543056d95dd5bb5ad4c8db8a6017be7b49527cfd58f`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:586fed106de60d6bebea6665796e0c0f4b44125970b5fd123f558dac8c964dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:7a1ab2e6e8274fa48286f74bdc4049613f4a195b106ad60b1c20d639a7d9e6eb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107616018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65a67e57e8400b4d29c0ad5699f7a280a95dfa3f515fcf965c4bacd3f16c3a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:51:18 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Wed, 09 Feb 2022 20:51:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580b72f9873a54f539c487aadc8937ae832cd2cffdd1af06f368629e058518ef`  
		Last Modified: Wed, 09 Feb 2022 20:52:11 GMT  
		Size: 4.5 MB (4522598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a10b192969d99c1eceb2713eeff85e1048113487b44dafa3d2012754fbdba`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e12c5402b38a673c9ae6c7de6d41c4f00a6c575f7e94336c5d9235c733efe2`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b17a4d20c99029a251a506f8c1b304cb89fbd352d8e4f0729834fae9e52cf3d`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adde8dc40298e7b0637e0543056d95dd5bb5ad4c8db8a6017be7b49527cfd58f`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:7d5e0768fec0607c8aca58d0f15fa00ca535c5abffaef46aaf4196657521a605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:33946d4adb965632134b6c514f7e588e27df9e4f7d4e3b555d31c28496fd2181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats:windowsservercore` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:2f206c7404528b4d1b631e8747726f7f32fa0519169bc201b32fc2b826d89a1f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718958093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8800eccde299346c51025ba23593daa22a824125479a0501431412ee4934a6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 15:04:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Feb 2022 18:10:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:48:50 GMT
ENV NATS_SERVER=2.7.2
# Wed, 09 Feb 2022 20:48:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Wed, 09 Feb 2022 20:48:52 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Wed, 09 Feb 2022 20:49:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Feb 2022 20:51:00 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Feb 2022 20:51:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:02 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f49d3791198cf2ea875fd54ce3bb715670742d4a58c00252395ad1b74036662a`  
		Last Modified: Wed, 09 Feb 2022 16:39:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4235aeeb4e8b577cc7aa26c7994ec94c94dd53a38764fc510b330b77cef4abad`  
		Last Modified: Wed, 09 Feb 2022 18:14:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5624de3564dcef1325bc61eea92cfcb7dbc1c7b35b0023cd17b2f17c38e6df9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3f050ab2ed35215f1fa3bd806046f502f70d7e85d3f070bdd6fd744864cf9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58550f980b41b606662c4c2d767cca700cbd91b7ec3445c99c5044ca946d586b`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5343d460a59e635dddf02a131dadf49fd2316ad0fef64a08af5e30a3cba30cb5`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 364.5 KB (364524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd6e130904f62e22c3a23ea8b080883ee9bbb534b2db618e0a38cab2766151e`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 4.9 MB (4865553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac13c2b0fa7ddd6703c6c46640b9752b4b5be3aac511ccf5af6c20188a55152`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff779110ef51e3be2fae7dc9e966b4392f3dc10973c23dc689c8c5e78e35494`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9efdff7b3152cb65b604c10ab9822a72e900481f5815179012a1c7a945f9567`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb94adbb9b65f8ab12036ec18b5b9903bb67aa43ed6e10f680078e35eb76c4fe`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:33946d4adb965632134b6c514f7e588e27df9e4f7d4e3b555d31c28496fd2181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:2f206c7404528b4d1b631e8747726f7f32fa0519169bc201b32fc2b826d89a1f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718958093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8800eccde299346c51025ba23593daa22a824125479a0501431412ee4934a6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 02 Feb 2022 19:28:56 GMT
RUN Install update 1809-amd64
# Wed, 09 Feb 2022 15:04:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Feb 2022 18:10:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:48:50 GMT
ENV NATS_SERVER=2.7.2
# Wed, 09 Feb 2022 20:48:51 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.7.2/nats-server-v2.7.2-windows-amd64.zip
# Wed, 09 Feb 2022 20:48:52 GMT
ENV NATS_SERVER_SHASUM=12706f570a4d237c4d59ad8308e40f86b5322338b51e67e84b9c26ea019221b2
# Wed, 09 Feb 2022 20:49:44 GMT
RUN Set-PSDebug -Trace 2
# Wed, 09 Feb 2022 20:51:00 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 09 Feb 2022 20:51:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:02 GMT
EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:03 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1bd78008c728d8f9e56dc2093e6eb55f0f0b1aa96e5d0c7ccc830c5f60876cdf`  
		Size: 995.4 MB (995381853 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f49d3791198cf2ea875fd54ce3bb715670742d4a58c00252395ad1b74036662a`  
		Last Modified: Wed, 09 Feb 2022 16:39:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4235aeeb4e8b577cc7aa26c7994ec94c94dd53a38764fc510b330b77cef4abad`  
		Last Modified: Wed, 09 Feb 2022 18:14:09 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5624de3564dcef1325bc61eea92cfcb7dbc1c7b35b0023cd17b2f17c38e6df9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3f050ab2ed35215f1fa3bd806046f502f70d7e85d3f070bdd6fd744864cf9a`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58550f980b41b606662c4c2d767cca700cbd91b7ec3445c99c5044ca946d586b`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5343d460a59e635dddf02a131dadf49fd2316ad0fef64a08af5e30a3cba30cb5`  
		Last Modified: Wed, 09 Feb 2022 20:51:50 GMT  
		Size: 364.5 KB (364524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd6e130904f62e22c3a23ea8b080883ee9bbb534b2db618e0a38cab2766151e`  
		Last Modified: Wed, 09 Feb 2022 20:51:49 GMT  
		Size: 4.9 MB (4865553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac13c2b0fa7ddd6703c6c46640b9752b4b5be3aac511ccf5af6c20188a55152`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff779110ef51e3be2fae7dc9e966b4392f3dc10973c23dc689c8c5e78e35494`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9efdff7b3152cb65b604c10ab9822a72e900481f5815179012a1c7a945f9567`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb94adbb9b65f8ab12036ec18b5b9903bb67aa43ed6e10f680078e35eb76c4fe`  
		Last Modified: Wed, 09 Feb 2022 20:51:47 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
