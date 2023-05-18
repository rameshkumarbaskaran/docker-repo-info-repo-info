## `nats:2-alpine`

```console
$ docker pull nats@sha256:1a7b320b294218d11b48ddcd1552a18a74ae8790c80ba5372726c58d0a5ee295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:7544f1dfe4b270789a68e2056135467d525da411f331f43640150b0642dee693
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8802768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ada7bbdb360a5406551ced3593bc48e57c6cea5ee5d502e1a0df2437156d06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:19:49 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:19:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:19:52 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:19:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:19:52 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:19:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba69a821f226517d8763fd5007b51eeb8a68e40f7fb32dec75e13297ea1cb49`  
		Last Modified: Thu, 18 May 2023 21:20:19 GMT  
		Size: 5.4 MB (5404276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ad2f9c9076c4ccedf3a056bf6e996a658fa5ece8cc35913e4728d58617e8b3`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb3c123b7bd114e7897ddf602c16bcd18f034abda3ee53d91a108b71c624faa`  
		Last Modified: Thu, 18 May 2023 21:20:18 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:08b7d50259bf79d1f0cc5476da2707cbe3723f8b25ececd27b4e20f5c3ba036e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8325871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676517e73baa5d6c0a13a665dcf0412659d93274c96643829ff67835d5e4905d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:04 GMT
ADD file:f87a991e2e9f185fd4a88569d86a9b8e5bc07182e7fa613b95acab25986f2a6c in / 
# Tue, 09 May 2023 23:11:04 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:49:22 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:49:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:49:24 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:49:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:49:24 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:49:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:49:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:015ee8d9fb3dca1b18815f1e4ee0d325d1f40cde6f2df4dd307918f7b69167d7`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.2 MB (3155679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06976c3bb336d8c3936e2bbb8d27dbd5b805054e1064aaf7c651d6fd5523aa71`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 5.2 MB (5169192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c85a9f3b4246d93c82583c9d4336cb58688e4b311be41f752bc0c9456a2135`  
		Last Modified: Thu, 18 May 2023 21:49:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6d307fb0f80f02bb15dbdbb0eba31d3a463afa38dca28f6cd0e913798ebf62`  
		Last Modified: Thu, 18 May 2023 21:49:47 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:882066add3894dc13cfadaeec8af9f9fce5b9c3fee92e377a13f0997a88a121f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8071388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574536f22d8de67b2c2f0962d9e7d108bb4b41d07cb13a05ebab5e3b82fe6d63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 22:57:32 GMT
ADD file:eb6b6a885e8ac9bccbf44a5c673b8542c8144bba927376688240446c2f413b10 in / 
# Tue, 09 May 2023 22:57:32 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:57:27 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:57:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:57:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:57:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:57:29 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:57:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:57:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e14425cf8fb9304b9ad4a9d1250e0d4c22e507a334ff747fa69b804500afc113`  
		Last Modified: Tue, 09 May 2023 22:57:50 GMT  
		Size: 2.9 MB (2911117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213de106e11b3e7261faf48da426167af8702e8a56ab0237f786ba0eb864a38d`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 5.2 MB (5159272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5535f74851ba24bbb57849b9f7085eb8441d584ea938b19bdd027f5ccf52a193`  
		Last Modified: Thu, 18 May 2023 21:58:07 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2518eda2d1b2ce9ae4c75acdccc0d3bbe028cfbdf30d7e173dfa82e489af6ec`  
		Last Modified: Thu, 18 May 2023 21:58:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:36980286981e9058cd3f3a1f58fb92741d5ba73ff1a66d3b8ef7b98e23ab8377
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8313998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1348d24d9abc62396994637b0c3153212850856ce4ab5c1cc49194dd4ef4872e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Thu, 18 May 2023 21:39:41 GMT
ENV NATS_SERVER=2.9.17
# Thu, 18 May 2023 21:39:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='c7cf7bf8c029500d1b51773132ecc13a1fc89f2e080faa6b505da8cb95aa2a0c' ;; 		armhf) natsArch='arm6'; sha256='b09812858f1c957fd1869e21d4b8d64b3b0d6cdf3abb34502167120640f1d5e1' ;; 		armv7) natsArch='arm7'; sha256='970649306f45c78404c42dc5c0ab37fa6d5149501e47a68bef7841a06730a654' ;; 		x86_64) natsArch='amd64'; sha256='4ad2d83dd2fb9cc44a7e078d2e400f37c188b8515100f5de0f10f0eefbeb6b23' ;; 		x86) natsArch='386'; sha256='59c42f21bb6e8a5ef6e101ce6e3c29692b2cc9b1eb28465e67edeb391450626c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 18 May 2023 21:39:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 18 May 2023 21:39:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 18 May 2023 21:39:43 GMT
EXPOSE 4222 6222 8222
# Thu, 18 May 2023 21:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 May 2023 21:39:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8409748378eca62a6e13533d1f6fef38e6b40a7ad726dff04ad548a63ae20313`  
		Last Modified: Thu, 18 May 2023 21:40:03 GMT  
		Size: 5.0 MB (4970150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a822f2037d3c235b73c5f9924d54c4de71f06b2ba22757fc2a059c4f33d5c6`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94f121392ee621f9e3f1aaa44685e70de92e169d23c2c547ba2d5172904b49d`  
		Last Modified: Thu, 18 May 2023 21:40:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
